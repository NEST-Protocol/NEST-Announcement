# NEST Protocol 1.0
> Before introducing NEST Protocol 2.0 , we need to understand what is NEST Protocol 1.0? 


> According to the previous definition, NEST is a DeFi ecological protocol developed based on Ethereum . The NEST Protocol 1.0 version mainly includes NEST Token contract, NEST mining pool contract and NEST dividend contract. It releases the NEST Token in the form of [use as-you-go mining] , thereby incentivizing users to participate in the use of NEST DeFi products; all ETH processing fees collected during the use of DeFi products by users will enter the system dividend pool for weekly community dividends , And it is a 100% dividend; the more users hold NEST, the more dividends they receive.
 
 
> Since the launch of the NEST Protocol version 1.0 in December 2018 , DeFi products and services such as decentralized digital asset mortgage lending, auctions, and quizzes have been launched . Among them , the performance of decentralized digital asset mortgage lending products on NEST is particularly outstanding. It uses the "on- chain contract + excess mortgage + no compensation " mechanism to achieve the decentralization of digital asset mortgage lending. As of October 2019 , a total of 32109 orders have been transacted for this mortgage loan product , and the cumulative transaction amount: 663368 ETH + 52517900 TUSD , which has long occupied the top of the daily turnover of Ethereum ecological DeFi products!


