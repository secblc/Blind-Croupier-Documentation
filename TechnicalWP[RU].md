
# Устройство алгоритма Blind Croupier

В игре участвуют 3 стороны: Игрок (клиентский JavaScript), Банк (смарт-контракт на Solidity) и Крупье (сервер). 

## Подготовка к игре

1. Крупье и Игрок втайне генерируют приватные ключи. Приватный ключ представляет из себя 64-символьную хекс-строку (приватный ключ Ethereum). Затем они вычисляют на их основе публичные ключи, пользуясь правилом вычисления адреса Ethereum. 

Крупье и Игрок отправляют в банк свои публичные ключи, используя метод 

```
/**
 * Sets the new public key for a participant.
 * This key will be used for all further game operations.
 * @param key - a key to submit as a public key
 */
 function submitPublicKey(SigningPublicKey key);
```

2. Игрок отправляет часть своих средств на депозит в Банк, используя метод:

```
/**
 * Puts the money attached to the sender's deposit
 */
 function depositFunds() payable {
```

Все готово к игре.

## Некоторые определения

1. Подпись это результат применение функции `ecsign` к числу `data` и приватному ключу `privateKey`. Результатом подписи является три числа: `signature = { r, v, s}`. Для проверки подписи необходимо передать функции `ecrecover` число `data` и подпись `signature`. Результатом ее работы будет публичный ключ `publicKey`, который должен точно совпать с публичным ключом, сгенерированным на основе `privateKey` алгоритмом *Ethereum*. Это будет означать, что подпись верна.

2. `gameId` это уникальный номер партии между Игроком и Крупье, считая с нуля. После успешного завершения партии, `gameId` увеличивается на единицу.

3. `salt` добавляется ко всем подписываемым сторонами сообщениям.

```
  salt = sha3(croupierAddress ^ playerAddress ^ gameId)
```

4. `BET_TOKEN`, `REPLACEMENT_TOKEN`, `SEED_TOKEN` - некие заранее выбранные и фиксированные в Банке числа.

5. В игре участвует 4 случайных сида: сиды Игрока (`seedId` 0..1) и сиды Крупье (`seedId` 0..1). Все они представляют из себя 256-разрядные неотрицательные целые числа и вычисляются следующим образом:

```
    msg = [SEED_TOKEN, gameId, seedId]
```

после чего `msg` подписывается приватным ключом соответствующего участника (Крупье или Игрока). Получается подпись `signature = { r, s, v }`. Искомый сид:

```
    seed = r & 0xffffffff
````

6. `chipCost` - стоимость игровой фишки в Wei. Определяется путем вызова 

```
    /**
     * Returns the current game chip cost
     * @return cost - the current game chip cost
     */
    function getChipCost() constant returns (WeiCount cost);
```

из Банка.

7. Смешивание двух случайных сидов `s1` и `s2` производится так:

```
    s3 = s1 ^ s2
```

8. Для игры используется простой генератор псевдослучайных чисел (PRNG) на основе заданного случайного сида:

```
    /**
     * Returns a randomly generated unsigned 32-bit integer from `min` to `max` (inclusively) using the random `seed` given
     * @param  seed - random seed to use
     * @param  min - a minimum value allowed (inclusively)
     * @param  max - a maximum value allowed (inclusively)
     * @return nextSeed - seed to use for the next integer generated (as the next input to `generate****` call)
     * @return randomValue - a random `uint32` value between `min` and `max` (inclusively)
     */
    function generateInt(RandomSeed seed, uint32 min, uint32 max) constant returns (RandomSeed nextSeed, uint32 randomValue) {
        nextSeed = seed + 1;
        Sha3Hash hash = sha3(seed);
        randomValue = uint32(uint(hash) & 0xffffffff) % (max - min + 1) + min;
    }
```

9. На основе данного PRNG производится тасовка колоды, расположенной изначально в заранее оговоренном порядке.

## Партия

1. Игрок определяет свою ставку (`bet` от `1` до `10` и `level` от `1` до `5`). После этого он формирует сообщение:

```
msg = [BET_TOKEN, level << 8, bet ,salt]
```

подписывает его своим приватным ключом и отправляет Крупье. 

2. Крупье отправляет это сообщение в Банк (в фоне).

```
/**
     * Accepts the signed Player's bet
     * @param  croupier - Croupier's address
     * @param  player - Player's address
     * @param  bet - a bet to put (1..10)
     * @param  level - a level to play on (1..5)
     * @param  betSignature - the signature of the message, consisting of `croupier`, `player`, `bet`, `level` and game salt **expandtype: Signature **
     */
    function submitBet(address croupier, address player, Bet bet, Level level, Signature betSignature);
```

3. Крупье вычисляет сид Крупье 0 и отправляет его в Банк (в фоне), а также сообщает Игроку.

```
/**
     * Accepts the seed provided by Croupier. Seed is provided as a `Signature` object,
     * must equal the signature of the message, consisting of `player`, `croupier`, current game index, `seedID` and game salt
     * @param  croupier - Croupier's address
     * @param  player - Player's address
     * @param  signature - the signature to be treated as seed **expandtype: Signature **
     * @param  seedID - seed id (0 or 1)
     */
    function submitCroupierSeedAsSignature(address croupier, address player, Signature signature, uint seedID);
