# BLINDCROUPIER.io White Paper
#### Jul 21, 2017 <img align="right" src="https://user-images.githubusercontent.com/30338333/28491741-d8bd2b18-6f28-11e7-9582-d9cbab2d1a06.png" width="95">

Blind Croupier is a **gambling software development company** [Business to business], providing decentralized, fair and transparent gambling solutions for casinos.

**Completely fair** — a casino can't possibly gain any advantages except for those defined by specific game rules, including the fair random generation.

**Absolutely transparent** —  all the transactions, software source code, are open to the public and available for revision.

**Decentralized** — this guarantees that a player, obeying the game rules, will certainly receive his award (paid to his Ethereum wallet), regardless of the casino’s reservations.


- [Introduction](#introduction)
- [Token WIN](#token-win)
  * [The Privilege Auction](#the-privilege-auction)
  * [Token Distribution](#the-privilege-auction)
  * [About Token Distribution Model](#about-token-distribution-model)
- [Put Your Tokens To Work](#put-your-tokens-to-work)
- [Raised Funds Distribution](#raised-funds-distribution)
- [Roadmap](#roadmap)
  * [Stage 1: Minimal Viable Product (MVP)](#stage-1-spring-summer-2017---minimal-viable-product-mvp)
  * [Stage 2: Development and Legal](#stage-2-fall-2017---development-and-legal) 
  * [Stage 3: Testing and Presentation](#stage-3-winter-2017-2018-testing-and-presentation)
  * [Stage 4: Advanced Platform and Blind Jackpot Fund](#stage-4-spring-summer-2018-advanced-platform-and-blind-jackpot-fund)
- [Background](#Background)
- [Algorithm and Video Poker Implementation](#algorithm-and-video-poker-implementation)
  * [Blind Chips](#blind-chips)
  * [Video Poker Game Rules](#video-poker-game-rules)
  * [Alghoritm Implementation](#alghoritm-implementation)
- [The Problems Solved By the Algorithm](#the-problems-solved-by-the-algorithm)
  * [Pseudo-Random Number Generation (PRNG)](#pseudo-random-number-generation-prng)
  * [Gaming Speed and Slow Staking](#gaming-speed-and-slow-staking)
  * [Fairness check](#fairness-check)
  * [Third Party Random Sources](#third-party-random-sources)
  * [The Jackpot Validation](#the-jackpot-validation)
- [Technologies and Methodologies](#technologies-and-methodologies)
- [iGaming Market](#igaming-market)
- [House Edge or Casino's Revenue](#house-edge-or-casinos-revenue)
- [Blind Croupier Business model](#blind-croupier-business-model)
  * [Royalties](#royalties)
  * [Fees](#fees)
  * [Custom Services](#custom-services)
  * [The Marketing Strategy](#the-marketing-strategy)
  * [Motivation and Mission](#motivation-and-mission)
  * [Premises](#Premises)
- [Turnkey Solution For Operators Casino](#turnkey-solution-for-operators-casino)
- [Blind Croupier Platform](#blind-croupier-platform)
  * [Description](#Description)
  * [Mobile Casino](#mobile-casino)
  * [Operation under BlindCroupier license](#operation-under-blindcroupier-license)
- [The Blind Jackpot Fund](#the-blind-jackpot-fund)
  * [BlindJackpot Main Features](#blindjackpot-main-features)
  * [Jackpot Winner Determining Algorithm](#jackpot-winner-determining-algorithm)
  

# Introduction

The moment smart contracts emerged, the gambling industry changed forever, making casinos more transparent and fair. A player can easily check all the transactions, confirm the source code validity and check a casino's advantage in no time.

It's also obvious that the industry will not move forward to a new stage of online gambling until there is a complete solution, providing both a platform and games while taking advantage of smart contracts. We believe that the market calls for the advance technology provides, which, in turn, drives the market to grow.

Blind Croupier will open a new door in online gambling and provide all the tools necessary to start your own decentralized casino. We are sure that our solution will create a new start for the industry, and that our company will take the lead in this emerging market, which has already **reached 42Billions USD.**

We have already done a tremendous job, starting from the general concept and ending up with a working beta-version of a video poker game. We have completely solved the problems of slow staking and fair, no oracle involved. (An oracle is a third-party data supplier for a smart-contract, pseudo-random number generation).

This document shows how our products can solve the existing industry problems, which innovations we are introducing, what advantage our investors are going to receive and our current goals.

# Token WIN

Токен WIN - это валюта проекта Blind Croupier служащая измерителем стоимости других товаров и услуг. Все категории участников могут использовать WIN для оплаты продуктов и услуг, связанных с проектом Blind Croupier. К тому же WIN может быть использован для оплаты или обмена среди всех участников обращения токена WIN.

## Token Distribution

**Emission:** The total amount of WIN Tokens emitted is 500,000,000 WIN. There will be no further emission. 
*All unsold tokens (if any) are destroyed at the end of every period* 

**Token Price:** Period 0 price: 0.07$
Period 1 price 1 WIN = $0.1$
In each new period, the price is increased by 0.7% from the price in the previous period. 
*If  20% of more of tokens were destroyed in the period, then the price would be maintained at the same level*

| Period  | Price | Offer | Demand  | Tokens Burnt % |
|---|:-:|---|---|---|
| 1  | 0.1$  | 10,000,000WIN | 10,000,000WIN  | 0%  |
| 2 |  0.1007 | 1,000,000WIN | 1,000,000WIN  | 0%  |
| 3-69 | -  | -  | -  |  - |
| 70 | 0.140$  | 1,000,000WIN | 800,000,000WIN  | **20%** |
| 71  | **0.140$**  | 1,000,000WIN  | 1,000,000WIN  | 0%  |

**5,000,000WIN:** Offered for Period 0. Это небольшой период для "раних птичек". Период будет завершен когда все доступные для него токены будут распределены или вместе с началом с Period 1 то есть ** УКАЗАТЬ ДАТУ**. *All the unsold tokens are destroyed at the end of the period.*

**15,000,000WIN** Offered for Token Distribution Period 1, ***который начнется УКАЗАТЬ ДАТУ**  The period lasts 161 hours (or until all the tokens are sold), after that the next period begins instantly. *All the unsold tokens are destroyed at the end of the period.*

 **366,000,000WIN:**  Split for periods 2-367. For each period, 1,000,000 WIN is available for 23 hours (or until all the tokens are sold). *All the unsold tokens are destroyed at the end of the period.*
 
**100,000,000WIN:** Reserved by Blind Croupier to award project participants for their work and are considered a long-term investment, **и поддержания баланса маркет мейкера**. The are put on hold and will be unlocked after 12 months.

**5,000,000WIN:** This tokens will be transferred to the market maker balance. A market maker is a dealer/bot/broker, storing WIN tokens and making transactions to maintain higher tokens liquidity on the market. 

**5,000,000WIN:** Reserved for the 'bounty' campaign. Tokens are distributed after each period and transferred to the participants' balances each 7 days. Please read more about getting involved into bounty campaign on our site.

**4,000,000WIN:** Reserved for the current and future Blind Croupier advisor. 

## The Privilege Auction

Top 5 Investors (considering ETH spent by the end of Period 25) receive a free platform subscription for 12 months (as soon as platform is released) and a discounted royalty (7% instead of 13%) for 12 months. To participate, they need to invest from a single Ethereum wallet.

The top Investor (considering ETH spend by the end of Period 25) will (in addition to the above bonuses) receive a unique Videopoker installation. We will offer this installation to these exclusive customers. This is a great opportunity be first to enter the transparent online gambling market. Videopoker is platform for MainNet release in September - October 2017 (beta is available right now).

*If the winner fails to contact us for verification and getting the award within 14 days from the end of Period 25, the bonus will be offered to the next Investor in the Top table until we are able to verify him. We reserve the right of the winner to give/sell the privileges gained to the third parties, but not earlier than the verification occurs.*

# About Token Distribution Model

The aforementioned Token Distribution model was developed to solve investors' problems which are, by our opinion and [blockchain community opinion](http://vitalik.ca/general/2017/06/09/sales.html), are most relevant.

1. Step-by-step investment - We look at this as at a great opportunity for an investor to look closer to the project, to assess how the given promises are fulfilled and divided the investment into stages. An investor, decided to take part in the Token Distribution will most probably be given a chance to do so. For us it is an opportunity to showcase our products during the Token Distribution and let the market vote for our project, final emission and the token price.

> It's worth mentioning, however, that if an extreme interest rises among the investors, new periods will finish and start without delays, which can, theoretically, lead to the fast end of period 367. But the price will also rise in this case, requiring further roadmap advancement and/or token destruction.

2. The low share boundary - An investor knows the total amount of tokens and their distribution. The only unknown figure is the amount of tokens issued to the market. But in the case we decrease the emission after the investment, the investor's share will grow.

3. Limited emission - 500'000'000 WIN is a maximum emission limited by the smart contract. The total amount of tokens can only decrease.

4. No command center - the Blind Croupier team doesn't possess enough tokens to manipulate price. Even in the case of 50% of the tokens, which are offered to the Token Distribution, are destroyed, Blind Croupier team will own 32% of the total emission. Also, part of the tokens will be send to the market maker, which is to support the stable token market price.

5. Market efficiency - the offered model agility is based on the token price increase in new periods until the investors are satisfied. If the demand decreases, the offer is decreased as well until the offer-demand balance is reached.

# Следование Механизмам Дефляционной Модели

Дефляция - это изъятие из обращения избыточной денежной массы с целью увеличения их покупательной способности. Дефляционный механизм лежит в основе всей экономической модели Blind Croupier, как во время первоначального распределения токенов, так и на протяжении всей дальнейшей жизни проекта. 

Тем самым мы выстариваем зависимость стоимости токена WIN от экономических показателей Blind Croupier. Основной показатель экономической эффективности Blind Croupier это размер полученных роялти отчислений от использующих ПО казино, отчисления составляют 13% от GGR(GGR=ставки-выигрыши).

Минимум 15% от полученной роялти прибыли будет использоваться для **постепенного** выкупа токенов WIN и их выводу из оборота. Чем лучше идут дела у проекта, тем больше средств будет выделено для вывода из оборота токенов, в случае если WIN оказался определенно не дооценен, то соответственно больше WIN будет выведено из оборота. Если же оценка стоимости на рынке окажется сбалансированной - будет выведено не значительное колличество WIN (Чем выше цена токена, то соответственно и на выделенную сумму мы можем купить меньше токенов). 

>Пример: Ожидается, что размер рынка интернет-гейминга в 2018 году достигнет $52млрд, если подключенные к Blind Croupier казино смогут занять минимальные 0.5% от рынка, то их годовой оборот достигнет $260,000,000, GGR в среднем составит 5% или $13,000,000 из которых 13% будут отправлены для Blind Croupier в виде Роялти, что составит $1,690,000, из этой суммы Blind Croupier выделит минимум 15% для следования механизмам дефляционной модели или $253,500 в год. Давайте рассмотрим в ниже приведенной таблице, какое колличество токенов будет уничтоженно при данных условиях, в зависимости от их стоимости:

| Выделено в год  |Средняя цена токена на рынке  | Токенов уничтоженно в год |
|---|---|---|
| $253,500  | $1  |  253,500WIN  |
| $253,500  | $0.5  | 507,000WIN  |
| $253,500  | $0.25  | 1,014,000WIN |
| $253,500  | $0.1  | 2,535,000WIN  |

Как видно из таблицы, когда цена токена снижается, дефляция ускоряется и стабилизирует рынок, соответственно когда стоимость токена WIN  достигнет стабильного уровня, который соответствует размеру будущей экономики Blind Croupier, дефляция будет замедлена. Данная модель постепенно увеличивает покупательную способность токена WIN, в зависимости от экономических показателей проекта Blind Croupier, не прибегая для этого к спекулятивным методам.  

## Ликвидность

Ограниченная эмиссия и постоянный вывод токенов из оборота на всей жизни проекта делает безопасным хранение токенов WIN в долгоcрочной перспективе. Однако это может повлечь за собой не способность токена быть быстро проданным по цене близкой к рыночной или другими словами низкую ликвидность токена на рынке. Для предотвращения подобных ситуаций, как вы уже возможно заметили из раздела [распределения токенов](#about-token-distribution-model), на рынке будет присутствовать маркет-мейкер. Маркет-мейкер хранит на своем балансе токены и другую валюту и принимает активное участие в покупке и продаже токенов WIN по рыночным ценам. Другими словами, если вы захотите приобрести токен WIN на бирже вам не прийдется платить цену выше рыночной чтобы это сделать, также как и не прийдетется выставлять предложение о продаже по цене ниже рыночной - маркет-мейкер купит/продаст токены по рыночной стоимости.


# Raised Funds Distribution

The further distribution plan is for reference only. Blind Croupier reserves the right to change funds distribution scheme, depending on the amount of funds raised, market situation and other circumstances. Blind Croupier is not obliged to provide accurate information about funds distribution, which, in turn, is supplied without any guarantee and obligations.

* 40% game and platform development
* 30% marketing
* 10% legal expenses
* 20% operating expenses

# Roadmap

This document supplies the general development plan, which is to be updated as the project progresses. All the roadmap content is subject to change at any time. The information is for reference only. Blind Croupier doesn't guarantee the information provided in the Roadmap is accurate, which, in turn, is supplied without any guarantee and obligations.

### Stage 1: Spring-Summer 2017 - Minimal Viable Product (MVP)

This stage was devoted to developing the general software concept for a new generation casino with three main requirements: quick bet placement, transparency, fair random generation, and creating an MVP. The goal was achieved, you can see the algorithms at work in the Videopoker beta version.

### Stage 2: Fall 2017 - Development and Legal

First of all we are going to launch Videopoker to main net and install it to the privilege auction winner. This fall the platform will be developed along with the set of basic games (baccarat, roulette, dice, blackjack). At the same time we will register a company and get a gambling license. We will expand our team to improve the product quality and development speeds. We will start developing the marketing campaign.

### Stage 3: Winter 2017-2018: Testing and Presentation

During Winter 2017, we are going to prepare the platform and the games for the open beta-testing. For the bugs and vulnerabilities found testers are going to get rewards. After that we are going to present the platform and install it along with the games for the 5 winners of the privilege auction. This winter we are going to get a gambling license, after that BlindCroupier casinos will be able to use our merchant account to process Visa/MasterCard payments (and many other popular payment methods), without losing fairness and transparency of Ethereum block chain gambling.

### Stage 4: Spring-Summer 2018: Advanced Platform and Blind Jackpot Fund

Development and testing: The Blind Jackpot Fund, advanced platform, first video slots set, and optimization of all products for the mobile devices. After the testing is finished, we are going to present the ready product at all main online gambling events. The marketing campaign is to be started and the product launched to the main market.

# Background

It all began in [1994](http://www.rightcasino.com/news/history-of-online-casinos/), when Microgaming Company presented the first online gambling platform, allowing to build a full-scale casino. The same year Antigua and Barbuda's government passed  ["Free Trade and Processing Zone"](http://laws.gov.ag/new/detail_page.php?page=content/year.php), describing steps required to obtain an online casino license. This act served as the foundation of the industry's growth. In 1997 there were about 200 online casinos around, compared to 15 in 1996.

A year after, in 1998, the progressive jackpot came in. This innovation implied strong player base growth. Players were attracted by the huge sums of possible wins. This principle still serves as a perfect selling point for gambling lovers all over the world. 

The further development of online gambling was enabled by the risk of a new breed of ambitious developers, rushing into the market with their competitive solutions. The game rules started to become better and the size of the maximum win also increased.

The appearance of the Bitcoin cryptocurrency in 2009 gave birth to a new wave of companies: software vendors which now dominate the market. 

The Bitcoin platforms also gave a boost to casinos using the currency because of the following reasons:

1. anonymity;
2. total balance control;
3. faster transactions and lower running costs; 

But Bitcoin casinos were still unable to solve the main gambling problem: a player can never be sure a casino is playing fair.

# Algorithms and Video Poker Implementation

Let's look at one of the possible Player-Croupier-Bank algorithms, already implemented in the beta version of the Video Poker game from Blind Croupier. Please note that the same idea can be used to develop and implement an algorithm for any possible casino game with 2 or more participants.

Our algorithms are specialized for building casinos for 3 parties: the Player (playing through the client-side JavaScript), the Croupier (an automatic server, belonging to the casino) and the Bank (a Solidity smart-contract, hosted in the Ethereum blockchain). The Player and the Croupier have no mutual trust in each other and trust the Bank unconditionally. The Bank receives the Player's and the Croupier's request, processes them and moves the funds (staking, winning, etc). In case someone (Player or Croupier) tries to cheat or refuses to oblige, the second party turn to the Bank (this is done automatically) and the Bank makes the final judgement and fines the guilty side if necessary.

The client-side JavaScript Player code is open-sourced and open for public inspection. Players may want to modify it, but this would be useless in terms of increasing the chances of winning. This can, on the contrary, degrade his chances. The Bank code is open-sourced as well. Moreover, the Bank acts independently of the Player's or the Croupier's will (and anyone's will at all), because it's a decentralized smart contract. The server-side Croupier code is hidden. **No server-side Croupier code modification can possibly give the Croupier any advantage over the Player**

## Blind Chips

BlindChips - Games in all the connected casinos will be played with special game credits, called BlindChips. These behave mostly like any other standard Ethereum tokens. They are stored in the buyer's Ethereum wallet and can be freely bought or sold. You can buy and sell BlindChips right on the casino's site. The main purpose of BlindChips is faster stake execution. Their main feature is the exchange algorithm. A Player can stake swiftly, by transmitting a signed bet order to the Croupier. **The value of 1 BlindChips is equal to $1 in fees.**

## Video Poker Game Rules

A video poker machine <img align="right" src="https://user-images.githubusercontent.com/30338333/28469012-74600e9a-6e67-11e7-9da0-67be5ffa5a7f.png" width="500"> is usually visually similar to a slot machine. 
On the top there are winning combinations and the payouts table. In the center there is a screen showing the player's hand. On the bottom side there are 3 fields, indicating the player's credit, the last game win and the current bet. By using the "Bet One" button, a player increases the current bet by one coin.

Having placed a bet, the player pushes the "Deal" button and receives five cards from the 52-card deck. By touching a card, the player can put it on hold. After that, the player pushes the "DRAW" button  and the machine changes the free cards for him. In case there is a winning combination, shown in the top table, the appropriate win is deposited to the player's account. The combinations correspond to the standard poker combinations, the lower the chances, the higher the payouts.

| Combination  | LVL1  | LVL2  | LVL3  | LVL4  | LVL5  |
|---|---|:-:|---|:-:|---|
| Flush Royal  | 250  | 500  |  750 |  1000 |  4000 |
| Straight Flush  | 50  | 100 | 150  | 200  |  250 |
| Four of Kind  | 25  | 50  | 75  | 100  |  125 |
|  Full House | 9  |  18 |  27 | 36  | 45  |
|  Flush |  6 |  12 | 18  |  24 | 30  |
|  Straight | 4  | 8  | 12  | 16  | 20  |
| Three Of Kind  | 3  |  6 |  9 | 12  | 15  |
| Two Pairs  |  2 | 4  | 6  |  8 |  10 |
| Jacks or Better  |  1 | 2  |  3 |  4 | 5  |
| **PAYOUTS** | 98,05%  | 98,05%  |  98,05% | 98,05%  |  99,54% |

# Alghoritm Implementation

The Player and the Croupier first generate a key pair of a private and a public key and submit the public key to the Bank. This operation uses 1 blockchain transaction, but must be completed only once. After it is done, all commands issued by any side (Player or Croupier) are signed by the private key of the corresponding side. The signature can then be validated by any party.

First of all, Player submits the signed bet command (the amount of chips they are willing to put at stake, signed by the private key) to Croupier. Croupier validates the command and begins the game.

Four random seeds are used in the algorithm (2 Croupier's and 2 Player's). They are derived from the signature of the fixed data set (a Player's address, a Croupier's address and game id), so only the owner of the private key can know the seed a priori. However, when a seed is published, any party can validate that the seed is generated correctly (using the normal signature validation procedure).

The first two seeds (Player 1 and Croupier 1) are mixed and used to shuffle the deck. After that operation, the first five cards are drawn by Player. 

When the five cards are drawn, Player submits the signed replacement order (the information about cards he is willing to replace, signed by the private key) to Croupier.

Two remaining random seeds (Player 2 and Croupier 2) are then mixed and used to shuffle the remainder of the deck. When this operation is completed, all parties agree on the game result and Croupier submits all the information (4 seeds, bet and replacement commands) to the Bank, which checks all signatures, calculates the game outcome and pays Player his win.

If Croupier fails to submit the information, Player kindly waits for the time required for the transactions to complete and submits the information himself. The result is the same - the Bank calculates the game result and pays Player his win.


# The Problems Solved By the Algorithm

The absence of fairness or transparency checking facilities is the main problem for a casino. A player has to rely on the good will of the casino owners and third party recommendations. He can't possibly check the source code and what is most important, whether a server generates unbiased random data. This is the case because the information is kept private and available only for the casino owners. The closed system is what discourages gamblers from using online casinos.

This is not good for the casino itself. Even if it plays fairly, there is no way to prove this as there is no way to prove the size of the jackpot stated. To solve this, a casino must pay rating agencies, creating an unnecessary dependency on affiliated third parties.

## Pseudo-Random Number Generation (PRNG)
 <img align="CENTER" src="https://user-images.githubusercontent.com/30338333/28472253-71b69640-6e72-11e7-8ae4-a76447229482.png" width="20"> **Problem:** For any online casino the used [PRNG](https://en.wikipedia.org/wiki/Pseudorandom_number_generator/) is of utter importance. The second problem is transparency. A closed system could generated pseudo-randomness (or even predefined randomness) to make advantage of player.

<img align="CENTER" src="https://user-images.githubusercontent.com/30338333/28471826-ffa1e268-6e70-11e7-80b7-27849ac874de.png" width="20"> **Our solution:** In the BlindCroupier's algorithm we use a very simple idea to generate random data. Each side has a private key, used to sign messages and commands. We use it to sign the fixed message, consisting of 4 parts: the Croupier's address, the Player's address, the game ID and the seed ID. The random seed is then acquired from this signature by a very simple manipulation. Until the seed is published it is only known to the owner of the private key. However, after the seed is published, any party can easily verify it by checking the signature against the public key of the seed owner. So, each random seed used in BlindCroupier's algorithm has two major traits:

* *The seed is determined and can't be changed by any side.*
* *The seed is revealed to the owner at the beginning of the game, and is available to public when the owner wishes to publish it.*

After both seeds are published (1 Croupier seed and 1 Player seed), we mix them to get a truly random unbiased seed. All sides use it to independently calculate the game result.

## Gaming Speed and Slow Staking

 <img align="CENTER" src="https://user-images.githubusercontent.com/30338333/28472253-71b69640-6e72-11e7-8ae4-a76447229482.png" width="20"> **Problem:** Most blockhain-based casinos require waiting time for the stake to be accepted (a time of one transaction). Because  smart contract transactions are slow, they require new blocks generation. That's the reason many existing solutions work slowly. This significantly spoils the game process.  

<img align="CENTER" src="https://user-images.githubusercontent.com/30338333/28471826-ffa1e268-6e70-11e7-80b7-27849ac874de.png" width="20"> **Our solution:** We use HTTPS only to exchange the signed commands between Player and Croupier. No Bank transactions are made that can disrupt or slow down the normal gameplay. The Player can place bets, draw and replace cards, finish the game and begin a new game as fast as allowed by their HTTPS connection. The only final transaction is made in the background when the game is finished. It doesn't slow down the gameplay. For staking we use specially designed BlindChips tokens. Their main distinguishing feature is the fact that anyone possessing the private key (initially generated by the player) can own them. So, to begin a game, the Player sends the Croupier the signed command to move some  BlindChips, and the Croupier instantly checks their validity and begins the game. There is no need to wait for the blockchain transaction confirmation. This approach combines the blockchain's absolute reliability and traditional online casino speed.

## Fairness check

 <img align="CENTER" src="https://user-images.githubusercontent.com/30338333/28472253-71b69640-6e72-11e7-8ae4-a76447229482.png" width="20"> **Problem:** There is no way to check the mathematical advantage of a casino because of the closed casino system.

<img align="CENTER" src="https://user-images.githubusercontent.com/30338333/28471826-ffa1e268-6e70-11e7-80b7-27849ac874de.png" width="20"> **Our solution:** All the randomness used in the process is generated from four random seeds. Each of the seeds is random and verifiable. No one can influence the generation of the seeds and anyone can check the seeds have been generated correctly. So, the advantage is truly determined by the game rules which are absolutely transparent.

## Miners' Manipulations

 <img align="CENTER" src="https://user-images.githubusercontent.com/30338333/28472253-71b69640-6e72-11e7-8ae4-a76447229482.png" width="20"> **Problem:** In some blockchain systems, freshly generated block parameters are used to generate randomness. This approach is criticized quite a [lot](https://ethereum.stack.com/questions/191/how-can-i-securely-generate-a-random-number-in-my-smart-contract), because it is vulnerable to some manipulation by the miners. Theoretically speaking, miners could delay the mined blocks until a better block appears, giving them an unfair advantage. It must be noted that all these attack vectors are purely theoretical and high-cost. There is no proof of real attacks taking place.

<img align="CENTER" src="https://user-images.githubusercontent.com/30338333/28471826-ffa1e268-6e70-11e7-80b7-27849ac874de.png" width="20"> **Our solution:** We don't use block parameters as a randomness source. Instead, we mix seeds generated by Croupier and by Player to get totally random seed.

## Third Party Random Sources

 <img align="CENTER" src="https://user-images.githubusercontent.com/30338333/28472253-71b69640-6e72-11e7-8ae4-a76447229482.png" width="20"> **Problem:** A lot of existing solutions use third party randomness vendors (e.g.http://random.org). Taking into account the aforesaid, it's clear that a malicious action by these vendors could lead to an unfair advantage for the Player or the Croupier. Simply put, while generating the required random seed, a site like random.org could easily win the jackpot. 

<img align="CENTER" src="https://user-images.githubusercontent.com/30338333/28471826-ffa1e268-6e70-11e7-80b7-27849ac874de.png" width="20"> **Our solution:** We don't use third party randomness. All our randomness is generated inside the system.

## The Jackpot Validation

 <img align="CENTER" src="https://user-images.githubusercontent.com/30338333/28472253-71b69640-6e72-11e7-8ae4-a76447229482.png" width="20"> **Problem:** There is no way to validate the fact that the published jackpot amount really exists.

<img align="CENTER" src="https://user-images.githubusercontent.com/30338333/28471826-ffa1e268-6e70-11e7-80b7-27849ac874de.png" width="20"> **Our solution:** The Croupier's bankroll is stored in the Bank, which is an Ethereum smart contract. All the funds of a smart contract are public and can be validated by anyone.


# Technologies and Methodologies

In development, we use the latest tech and methodological stack. The main programming languages used in our project are JavaScript (ECMAScript 6) and Solidity 0.4.11. Initially we write all the smart contracts code in specially designed iSolidity language, which is compiled into normal Solidity code. We designed iSolidity and implemented iSolidity to Solidity compiler to solve some major problems of Solidity (like the inability to pass structures and arrays of structures to and from a contract). For smart contract development we use the [Truffle framework](https://truffleframework.com). We are unit-testing with [Mocha](https://mochajs.org) and [Chai](https://chaijs.com). For source code transpiring we use [Babel](https://babeljs.io). We stick to the strict source code style and validity by using [ESLint](eslint.org). We use [solc](https://github.com/ethereum/solidity) for the smart contract compilation. For Player-Croupier API building we use [Swagger](http://swagger.io/) and [Express framework](https://expressjs.com/). We use [Webpack](https://webpack.github.io/) for packaging and optimizing the source code.

* *Methodologies: We use Agile working methodologies. To coordinate our work we use [Pivotal
Tracker](https://pivotaltracker.com), Discord, Slack. To control the source code versions we use [Git](https://git-scm.com/).*
* *Client Side: The client side uses HTML5, CSS3, JavaScript with React / Redux. To preprocess CSS we use [LESS](http://lesscss.org/).*
* *Server Side: The Server Side is implemented in JavaScript with the use of Node.js.*

# iGaming Market

<img align="right" src="https://user-images.githubusercontent.com/30338333/28489539-d48dc560-6ef7-11e7-87f8-f159419e45e9.png" width="470">
Online gaming, or gambling, is the wagering of something of value, usually money, on the outcome of an event or game using the internet. Online gaming includes such activities as poker, casinos (where people can play traditional casino games, like roulette or blackjack, but online), sports betting, bingo and lotteries. Of these, casino games and sports betting make up the largest share of the market. The market volume of online gaming was forecasted to reach 51.96 billion U.S. dollars in 2018, more than doubling since 2009. 

# House Edge or Casino's Revenue

A casino's revenue is formed from the house edge. The house edge is defined as the ratio of the average loss to the initial bet. The house edge is not the ratio of money lost to total money wagered. We will develop games with different house edges. These include games with minimal house advantages requiring skills to play: video poker, the house edge, given a player sticks to the best strategy possible, is 0.46%, for blackjack — 0.28% and the most popular games, in which success depends heavily on a player's luck: For roulette the house edge is 2.7%, for videoslots — 1-10%.

> **For example:** Games like Roulette, the “Edge” is achieved by the casino paying slightly less than the “true” odds for a particular bet. For example, the true odds for a single Roulette number to win are 36 to 1, since there are 37 compartments on the wheel. However, winning bets are actually paid at 35 to 1. Therefore the house advantage is equal to 1/37*100 = 2.7%. In theory after 10 spins, betting 1 unit per spin, the average house profit will be 10 x 1 x 2.76% = 0.27 units. Of course, the casino may not win exactly 0.27 units; this figure is the average casino profit from each player if it had millions of players each betting for 10 spins at 1 unit per spin.


# Blind Croupier Business model

Basically, Blind Croupier uses a standard revenue model, which consists of fixed fees and variable charges. This model minimizes the initial software investment for casino's. We believe that a casino should invest mainly in marketing and bankrolling.

For Blind Croupier this model guarantees monthly revenue flow, motivating us to improve our products and to release new ones. We look forward to providing first-class support and helping our partner casinos — we are interested in their success like no one else! 

## Royalties
The basic charge for the platform and games is 13% of Gross Gaming Revenue (GGR = Stakes - Wins). The royalty payout is performed automatically from the casino's bankroll to the Royalty Fund by the smart contract. The charge for the third party games may be increased.

## Fees

Usage fees are fixed regular payments for platform services, support and server maintenance. The average annual fee is approx. 10,000 $. The basic to advanced platform transition is free of charge. The fee, however, depends on the platform version being used.

## Custom Services

Our partners can use a template platform design or order a unique one. Besides, partners can order unique games, which will be developed exclusively for their project, thus giving them marketing advantages.

## The Marketing Strategy

BlindCroupier, we believe, is going to be a quality brand in the online gambling world. It is important for those casinos working with our software for Blind Croupier to be associated with fine gameplay, fairness and large wins (which is, of course, true). Our strategy is to provide higher conversion rates for those casinos using our solutions. This will increase both our revenues accordingly. We intend to acquire our first clients during the Token Distribution (See our Auction Privileges). First stage will be mainly used for the continuous delivery of our products. We are not going to invest in a marketing campaign while it's still inefficient. However, the marketing campaign will be planned thoroughly and will be started before the release of the final product set. We are going to hire the best specialists for this purpose.

The basic platform and the basic game set are to be presented to the blockchain community. The advanced platform with advanced games are to be presented at the main online gambling exhibitions. During this stage we are going to showcase all the features of our solutions. We will start following a marketing plan as soon as this becomes efficient. 

## Motivation and Mission

To enter a new era of transparent, decentralized casinos one important part is missing — a software vendor. As stated repeatedly in this document, the industry started after the first online casino platform was introduced. Its further growth was closely connected to the development of these platforms. These factors are the main motivation for our team.

Our mission is to deliver all the tools necessary for the industry to shift to new standards of decentralized, unbiased, fair and transparent online gambling. Our task is to free casino owners from ratings agencies services. Casinos, using Blind Croupier's software, are to be associated with indisputable fairness and large wins. This will give a feeling of excitement for players all over the world.

## Premises

Before starting to develop our platform, we looked into building an online casino utilizing a smart contract and BlindCroupier's algorithms. While analyzing, we found out 3 major spending items:

* **Software Development.** This requires focus and large investment. The return period for the investiment spent on software development is quite long, not to mention lots of games and a constant need of developing new ones for the casino to be competitive. A rule of thumb is that there is a separate industry working to deliver software for the casinos. 

* **Player Attraction and Retention.** This is a casino's main task, which includes manipulating a high volume of traffic and competent marketing. To fulfill its main purpose a casino needs major investment. Despite all this, if the software quality doesn't meet market requirements, a marketing campaign is going to be inefficient.

* **Bankroll investment.** Securing players' stakes is required for a casino. It's a direct investment, the more stakes there are, the higher its bankroll must be. At this point we must remind you that BlindCroupier's platform is going to adjust maximum stakes depending on the casino's bankroll.

*As each of these tasks needs large investments, we decided to focus on delivering quality solutions for other professionals, who, in turn, will use their resources to attract players and secure their stakes. Together we can bring new horizons to online gambling.*

# Turnkey Solution For Operators Casino 

Blind Croupier solutions are not for a single casino, but for many casinos working together with the same software. To the casino operators, we guarantee a modern platform, all available games, and the ability to process transactions using our gambling license as soon as possible (everything is already done). We require minimum investment from a casino owners and little effort to launch a project. To begin, they will only need to develop a casino's design and a marketing plan (which is what Blind Croupier would help with) - and that's it, they can serve the clients in their own new generation casino.

# Blind Croupier Platform

The release of the platform is split into two stages. The features and functionality are described in table.

|  Platform features | Basic platform  | Advanced platform  |
|---|---|:-:|
| Analytics  | <img align="CENTER" src="https://user-images.githubusercontent.com/30338333/28471826-ffa1e268-6e70-11e7-80b7-27849ac874de.png" width="25">  | <img align="CENTER" src="https://user-images.githubusercontent.com/30338333/28471826-ffa1e268-6e70-11e7-80b7-27849ac874de.png" width="25">   |
| Cryptocurrencies Exchange  | <img align="CENTER" src="https://user-images.githubusercontent.com/30338333/28471826-ffa1e268-6e70-11e7-80b7-27849ac874de.png" width="25">   | <img align="CENTER" src="https://user-images.githubusercontent.com/30338333/28471826-ffa1e268-6e70-11e7-80b7-27849ac874de.png" width="25">   |
| White Label  | <img align="CENTER" src="https://user-images.githubusercontent.com/30338333/28471826-ffa1e268-6e70-11e7-80b7-27849ac874de.png" width="25">  | <img align="CENTER" src="https://user-images.githubusercontent.com/30338333/28471826-ffa1e268-6e70-11e7-80b7-27849ac874de.png" width="25">   |
| Basic Game  |  <img align="CENTER" src="https://user-images.githubusercontent.com/30338333/28471826-ffa1e268-6e70-11e7-80b7-27849ac874de.png" width="25">   | <img align="CENTER" src="https://user-images.githubusercontent.com/30338333/28471826-ffa1e268-6e70-11e7-80b7-27849ac874de.png" width="25">   |
| Multilingual Support  | <img align="CENTER" src="https://user-images.githubusercontent.com/30338333/28471826-ffa1e268-6e70-11e7-80b7-27849ac874de.png" width="25">   | <img align="CENTER" src="https://user-images.githubusercontent.com/30338333/28471826-ffa1e268-6e70-11e7-80b7-27849ac874de.png" width="25">   |
| Operation under BlindCroupier license   | <img align="CENTER" src="https://user-images.githubusercontent.com/30338333/28471826-ffa1e268-6e70-11e7-80b7-27849ac874de.png" width="25">  |  <img align="CENTER" src="https://user-images.githubusercontent.com/30338333/28471826-ffa1e268-6e70-11e7-80b7-27849ac874de.png" width="25">  |
| Extended Game Set  | <img align="CENTER" src="https://user-images.githubusercontent.com/30338333/28472253-71b69640-6e72-11e7-8ae4-a76447229482.png" width="25">  | <img align="CENTER" src="https://user-images.githubusercontent.com/30338333/28471826-ffa1e268-6e70-11e7-80b7-27849ac874de.png" width="25">   |
| Bonus Program Management  |  <img align="CENTER" src="https://user-images.githubusercontent.com/30338333/28472253-71b69640-6e72-11e7-8ae4-a76447229482.png" width="25"> | <img align="CENTER" src="https://user-images.githubusercontent.com/30338333/28471826-ffa1e268-6e70-11e7-80b7-27849ac874de.png" width="25">   |
| CMS  |  <img align="CENTER" src="https://user-images.githubusercontent.com/30338333/28472253-71b69640-6e72-11e7-8ae4-a76447229482.png" width="25"> |  <img align="CENTER" src="https://user-images.githubusercontent.com/30338333/28471826-ffa1e268-6e70-11e7-80b7-27849ac874de.png" width="25">  |
| BlindJackpot Fund   | <img align="CENTER" src="https://user-images.githubusercontent.com/30338333/28472253-71b69640-6e72-11e7-8ae4-a76447229482.png" width="25">  |  <img align="CENTER" src="https://user-images.githubusercontent.com/30338333/28471826-ffa1e268-6e70-11e7-80b7-27849ac874de.png" width="25">  |
| Jackpot  | <img align="CENTER" src="https://user-images.githubusercontent.com/30338333/28472253-71b69640-6e72-11e7-8ae4-a76447229482.png" width="25">  | <img align="CENTER" src="https://user-images.githubusercontent.com/30338333/28471826-ffa1e268-6e70-11e7-80b7-27849ac874de.png" width="25">   |
| Mobile Casino  | <img align="CENTER" src="https://user-images.githubusercontent.com/30338333/28472253-71b69640-6e72-11e7-8ae4-a76447229482.png" width="25">  | <img align="CENTER" src="https://user-images.githubusercontent.com/30338333/28471826-ffa1e268-6e70-11e7-80b7-27849ac874de.png" width="25">   |


### Description

* **Cryptocurrencies Exchange** To begin playing with a casino, a player needs to connect his existing wallet or create a new Ethereum wallet. This is done online at the casino's site. After doing this, he is then able to buy BlindChips, using many different cryptocurrencies.

* **White Label** is a complete turnkey project of online casino ready for a successful release, requiring only a brand new name and design, selected according to your personal preferences.

* **Analytics.** The platform includes a dashboard, showing detailed revenues, expenses and stakes. There is also a tool to calculate the required bankroll amount and the maximum allowed stake (depending on the bankroll), a revenue prognostic tool and other helpful real-time information displays.

* **Bonus Program**. Set up your bonus program to motivate your players even more. Add free spins and bonus rewards. We are going to develop new bonus types and bonus programs and keep you informed.

* **CMS**. Edit the content, drag and drop game blocks, add special offers, set up SEO.

* **Multilingual**. Localize your casino for any market.

* **JACKPOT**. A progressive jackpot motivates your players to increase the stakes. You can connect your games to a system which certifies the jackpot size and choosing the winner in a fair manner.

*  **Anti-Fraud System.** Our algorithms make Player fraud and Croupier cheating impossible even in theory. All money transfers are controlled by the smart contract, immune to external control.


## Mobile Casino 

Mobile casinos actually represent a brand new craze of online casino industry (Reached €13.5Billions [H2 Gambling Capital report](http://www.igamingbusiness.com/news/igaming-dashboard-june-2017)). Internet expansion in Smartphone helped greatly the world of gambling providing a wide array of online mobile casinos. Online mobile casinos offer the same excitement and thrill like you get in real casino. Besides, some of the reputed mobile casinos. Blind Croupier will, provide gamblers with high quality graphics and most powerful software to offer a realistic gambling experience. With all these advantages, there is no doubt that online mobile casino is here to stay. 


## Operation under BlindCroupier license 

The main reason preventing us from delivering our products at a global level is Ethereum's lack of recognition outside the blockchain community. There needs to be a way to deposit funds more conveniently. To achieve this one must acquire a gambling license. We are going to get one and introduce the sale of BlindChips online by using traditional payment methods: credit cards and payment systems. This has nothing to do with gameplay fairness and transparency. For the casino owners this means there is no need to get a gambling license because all the payments are processed by Blind Croupier.

# The Blind Jackpot Fund 

Any casino, using Blind Croupier software can choose a set of games to connect to the BlindJackpot fund. A percentage of bets placed will be automatically put into it. The percent transferred is 1/5 of the house edge of the specific game.

> **For example:** for the videopoker 5-bet game the casino's expected revenue from each bet is 0.46%, so 1/5 or 0.092% of each bet is transferred to Blind Jackpot Fund.

The chance of winning the jackpot depends on the number of transactions made to the Fund the player has made *(the more transactions made, the larger the Fund's share is and the higher the chance is)*. **Only high-bidders can deposit to the Fund.**


## The Blind Jackpot Fund is divided into three prize funds:

The prize fund is built in a way that money are always accumulated, so the fund doesn't deplete but rather move from cycle to cycle.

* **Mega Jackpot** is the largest one.The winning amount is 13% of the Fund's size. The payout interval is 28 days. After Mega Jackpot payout the rest of the money is moved to the next cycle.
**All the "tickets" are destroyed before the new cycle beginning.** 
	
* **Miracle Jackpot** is the second largest of the regular payouts. It's 4% of the Fund's size. The payout interval is 16 days. The winning "ticket" is excluded from the further payout cycles.

* **Wild Jackpot** is the daily payout of 0.3% of the Fund's size. **Wild Jackpot не разыгрывается по дням когда идут розыгрыши других фондов**

> **E.g.** To make things clear, let's suggest that the prize fund is not replenished by the new bets and its balance during the whole cycle is $1,000. To pay Wild Jackpot, $74 are needed (daily payouts), to pay Miracle Jackpot - $38 (one payout for the current cycle, two payouts during the next cycle), for the Mega Jackpot - $117. So, $771 is moved to the next cycle and so on.

*Blind Croupier reserves the right to make any changes during the system's beta-testing period exclusively to improve its functionality. Changes may include: the distribution of the prize fund, the transferred bet percentage and other changes needed for the quality and fair system operation.*


## BlindJackpot Main Features
* **Cycles:** For the long time players are not excited by the low-chance large-sized jackpots. In the BlindJackpot fund money don't accumulate for ages, instead there are cycles with certain time periods. Everyone knows the moment a new winner is determined. The cycle lasts for 28 days, after that all the "tickets" are destroyed and the rest of the money is moved into the next cycle. Working this way we hope to reach the balance between the jackpot's size and the probability of winning.

* **The teamwork** - the BlindJackpot fund is an excellent opportunity for the competitive casinos to cooperate. Collectively, giving away a small percentage of the revenue they can achieve a really impressive prize fund. The player's chance to win is the same independent of the specific casino he is playing in.

* **Accumulation** - each cycle ends with the announcement of the winner. It lasts 28 days. The major part of the money is then transferred to the next cycle to keep the BlindJackpot Fund growing.

* **Transparency** - the BlindJackpot Fund is controlled by a smart contract. All the transactions, source code, balance, winner determining are transparent and open for the public inspection.

* **Player Motivation and Syndicates creation** - the BlindJackpot Fund is created to motivate player to place larger bets rather than the required size thus increasing the casino's revenue. The main motive for the players are transparency and large win possibility. To drive the motivation even more Blind Croupier is going to promote the creation of syndicates. A syndicate gives a higher winning chance in exchange of a small prize share. They can be formed either by a group of people closely connected to each other (relatives, friends) or in specially created communities.

## Jackpot Winner Determining Algorithm

A winner is determined randomly using a specially designed blockchain-based algorithm. At the moment of writing this document we are inclined to using a [RANDAO](https://github.com/randao/randao) based method. Yet, we leave the possibility to design and implement a totally different fair and transparent system for this purpose.

# Заключение

Программное обеспечение от Blind Croupier разработано на основе проверенных методов криптографии и технологии блокчейн, с использованием наилучших методик и практик, что в совакупности предсталяет собой абсолютно новый ранее недостижимый уровень в интернет-гейминге. Само программное обеспечение является инструментом с помощью которого любой желающий сможет запустить собственное честное, прозрачное, децентрализованное казино нового поколения за несколько кликов. 