> NEST Protocol version 1.0 has been running on the chain safely and stably for nearly a year. Throughout the process, the NestCore development team is constantly optimizing and upgrading it; at the same time, NEST ecological users have also provided a lot of far-reaching feedback. After a year of precipitation and depth exploration technology, in order to better promote the NEST Protocol development, NestCore development team decided to NEST Protocol 2.0 version of the development and upgrading work, and in 2019 Nian 10 Foreign month announced the " NEST Protocol 2.0 development version plan". In NEST Protocol 2.0 version, NestCore team will NEST system time to adjust and optimize, make them more security, scalability, openness, and more to the center.
 
 
> After a period of 4 development week, NEST Protocol 2.0 version is finally here!
 
 
> This review focuses on the NEST Protocol 2.0 . It will describe the specific content of the entire 2.0 version and the profound meaning behind it.
 
 
# NEST-Price of NEST Protocol 2.0
 
 
> NEST-Price is 2.0 NEST Protocol in the most important part, representing NEST core system of values.
 
 
## So, what is NEST-Price ?
 
 
> If it is more popular in the industry, NEST-Price is a decentralized oracle system based on the Ethereum network.If it is described in a more essential language, NEST-Price is a distributed quotation system that implements the synchronization of price facts on the chain in a decentralized manner .
 
 
> NEST-Price defines and implements a new mechanism for generating on-chain facts on the blockchain network. Game theory uses its market, miner offer by way of the chain price at the fact that the market is generated in synchronization chain on , combined with NEST offer mining mechanism, miners excite, making it a logical loop distributed quotation system, Perfectly synchronize the off- chain price facts on the chain to form NEST-Price .
 
 
> The NEST-Price quote system is mainly composed of 4 core parts: a quote generation module, a quote purchase module, a quote fund management module, and an on- chain price generation module. Next, let's take a look at the specific implementation of NEST-Price .
 
 
## Quotation system description
 
 
> The NEST-Price quote system supports direct quotes for ERC20 Token / ETH trading pairs. At the initial stage of the system's launch, only the following two trading pairs are supported:
 
 
> 1.USDT / ETH
 
 
> 2.HT / ETH
 
 
> Quotation miner: Anyone can participate in the quotation and perform NEST mining without threshold.
 
 
## How do miners quote?
 
 
> When a miner makes a quote, he needs to transfer the specific amount of assets corresponding to the quote transaction pair. The minimum unit is 1 ETH. Assuming that the current market price of the USDT / ETH trading pair is 200 USDT = 1 ETH, then the quoted miner needs to transfer both the quoted asset of 200 USDT and 1 ETH to the quoted contract. After the transfer is successful, the quote contract will display the time of 25 blocks (about 5 minutes) in the quote market ; during this period, anyone can redeem according to the miner's quote data; for example, I can Transfer 200 USDT into the quote contract to exchange 1 ETH, and I can also transfer 1 ETH into the quote contract to exchange 200 USDT. This means that if the price of the miner deviates significantly from the real market price, it will provide an arbitrage opportunity for others, and anyone can participate in arbitrage; through this arbitrage penalty mechanism, the miner will be quoted at the market fair price , And then send real and effective price information to the quotation system.
 
 
## What prices will be adopted by the system?
 
 
> If the quotation initiated by the miner is not fully eaten after block 25 , that is, the quotation assets in the quotation are still left, then this quotation data will be used by the quotation system. Conversely, if the arbitrageur completely eats the quotation, its quotation data will be automatically discarded, and it will not participate in the on- chain price formation .
 
 
## What to do if the quote system is maliciously eaten by an attacker ?
 
 
> In any decentralized system, attack costs need to be considered, as is the NEST-Price quote system. To prevent an attacker who by malicious eating single cause of price information that depart from or delay occurs, NEST-Price uses to eat a single double quotation mechanism, which must be issued by eating a single sum of their offer while eating single , and Quote fund double.
 
 
> If the order-taker is a normal order, then his quotation data at the time of the order should be rational and normal ; if the order-taker is a malicious attacker and he wants to achieve his purpose, then his quote data at the time of order should deviate from market data; this time, a larger arbitrage machine will appear on the attacker's malicious quotation will be arbitrageurs in the market quickly digested, this time on the market arbitrageurs will report a rational offer When the order comes out, the price data returns to normal, and the attack fails. If the attacker, rob their own list, then the cost of its future will be higher, the market arbitrage opportunities will be greater, the attacker's own single probability of success will eat less and less, eventually pay The huge loss was eaten by market arbitrageurs and the attack failed. In short, when attackers attack the NEST-Price system, they are playing against the entire market, which is difficult, unimaginable, and the results are self-evident.
 
 
## NEST-Price price generation mechanism
 
 
> In the NEST-Price quotation system, the effective price data that is ultimately used exists in each block of Ethereum. We can generate a custom price P by algorithm according to different DeFi business needs. There are three common types of P, namely : timely price (latest price), average price (average price of n blocks), and weighted average price (custom weight).
 
 
## How does the developer call the price P generated by the NEST-Price quote system ?
 
 
> In the early days, the price P will not open , NEST developers will take the lead in developing a several classic DeFi products , these products are quoted price P, such as decentralized digital asset-backed lending products, decentralized exchange, stable currency Wait. In the process of using these DeFi products for users, they will charge a small ETH processing fee to pay for the price P. This part of the fee income will go directly to the NEST system dividend pool for the weekly NEST Token holders. ETH dividends .
 
 
> So how do third-party developers call the price P, please stay tuned for the NEST Protocol Developer Program. (No specific introduction here)
 
 
# NEST DeFi of NEST Protocol 2.0
 
 
> In chapter two, we have already learned about the NEST-Price system, as well as its operating principle and price generation mechanism. So what's the use of NEST-Price ?
 
 
> The definition of blockchain in the field of economic science : "Blockchain is a machine of trust." The biggest core innovation of blockchain is to solve the trust problem in a decentralized manner, without the need to trust and rely on third-party institutions for value transfer. Among them, smart contracts play an important role. It is a set of contracts defined in digital form, helping contract participants to execute the agreement to complete tasks, saving time and tedious steps. 
 
 
> But in fact, the blockchain cannot actively obtain real-world data. And most of the decentralized products implemented through smart contract technology have a heavy dependence on real-world data, and the DeFi field is particularly urgent. For example, DeFi products and services such as decentralized digital asset mortgages, stablecoins , and insurance all need to introduce real-world price information to complete the logical closed loop of the product itself. However, in the process of invoking market price information, developers have to consider the authenticity, stability, degree of decentralization, and attack costs of value data.
 
 
> In order to solve the problem of lack of decentralized price information, there are also some solutions in the industry: For example, MakerDAO feeds prices through 14 feed miners to form the so-called "decentralized price"; ChainLink provides price data through off-chain reputation nodes , Forming the so-called "decentralized price". No matter what the plan is, everyone has only one purpose, to provide a callable "decentralized price" for DeFi products. At this point, you should also understand that NEST-Price has done the same thing, generating decentralized price data in the way of miner quote mining, providing callable decentralized price information for NEST DeFi products . .
 
 
> Since there are competing products, I have to explain the advantages of NEST-Price :
 
 
> 1 , more of decentralization. NEST-Price synchronizes price information on the chain by means of "miner quote mining" . Everyone can become a quote miner, participate in quotes, and is very decentralized (distributed);
 
 
> 2. The cost of attack is higher. In chapter two, we have described the mechanism of quotation and eating orders. If an attacker wants to deviate from the NEST-Price , the cost of the attack is extremely high ; the more the attack, the higher the cost, the attacker falls into the death spiral;
 
 
> 3 , more real and effective. In the NEST quotation mechanism, every quotation made by the miner must pay real money and bear the high risk cost of evil, and the authenticity is self-evident;
 
 
> 4. Higher stability. NEST-Price 's price data is strictly guaranteed by a set of scientific algorithms . Continuously provide stable and effective price information for DeFi products. There are several types of timely prices, daily average prices, and weighted average prices for DeFi developers to choose freely.
 
 
> the above. We now understand the role of NEST-Price and its industry advantages.
 
 
## So, let's introduce NEST DeFi :
 
 
> We already have the NEST-Price available , and now we make a definition: whenever a DeFi product or service that references NEST-Price price data , we collectively call it NEST DeFi .
 
 
> NEST DeFi is a Wall Street based on the NEST-Price blockchain world. In the NEST DeFi layout, we can see various forms of decentralized mortgage lending products, constant currency, decentralized exchange ( DEX ), decentralized digital asset insurance, and decentralized digital asset "bank". DeFi products and services. As long as you hold digital assets, you can find the DeFi products and services you need in NEST DeFi to meet all your financial needs regarding digital assets.
 
 
> As we all know, it is difficult for ordinary users to interact directly with the blockchain, because not everyone can type code. Therefore, the third-party development team developed a decentralized smart contract interaction tool based on the NEST Protocol -NEST DAPP . In this DAPP , you can easily use NEST DeFi to manage your digital assets.