```

4. Банк перечисляет ставку `bet * level * chipCost` со счета Игрока на счет Крупье.

5. Игрок вычисляет сид Игрока 0 и передает его Крупье.

6. Крупье передает сид Игрока 0 в Банк (в фоне).

```
    /**
     * Accepts the seed provided by Player. Seed is provided as a `Signature` object,
     * must equal the signature of the message, consisting of `player`, `croupier`, current game index, `seedID` and game salt
     * @param  croupier - Croupier's address
     * @param  player - Player's address
     * @param  signature - the signature to be treated as seed **expandtype: Signature **
     * @param  seedID - seed id (0 or 1)
     */
    function submitPlayerSeedAsSignature(address croupier, address player, Signature signature, uint seedID);
```

7. Игрок смешивает сид Игрока 0 и сид Крупье 0 и получает сид игры 0.

8. Игрок тасует колоду, используя сид игры 0 и вытягивает 5 карт.

9. Игрок принимает решение о замене карт и формирует команду замены, например:

```
    replacementOrder [1, 0, 1, 0, 1]
```

`1` означает замену, а `0` - отказ от замены карты, стоящей в этой позиции.

10. Игрок формирует сообщение:

```
    const msg = [
        REPLACEMENT_TOKEN,
        replacementOrder[0],
        replacementOrder[1] << 1,
        replacementOrder[2] << 2,
        replacementOrder[3] << 3,
        replacementOrder[4] << 4,
        salt,
    ];
```

подписывает его своим приватным ключом и отправляет Крупье.

11. Крупье отправляет это сообщение в Банк (в фоне).

```
/**
     * @param  croupier - Croupier's address
     * @param  player - Player's address
     * @param  replacementOrder - an array of `HAND_SIZE` 0's and 1's, telling which cards in hand to replace
     * @param  replacementSignature - a `Signature` of the message, consisting of `croupier`, `player`, `replacementOrder` and game salt **expandtype: Signature **
     */
    function submitReplacementOrder(address croupier, address player, uint8[HAND_SIZE] replacementOrder, Signature replacementSignature);
```

12. Крупье вычисляет сид Крупье 1 и отправляет его в Банк (в фоне), а также сообщает его Игроку.

13. Игрок вычисляет сид Игрока 1 и сообщает его Крупье.

14. Крупье отправляет сид Игрока 1 в Банк (в фоне).

15. Игрок смешивает сид Игрока 1 и сид Крупье 1, получая сид игры 1. На основ этого сида он тасует остаток колоды и вытягивает нужное количество карт замены, получая финальную руку.

16. Крупье в фоне дает команду Банку рассчитать партию:

```
/**
  * Performs the game calculation and all payouts
  * @param  croupier - Croupier's address
  * @param  player - Player's address
  */
 function submitGameResult(address croupier, address player);
```

Банк в фоне воспроизводит партию на основе полученных данных и выплачивает Игроку его выигрыш (если таковой имеется).

17. Тем временем, Игрок и Крупье могут начинать следующую партию.

## Возможные попытки мошенничества

Система построена так, что Крупье и Игрок взаимно не доверяют друг другу, но полностью доверяют Банку. Поэтому они оба могут предпринимать попытки обмануть другую сторону, чтобы увеличить свой выигрыш. Рассмотрим некоторые схемы мошенничества:

1. Игрок отказывает от игры в любой момент: после передачи Игроком подписанной ставки, Крупье отправляет команду ставки и сид Крупье 0 в Банк, после чего Банк списывает ставку с депозита Игрока. Игрок должен завершить игру, чтобы иметь шанс вернуть ставку. 

2. Крупье отказывается от игры до отправки сида Игрока 1 в Банк: Игрок может сам отправить сид Игрока 1 в Банк и произвести расчет партии.

3. Крупье отказывается от игры до отправки сида Крупье 1 в Банк: Игрок может выждать оговоренное время и воспользоваться специальной функцией:

```
    /**
     * If Croupier has failed to submit the second seed, performs the game calculation and pays the `player` his win
     * @param  croupier - Croupier's address
     * @param  player - Player's address
     */
    function complainNoSecondCroupierSeed(address croupier, address player) {
```

и Банк произведет расчет партии на основе имеющихся данных.

4. Крупье отказывается от игры до отправки сида Игрока 0 в Банк: Игрок может сам отправить сид Игрока 0 в Банк, после чего см. п. 3.

5. Крупье отказывается от игры до отправки сида Крупье 0 в Банк: ставка не была списана. Игрок не пострадал.

6. Крупье пытается отправить неверную ставку или команду замены в Банк: невозможно, ставка и команда замены подписаны приватным ключом Игрока и не будут приняты Банком.

7. Кто-либо пытается отправить ставку или команду замены после того, как они были приняты Банком: повторная отправка разрешена только для Крупье, т.к. он заведомо не может знать никакую другую ставку (с подписью) и команду замены (с подписью), кроме тех, которые ему сообщил Игрок.

8. Кто-либо пытается отправить неверный сид: невозможно, сид однозначно вычисляется для каждого `gameId` и приватного ключа. Априори сид знает только его владелец, но проверить валидность сида после его публикации может любой желающий (в т.ч. Банк).