> Above, this is NEST DeFi , on Wall Street!
 
 
# NEST Economics of NEST Protocol 2.0
 
 
> This chapter mainly describes the economics in the NEST Protocol , including the NEST Token distribution mechanism, value model, and economic model.
 
 
## First, NEST Token Profile
 
 
> NEST ( NEST Token ) is a token issued by the NEST Protocol based on the Ethereum ERC20 protocol , and is the sole equity token of the NEST ecosystem.
 
 
> Total number of NEST Tokens : 10 billion, never issued again!
 
 
> NEST Token release method: quote mining
 
 
> NEST Token contract address: 0x04abeda201850ac0124161f037efd70c74ddc74c
 
 
> NEST Token Block Browser: https://etherscan.io/token/0x04abeda201850ac0124161f037efd70c74ddc74c
 
 
## Second, the NEST Token distribution plan
 
 
> The total number of NEST Tokens is 10 billion. The founding developers have no reservations, no pre- mining , and no pre-sale. 100% of them are released by miners through " quotation mining".
 
 
> The distribution ratio of NEST Token is as follows:
 
 
> Miners 80% , the developer 5% , guardian nodes 15% .
 
 
## Third, NEST Token release mechanism


> The initial year ( 2.4 million blocks) release 10 Yi NEST , divided equally to each block about the release of 400 NEST , a year after the decay of 10% .


> Initial value: Given that NEST has already mined nearly 1.1 billion, according to the above algorithm, this NEST Protocol 2.0 upgrade is in the first attenuation zone. Therefore, since the launch , the initial block is recorded as the 2788888 mining block. Each block has 360 NESTs .


> Miners obtain NEST Tokens through quote mining. Each quote requires an ETH processing fee (1% of the ETH amount at the time of the quote ), and the system-charged fees are all entered into the dividend contract. This means that behind every NEST Token release, miners are paying real money, not free.


> Calculation of NEST mining quantity per miner's quote:


> First, we must first calculate the number of NEST mining rewards M contained in the block of the quoted transaction. If the height difference between the block and the previous block containing the quoted transaction is K, then:


M = K * 360


> Assuming that the block that contains the quote of trading on the types C types , of which a certain kind of transaction type of fee is the sum of E, with the same type of a sum offer to pay the fee is e, then the sum The quoted NEST mining quantity is N :


N = (e / E) * ( M / C)
 
 
## Fourth , NEST Token dividend income
 
 
> First introduce the source of NEST dividend income:
 
 
> Source 1 : quote the fee paid by the miner during the mining process. Mining miners who participate in bidding quotes are required to pay ETH processing fees, and these processing fees will all enter the system dividend pool .
 
 
> Source 2 : Value generated by NEST-Price . When a DeFi product calls NEST-Price , it is necessary to pay a certain percentage of ETH fees to the NEST Protocol , and the specific income is all entered into the system dividend pool .
 
 
> User dividend plan: The NEST dividend contract calculates the corresponding amount of ETH dividends according to the proportion of each user holding the NEST Token . The higher the proportion of NEST holdings, the more the ETH dividend income will be, and the dividend will be paid once a week.
 
 
> Income leveling mechanism: The system will withdraw 10% of ETH assets from the dividend income of each cycle and deposit them in the leveling contract, and the remaining 90% of ETH will be distributed . Stabilization of ETH contract will be saving to prepare for a week of ETH be filled insufficient income . The income leveling mechanism makes the dividend income of NEST investors relatively stable, thereby promoting the stable and sustainable development of NEST ecology . For the judgment criterion of whether to use the ETH funds of the leveling contract, please read the document "NEST income leveling mechanism description" .
 
 
# NEST DAO of NEST Protocol 2.0
 
 
> We all know that no system architecture is flawless from the beginning, even if it is Bitcoin. The NEST Protocol is the same. It also needs to be continuously optimized and upgraded to make it more secure, expandable, open, and more decentralized. In this process, we need an autonomous organization to promote the development of the NEST Protocol . Here we call this organization NEST DAO .
 
 
> NEST DAO is essentially an on-chain governance system, which mainly consists of two major modules, namely the NEST voting system and the NEST guardian node NestNode .
 
 
> I. Introduction to the NEST voting system
 
 
> First of all: Any wallet address holding a NEST Token has an inherent voting right to participate in NEST voting.
 
 
> The voting system itself is also a contract system. Each vote requires the voting initiator to deploy a voting contract. At the same time, the contract needs to open source code and explain the voting content. In order to encourage NEST holders to vote, vote the contract deployer can turn to vote in a certain number of contracts NEST , in order to motivate people to vote; if the vote goes through, this NEST will be destroyed; if the vote did not pass, the deployer NEST can be retrieved from the contract .
 
 
> After reading the contract code and voting content, NEST Token holders can make their own judgments and decide whether to participate in voting (participation in voting is deemed to be supported, and non-participation is considered not to support). When the number of NESTs participating in the voting exceeds 51 % of the NEST circulation , it is deemed to have passed the voting. At this time, anyone can trigger the voting contract and execute the voting content in the contract.
 
 
> Second, the introduction of the Guardian Node NestNode
 
 
> Guardian nodes are what we usually call "super nodes". The Guardian Node NestNode is an important part of the NEST ecosystem. It provides various resources and funds for the development of the NEST Protocol , and is the core source of power for the early development of NEST . There will be rewards for paying. In the process of NEST development, NestNode also enjoys some of the benefits and influence brought by the NEST ecosystem, which are mainly reflected in the following two points:
 
 
> 1 , NEST Token usufruct: in NEST Token release distribution mechanism, the miners accounted for 80% , developers accounted for 5% , guardian node accounted for 15% ; can be simply understood as: Quote miners in the mining process, NEST contract mining pool every release 100 Mei NEST Token , of which 15 Mei assigned to the guardian node NestNode .
 
 
> 2 , NEST voting rights: NestNode holders have NEST system of voting rights, rights more important than NEST 'Importance higher weight ratio between the two will follow right proportion NEST liquidity adjusted .
 
 
> In order to better reflect the NEST to the center of the features of the system, the node guardian NestNode been Token of. NestNode is also a Token issued based on the Ethereum ERC20 protocol , with a total of 1500 tokens . Tokenized guardian nodes can freely transfer and trade.
 
 
> Whether it is who owns NestNode , he will actively promote NEST Protocol development, actively participate NEST ecological construction, because he himself also is NEST decentralized project core beneficiary .
 
 
> The above is the introduction of NEST DAO .
 
 
# NEST Community of NEST Protocol 2.0
 
 
> The NEST community mainly introduces the current community composition of the NEST ecosystem and the specific situation of the fan community and partners around the NEST Protocol .
 
 
## 1 , NEST ecosystem group consisting of
 
 
> NestCore developer group: develop and maintain the NEST Protocol ;
 
 
> NEST DAPP developer team: develop and maintain NEST DAPP ;
 
 
> DeFi product developer group: a developer team corresponding to various DeFi products;
 
 
> NEST-Price quote miners: Miners participating in NEST-Price quotes;
 
 
> NEST-Price arbitrage miners: professional arbitrage institutions and quantitative institutions;
 
 
> NEST DeFi user group: DeFi users;
 
 
> NEST Token investors: NEST Token holders, NEST consensus maintainers and promoters;
 
 
> NestNode Guardian Node: NEST consensus maintainer and promoter;
 
 
## 2 , NEST enthusiast community building
 
Fire letter autonomous community: 120,000 people
Telegram exchange community: 50,000 people
 
## 3 , NEST Protocol partners
 
 
> NEST DAPP Development Team : The NEST DAPP team is a professional development team from overseas that focuses on blockchain product development and interactive research and development. They developed the NEST DAPP smart contract front-end interaction tool based on the NEST Protocol .
 
 
> Square Foundation Ethernet : Ethernet Square Foundation is a registered Swiss non-profit organization, designed to manage Ethernet currency sales in the financing of the fund, in order to better serve the Ethernet Technology Square and to the center of ecosystem services. The NEST Protocol is a decentralized protocol developed based on the Ethereum network.NestCore maintains close communication and cooperation with the Ethereum Foundation to jointly promote the development of the Ethereum ecosystem.
 
 
> Know Chuangyu : Beijing knows that Chuangyu is the most influential security company in China, providing anti- DDoS attacks, anti-black and intrusion prevention, smart contract auditing, computing power security monitoring, public chain auditing, penetration testing, etc. for the blockchain industry. The security solution has been highly recognized by the Ministry of Public Security, Supreme Law, General Administration of Industry and Commerce, China Merchants Bank, CITIC Securities, Tencent, JD.com, Bitmain and other government departments and leading global technology companies.
 
 
> An laboratories : Ann ratio (SECBIT) laboratory block chain industry in China the most representative block chain security company , focused on research contracts and trusted intelligent protocol security consensus. The contract security and formal verification of the NEST Protocol is provided by Abe Laboratories.
 
 
> DVP vulnerability platform : DVP is a decentralized vulnerability platform. DVP implements responsible disclosure of vulnerabilities in an all-round and multi-dimensional manner through a self-organized organization of the security community. At the same time, it serves as a core link between white hats and manufacturers, and builds an efficient and transparent security information platform for users of blockchain vendors. N estCore and DVP cooperation jointly initiated NEST Protocol vulnerability reward program, as NEST escort development.
 
 
> Hash think tank : Hash think tank is China's leading digital economy industry think tank type platform, which is jointly contributed by Huawen Media and Times Media. Committed to promoting the effective integration of "digital economy + real economy". Deeply cultivated in representative fields of digital economy such as artificial intelligence, big data, and blockchain. The marketing and media cooperation of the NEST Protocol are provided by the Think Tank.
 
 
> HuobiClub : Based on Huobi Group's own brand resources and ecological advantages, Hu obi Club is committed to creating a professional offline blockchain industry communication and service platform, bringing together global site resources in the blockchain industry, and attracting high-quality teams for it. Carry out a full range of blockchain deep value-added services, integrate the local resources of the site to form a closed loop of the industrial chain, help partners grow, and help the industry develop. NEST Protocol and HuobiClub establish deep partnerships that promote NEST Protocol played a key role in the exchange of dialogue with the block chain industry.
 
 
> NestFans : NestFans is a co-sponsored the formation of the early miners and enthusiasts by the NEST user autonomous community forum , designed to block the chain industry, users and practitioners offer a exchange learning NEST Protocol of channels, better promote the NEST ecological development and community Consensus building.
 
 
# The Summary Of NEST Protocol 
 
 
> The NEST-Price in the NEST Protocol is a major innovation and breakthrough in the blockchain industry.It synchronizes the off-chain price facts on the chain in a highly decentralized manner , forming true and effective price data on the chain. . NEST-Price is settled application block chain technology provides the most important of infrastructure , promoting the development of the whole industry has played a huge role!
 
 
## Summary about de facto chains :
 
 
> 1. In fact, the essence of the chain is not to " upload " fact information to the chain, but to form (generate) facts on the chain;
 
 
> 2 , regardless of the fact that the center of uploading information, or go to the center of the way uploaded, means that the fact that the first produced under the chain on the chain. For a real oracle system , the off-chain facts should be synchronized on the chain;
 
 
> 3.NEST-Price is unique in that it forms a price fact directly on the chain, while other oracle systems simply upload a price fact to the chain, which is an essential difference.
 
 
> So, what is the NEST Protocol?NEST Protocol is a decentralized network of price fact prediction machines .

---

# NEST Protocol 1.0

## 在介绍 NEST Protocol 2.0 之前，我们需要了解一下 NEST Protocol 1.0 是什么？

> 根据此前的定义，NEST 是一个基于以太坊开发的 DeFi 生态协议。NEST Protocol 1.0 版本主要包含 NEST Token 合约、NEST 矿池合约 和 NEST 分红合约。其采用【使用即挖矿】的方式释放 NEST Token，进而激励用户参与 NEST DeFi 产品的使用；在用户使用 DeFi 产品过程中收取的 ETH 手续费会全部进入系统分红池，用于每周的社区分红，而且是 100% 分红；用户持有 NEST 的占比越多，分红收益越多。

> NEST Protocol 1.0 版本自 2018 年 12 月份上线以来，陆续上线了去中心化数字资产抵押借贷、拍卖、竞猜等 DeFi 产品和服务。其中 NEST 上的去中心化数字资产抵押借贷产品表现尤为突出，其采用“ 链上合约+超额抵押+无需补偿 ”的机制，实现了数字资产抵押借贷的去中心化。截止到 2019 年 10 月，该抵押借贷产品累计成交了 32109 单，累计成交金额：663368 ETH +52517900 TUSD，长期霸占以太坊生态 DeFi 类产品日成交额榜首！ 

> NEST Protocol 1.0 版本已经在链上安全、稳定运行了近一年之久。在整个过程中，NestCore 开发团队也在不断对其进行优化和升级；同时，NEST 生态用户也对其提出了很多具有深远价值的反馈。经过一年的技术沉淀与深度探索，为了更好的促进 NEST Protocol 的发展，NestCore 开发团队决定进行 NEST Protocol 2.0 版本的开发和升级工作，并在 2019 年 10 月份对外公布了《NEST Protocol 2.0 版本开发计划》。在 NEST Protocol 2.0 版本中，NestCore 团队将对 NEST 系统进行一次调整和优化，使其更加具有安全性、拓展性、开放性，同时更加的去中心化。

> 经过为期 4 周的开发，NEST Protocol 2.0 版本终于要来了！本篇综述主要围绕 NEST Protocol 2.0 展开，将详细的描述整个 2.0 版本的具体内容及其背后所代表的深刻意义。


# NEST Protocol 2.0 之 NEST-Price

> NEST-Price 是 NEST Protocol 2.0 中最重要的部分，代表着 NEST 系统的核心价值。

## 那么，NEST-Price 是什么？

> 如果用行业内比较通俗的话来说，NEST-Price 是基于以太坊网络构建的一个去中心化的预言机系统。如果用比较本质的语言来描述，NEST-Price 是一个以去中心化的方式实现了价格事实同步上链的分布式报价系统。

> NEST-Price 定义并实现了一种全新的在区块链网络上生成链上事实的机制。其采用市场博弈理论，通过矿工报价的方式将链下市场的价格事实同步产生于链上，并结合 NEST 报价挖矿机制，对矿工进行激励，使其成为一套逻辑闭环的分布式报价系统，完美的将链下价格事实同步在链上生成出来，形成 NEST-Price。

> NEST-Price 报价系统主要由报价生成模块、报价单买入模块、报价资金管理模块、链上价格生成模块 4 个核心部分构成。接下来，我们来看一下，NEST-Price 的具体实现方式。

## 报价系统说明

> NEST-Price 报价系统支持 ERC20 Token / ETH 交易对的直接报价，在系统上线初期，仅支持以下两个交易对：

> 1.USDT / ETH
> 2.HT / ETH

> 报价矿工：任何人都可以参与报价，进行 NEST 挖矿，无门槛限制。

## 矿工如何报价？

> 矿工在进行报价时，需要转入报价交易对所对应的具体数额的资产，最小单位为 1 ETH。假设当前 USDT / ETH 交易对的市场价格是 200 USDT = 1 ETH，那么报价矿工需要往报价合约单中同时转入 200 USDT 和 1 ETH 的报价资产。转入成功之后，该报价合约单会在报价市场中显示 25 个区块的时间（大约 5 分钟）；在这一段时间内，任何人都可以按照该矿工的报价数据进行兑换；比如，我可以往报价合约中转入 200 USDT 兑换出 1 ETH，我也可以往报价合约中转入 1 ETH 兑换出 200 USDT。这就意味着，如果矿工的报价与市场真实价格偏离较大，那么就给他人提供了一个套利机会，任何人都可以参与套利；通过这种套利惩罚机制促使报价矿工都会按照市场公允价格进行报价，进而向报价系统输送真正有效的价格信息。

## 哪些价格会被系统采用？

> 如果矿工发起的报价单在 25 区块后没有被人完全吃单，即报价单内的报价资产仍有剩余，那么这一单报价数据将会被报价系统采用。反之，被套利者完全吃掉的报价单，其报价数据将自动舍去，不参与链上价格形成。

## 报价系统被攻击者恶意吃单怎么办？

> 任何一个去中心化的系统，都需要考虑攻击成本，NEST-Price 报价系统亦是如此。为了防止攻击者通过恶意吃单的方式致使价格信息发生偏离或延时，NEST-Price 采用了吃单双倍报价机制，即吃单者在吃单的同时必须要发出一笔自己的报价，且报价资金 double。

> 如果吃单者是正常吃单，那么他在吃单时的报价数据应该是理性且正常的；如果吃单者是恶意攻击者，他要达到自己的目的，那么他在吃单时的报价数据应该是偏离市场数据的；此时，一个放大的套利机会就出现了，攻击者的恶意报价单会被市场上的套利者迅速消化掉，此时市场上的套利者会报出理性的报价单出来，进而价格数据回归正常，攻击失败。如果攻击者，自己抢吃自己的单子，那么其往后的成本将越来越高，市场套利机会也将越来越大，攻击者自己吃单成功的概率将越来越小，最终会付出巨大的损失被市场套利者吃掉，攻击失败。简而言之，攻击者在攻击 NEST-Price 系统的时候，就是其在与整个市场进行博弈，难度之大，不可想象，结果不言而喻。

## NEST-Price 价格生成机制

> 在 NEST-Price 报价系统中，最终被采用的有效价格数据存在于以太坊各个区块中，我们可以按照不同的 DeFi 业务需求通过算法生成自定义价格 P。常见的 P 有三种，分别是：及时价格（最新价格），平均价格（n个区块的平均价格），加权平均价格（自定义权重）。

## 开发者如何调用 NEST-Price 报价系统生成的价格 P ？

> 在初期，价格 P 不会对外开放，NEST 开发者会率先开发出几款经典的 DeFi 产品，在这些产品中引用价格 P，比如去中心化数字资产抵押借贷产品、去中心化交易所、稳定币等。这些 DeFi 产品在面向用户使用的过程中，会收取少许的 ETH 手续费，用于对价格 P 的付费，这部分手续费收入会直接进入 NEST 系统分红池，用于 NEST Token 持有者每周的 ETH 分红。

## 那么，第三方开发者如何调用价格 P，请持续关注 NEST Protocol 开发者计划。（这里不做具体的介绍）


# NEST Protocol 2.0 之 NEST DeFi

> 在章节二中，我们已经了解了 NEST-Price 系统，以及其运行原理和 Price 生成机制。那么 NEST-Price 究竟有什么用呢？

> 经济科学领域对区块链的定义：「区块链是信任的机器」。 区块链最大的核心创新在于去中心化的解决信任问题，不需要再去信任和依靠第三方机构的情况下进行价值转移。其中，智能合约起到了重要的作用。它是一套数字形式定义的合约，帮助合约参与方执行完成任务的协议，节省了时间和繁琐的步骤。

> 但事实上，区块链无法主动获取现实世界的数据。而且大多数通过智能合约技术实现的去中心化产品又存在着对现实世界数据的严重依赖，其中 DeFi 领域尤为迫切。比如去中心化数字资产抵押借贷、稳定币、保险等 DeFi 产品和服务，都需要引入真实世界的价格信息，来完成产品自身的逻辑闭环。但在调用市场价格信息的过程中，开发者又不得不去考虑价值数据的真实性、稳定性、去中心化程度、攻击成本等。

> 为了解决去中心化价格信息缺失的问题，行业内也有了一些解决方案：比如 MakerDAO 通过 14 名喂价矿工进行喂价形成所谓的“去中心化价格”；ChainLink 通过链下信誉节点来提供价格数据，形成所谓的“去中心化价格”。无论方案怎么样，大家的目的都只有一个，为 DeFi 产品提供一个可调用的「去中心化价格」。到这里，你应该也明白了，NEST-Price 也做了同样的一件事，以矿工报价挖矿的方式生成了去中心化的价格数据，为 NEST DeFi 产品提供可调用的去中心化价格信息。

> 既然有竞品，那就不得不去说明一下 NEST-Price 的优势：

1、更加的去中心化。NEST-Price 通过「矿工报价挖矿」的方式，同步在链上生成价格信息。人人都可以成为报价矿工，参与报价，非常的去中心化（分布式）;

2、攻击成本更高。在章节二中，我们已经描述了报价吃单的机制，攻击者要想使 NEST-Price 发生偏离，其攻击成本是极其高昂的； 越攻击，成本越高，攻击者陷入死亡螺旋；

3、更加的真实有效。NEST 报价机制中，报价矿工的每一次报价，都要付出真金白银，并且承担作恶的高风险成本，真实性不言而喻；

4、稳定性更高。NEST-Price 的价格数据采用有一套科学的算法严格保证。为 DeFi 产品持续不断的提供稳定有效的价格信息，主要有及时价格、日均价、加权均价等几种类型，供 DeFi 开发者们自由选择。

以上。我们现在已经明白了 NEST-Price 的作用以及行业优势。

## 那么，接下来我们来介绍一下 NEST DeFi：

> 我们已经有了可用的 NEST-Price，现在我们做一个定义：但凡引用 NEST-Price 价格数据的 DeFi 产品或服务，我们统称之为 NEST DeFi。

> NEST DeFi 就是一个基于 NEST-Price 的区块链世界的华尔街。在 NEST DeFi 版图中，我们可以看到去中心化的抵押借贷产品，恒定币，去中心化交易所（DEX），去中心化数字资产保险，去中心化数字资产“银行”等形式各样的 DeFi 产品和服务。只要你持有数字资产，都可以在 NEST DeFi 中找到你所需要的 DeFi 产品和服务，满足你所有的有关数字资产的金融需求。

> 众所周知，普通用户很难与区块链直接进行交互，因为并不是所有人都能敲代码。所以，第三方开发团队基于 NEST Protocol 开发了一款去中心化的智能合约交互工具 -- NEST DAPP。在这款 DAPP 中，你可以轻松的使用 NEST DeFi，管理自己的数字资产。

> 以上，这就是 NEST DeFi，链上华尔街！


# NEST Protocol 2.0 之 NEST Economics

> 这一章主要讲述一下 NEST Protocol 中的经济学，主要包括 NEST Token 分发机制、价值模型、经济模型等。

## 一、NEST Token 简介

NEST（NEST Token）是由 NEST Protocol 基于以太坊 ERC20 协议发行的 Token，是 NEST 生态系统的唯一权益通证。

NEST Token 总量：100 亿枚，永不增发！

NEST Token 释放方式：报价挖矿

NEST Token 合约地址：0x04abeda201850ac0124161f037efd70c74ddc74c

NEST Token 区块浏览器：https://etherscan.io/token/0x04abeda201850ac0124161f037efd70c74ddc74c

## 二、NEST Token 分配方案

NEST Token 总量 100 亿枚，创始开发者无预留、无预挖、无预售，100% 通过矿工「报价挖矿」的方式进行释放。

NEST Token 分配比例如下：

矿工 80%，开发者 5%，守护者节点 15%。

## 三、NEST Token 释放机制
初始每年（2400000 区块）释放 10 亿 NEST，平分到每个区块约释放 400 NEST，以后每年衰减 10% 。
初始值：鉴于目前 NEST 已经挖出近 11 亿，根据上面的算法，本次 NEST Protocol 2.0 升级后，处于第一次衰减区间内，因此自上线开始，初始区块记为 2788888 号挖矿区块，每个区块出矿 360 枚 NEST。
矿工通过报价挖矿的方式获取 NEST Token，每次报价需要付出 ETH 手续费（报价时 ETH 数量的 1%），系统收取的手续费全部进入分红合约中。这就意味着每一枚 NEST Token 释放的背后都有矿工在付出真金白银，并不是免费获取。
矿工每一笔报价的 NEST 挖矿数量计算：
首先，要先计算出打包报价交易的区块中包含的 NEST 挖矿奖励数量 M，如果该区块距离上一个含有报价交易的区块的高度差是 K，那么： 
M = K * 360
假设该区块中所包含的报价交易对类型有 C 种，其中某一种交易对类型的手续费之和是 E，与之同类型的某一笔报价付出的手续费是 e，那么该笔报价的 NEST 挖矿数量为 N：
N = （e / E）* (M / C)

## 四、NEST Token 分红收益

先介绍一下 NEST 分红收益来源：

来源1：报价矿工挖矿过程中付出的手续费。报价矿工参与报价矿工是要付出 ETH 手续费的，这些手续费会全部进入系统分红池。

来源2：NEST-Price 所产生的价值。当有 DeFi 产品调用 NEST-Price 时，需要向 NEST Protocol 支付一定比例的 ETH 费用，该比收入全部进入系统分红池。

用户分红方案：NEST 分红合约根据每位用户持有 NEST Token 的占比来计算与之对应的 ETH 分红数量，持有 NEST 占比越高，ETH 分红收益越多，每周分红一次。 

收益平准机制：系统会从每一周期的分红收益中抽出 10% 的 ETH 资产存入平准合约中，余下的 90% ETH 进行分红。平准合约中的 ETH 会进行储蓄，以备某一周期 ETH 收益不足时进行补齐。收益平准机制使得 NEST 投资者分红收益相对稳定，进而促进 NEST 生态稳定可持续发展。有关是否使用平准合约的 ETH 资金的判断标准可阅读文档《NEST收益平准机制说明》。


# NEST Protocol 2.0 之 NEST DAO

> 我们都知道，没有一个系统架构从一开始就是完美无瑕的，哪怕他是比特币。NEST Protocol 也一样，也需要不断的优化、升级，使其更加具有安全性、拓展性、开放性以及更加的去中心化。在此过程中，我们需要一个自治组织去推动 NEST Protocol 的发展，在这里我们称该组织为 NEST DAO 。

> NEST DAO 本质来说是一个链上治理系统，其主要有两大模块组成，分别是 NEST 投票系统和 NEST 守护者节点 NestNode。

## 一、NEST 投票系统介绍

首先说明：任何持有 NEST Token 的钱包地址都拥有与生俱来的投票权，参与 NEST 投票。

投票系统本身也是一个合约系统，每一次投票都需要投票发起者部署一张投票合约，同时该合约需要进行代码开源以及投票内容的解释说明。为了激励 NEST 持有人参与投票，投票合约部署者可以往投票合约中转入一定数量的 NEST，以此来激励大家投票；如果投票通过，这笔 NEST 会被销毁；如果投票没有通过，部署者可取回合约中的 NEST。

NEST Token 持有人在阅读合约代码和投票内容之后，可自行做出判断，决定是否参与投票（参与投票视为支持，不参与视为不支持）。当参与投票的 NEST 数量超过 NEST 流通量 51% 以上，视为投票通过，此时任何人都可以触发该投票合约，执行合约中的投票内容。

## 二、守护者节点 NestNode 介绍

守护者节点即为我们通常所说的“超级节点”。守护者节点 NestNode 是 NEST 生态系统的重要组成部分，它为 NEST Protocol 的研发提供了所需的各种资源和资金，是早期推动 NEST 发展的核心源动力。有付出就会有回报，在 NEST 发展过程中，NestNode 也享受着 NEST 生态所带来的一些收益和影响力，主要体现为以下两点：

1、NEST Token 收益权：在 NEST Token 释放分配机制中，矿工占比 80%，开发者占比 5%，守护者节点占比 15%；可以简单理解为：报价矿工在挖矿过程中，NEST 矿池合约每释放 100 枚 NEST Token，其中有 15 枚分配给了守护者节点 NestNode。

2、NEST 投票权：NestNode 持有人拥有 NEST 系统的投票权，权重要比 NEST 权重要高一些，两者的权重比例会跟随 NEST 流通量的占比进行调节。

为了更好的体现 NEST 系统的去中心化特征，守护者节点 NestNode 已经 Token 化。NestNode 也是一种基于以太坊 ERC20 协议发行的 Token，总量恒定为 1500 个。Token 化的守护者节点可以自由的进行转让、交易。

无论是谁拥有 NestNode，他都会积极的推动 NEST Protocol 的发展，主动参与 NEST 生态建设，因为他本身也是 NEST 去中心化项目的核心受益者。

以上，是有关 NEST DAO 的介绍。


# NEST Protocol 2.0 之 NEST Community

有关 NEST 社区主要介绍一下 NEST 生态系统当前的群体组成，以及围绕着 NEST Protocol 相关的爱好者社群和合作伙伴的具体情况。

## 1、NEST 生态系统群体组成

NestCore 开发者小组：对 NEST Protocol 进行开发和维护；

NEST DAPP 开发者团队：对 NEST DAPP 进行开发和维护；

DeFi 产品开发者群体：各种 DeFi 产品所对应的开发者团队；

NEST-Price 报价矿工：参与 NEST-Price 报价的矿工；

NEST-Price 套利矿工：专业的套利机构和量化机构；

NEST DeFi 用户群体：DeFi 用户；

NEST Token 投资者：NEST Token 持有人，NEST 共识维护者和推动者；

NestNode 守护者节点：NEST 共识积极维护者和推动者；

## 2、NEST 爱好者社群建设

火信自治社群：12万人
电报交流社群：5万人

## 3、NEST Protocol 合作伙伴

> NEST DAPP 开发团队：NEST DAPP 团队是一个来自海外的专注于区块链产品开发与交互研发的专业开发团队。他们基于 NEST Protocol 开发了 NEST DAPP 智能合约前端交互工具。

> 以太坊基金会：以太坊基金会是一个注册在瑞士的非营利性机构，旨在管理以太币销售中所筹措的基金，以更好地为以太坊和去中心化技术生态系统服务。NEST Protocol 是一个基于以太坊网络开发的去中心化协议，NestCore 与以太坊基金会保持密切沟通协作，共同推动以太坊生态发展建设。

> 知道创宇：北京知道创宇是中国最具影响力的安全公司，为区块链行业提供抗DDoS攻击、防黑防入侵，智能合约审计，算力安全监控，公链审计、渗透测试等整体安全解决方案，得到了公安部、最高法、工商总局、招商银行、中信证券、腾讯、京东、比特大陆等众多政府部门和全球领先的科技企业的高度认可。

> 安比实验室：安比(SECBIT)实验室是中国区块链行业最具代表性的区块链安全公司，专注于可信智能合约与安全共识协议研究。NEST Protocol 的合约安全和形式化验证工作由安比实验室提供。

> DVP漏洞平台：DVP 是一个去中心化的漏洞平台。DVP 通过安全社区自治的组织方式，全方位多维度贯彻执行漏洞的负责任披露，同时作为白帽子与厂商的核心纽带，为区块链厂商用户搭建高效、透明的安全信息平台。NestCore 与 DVP 合作共同发起 NEST Protocol 漏洞赏金计划，为 NEST 发展保驾护航。

> 算力智库：算力智库是中国领先的数字经济产业智库型平台，由华闻传媒、时报传媒联袂巨献。致力于推动 “数字经济+实体经济”的有效融合。深耕于人工智能、大数据、区块链等数字经济代表领域。NEST Protocol 的市场推广、媒体合作等工作由算力智库提供。

> HuobiClub：Huobi Club 立足于火币集团本身的品牌资源及生态优势，致力于打造专业的线下区块链行业交流和服务平台的方式，汇聚区块链行业全球站点资源，吸纳优质团队为其进行全方位的区块链深度增值服务，整合站点当地资源形成产业链闭环，帮助合作伙伴成长，助力行业发展。NEST Protocol 与 HuobiClub 建立有深度的合作关系，其为推动 NEST Protocol 与区块链行业的交流对话起到了关键作用。

> NestFans：NestFans 是一个由 NEST 早期矿工和用户共同发起组建的爱好者自治社区论坛，旨在为区块链行业用户和从业者提供一个交流学习 NEST Protocol 的渠道，更好的推动 NEST 生态发展和社区共识建设。

# NEST Protocol 【总结】

> NEST Protocol 中的 NEST-Price 是区块链行业内的重大创新和突破，它以一种高度去中心化的方式把链下价格事实进行了同步上链，在链上形成了真实有效的价格数据。NEST-Price 为区块链技术的落定应用提供了最为重要的基础设施，对推动整个行业的发展起到了巨大作用！

关于事实上链的总结：

1、事实上链的本质不是往链上“上传”事实信息，而是要在链上形成（生成）事实；

2、不管是中心化的上传事实信息，还是以去中心化的方式上传，都意味着链下事实先于链上产生。而真正的预言机系统，应该要做到链下事实同步产生于链上；

3、NEST-Price 的独特之处是直接在链上形成一个价格事实，而其他预言机系统则只是往链上传了一个价格事实，这是本质差异。

那么，NEST Protocol 是什么？
NEST Protocol 是一个去中心化的价格事实预言机协议网络。

