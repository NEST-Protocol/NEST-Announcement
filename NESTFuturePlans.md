# NEST System Future Development

As a decentralized price provider on the chain, NEST has been working hard to realize the dream of a new financial order on the chain. The Core team has never stopped thinking and developing NEST. Up to the current version, NEST is still evolving, rather than becoming perfect all at once, which reflects the complexity and difficulty of innovation in the blockchain industry. Judging from the existing development and downstream ecosystem, NEST is about to launch version 3.5 at present, and the CoFiX project is already using the NEST Oracle prices as a promising downstream project, but our thinking and efforts are far more than that. Here are some new ideas and plans to communicate with the community.

In the next version of NEST, some adjustments are determined. For example, in order to reduce the quotation Gas merges the main currency quotation and the Ntoken quotation; increase the miner quotation to pledge NEST; lower the threshold for opening a new oracle; increase the volatility and average price indicators ( It will be more convenient for DeFi downstream usage), which will be certainly introduced in NEST3.5, but there are some important adjustments that require community participation and support.

### 1. Replace dividends with repurchase based on the market price.

Rationale behind the change: 

1. Compared with repurchase, the dividend model has a free-riding problem: a decentralized system is essentially a game system, and there may be different rounds of game participants, such as the first round of participants through mining The number of NEST obtained is X1, and the contribution of ETH is Y1. Under the repurchase model, X1 can be sold to the system and destroyed (for the time being regardless of long-term holders), because the repurchase amount and mining cost are equivalent , so the total value does not overflow outside the system, but different people get different buyback prices. After the repurchase is completed, the second round of participants will obtain X2 NEST through mining and contributed ETH Y2. If they are still not optimistic, they can sell to the system as in the first round, because the long-term holdings in the first round are not considered, so the amount of repurchase and the cost of mining are still equivalent, that is, Y2 corresponds to X2. But if it is a dividend model, regardless of whether the first round of players hold NEST distribution income, this means that Y2 needs to be allocated to X1+X2, which is not friendly to new players, which is equivalent to a part of the value sent to the previously abandoned participants.

2. Since NEST needs to be deposited in the smart contract to receive dividends, especially version 3.5 is changed to accumulate income based on time, which means that the application of NEST assets in the DeFi field will be affected by the loss of yield, such as mortgage lending will sacrifice NEST Dividend income, resulting in few people willing to use NEST to mortgage ETH, which is very detrimental to the parallel assets mentioned later and the expansion of the use of NEST (including Ntoken).

3. The dividend model has a certain effect on attracting non-community participants (not interested in NEST itself, but interested in dividend income), but it also has some negative effects, such as being easy to be misunderstood as securities, or currency holders chasing income more Rate illusion instead of the intrinsic value of the NEST system, etc., repurchase is equivalent to a decision-making requirement for currency holders: in the absence of dividend income, either choose to sell to the system, or hold for a long time based on intrinsic value.

4. The change in dividends to repurchase has changed greatly. The challenge is whether the NEST oracle quotation system is timely enough, whether the game of miners is effective, whether the secondary market and the repurchase system are consistent, etc. This requires the gradual strengthening and improvement of the entire system. But repurchase will increase the use of oracles, which is also the creation of the most basic demand: internal settlement demand.

### 2. An important application is made around the community requirements of the NEST system: Parallel Assets, which requires the NEST protocol to be compatible with parallel asset quotations.

Rationale behind the change:

1) The core idea of Parallel Assets is to generate a "parallel world" of Ethereum based on the price data of NEST system assets and oracles: any asset has a 1:1 parallel asset with an inherent value for system quotation. For details, see the Parallel Asset white paper. Taking ETH/USDT quoted by miners as an example, miners need to hold these two assets. Once the quotation density is high, or if the order takes place, they need to hold more ETH and USDT, so they must bear the price risk of the two quotation assets. , But if you rely on NEST/nToken to generate two kinds of assets, you only need to pay a certain amount of "interest" without having to bear the overall risk of asset fluctuations. This has been the demand of miners. This demand makes use of both NEST itself and the NEST oracle.

2) Parallel Assets allow NEST to build an ecosystem that takes the NEST system as the starting point and gradually covers the NEST community, NEST related parties, and the DeFi world, and all of this is based on real requirements first, thereby continuously increasing the frequency of usage and value of NEST oracles.

3) Parallel Assets enable holding NEST/nToken asset to hold various assets on ETH (as long as there is a quote), thereby increasing the leverage ratio of the system (previously 1) and increasing the total value of the NEST ecosystem.

4) Parallel Assets put forward higher requirements for NEST quotation and product design, especially the NEST system compatible with parallel asset quotation is a process that needs to be gradually improved, requiring repeated thinking and support from the community.

### 3. The long-term vision of NEST system and future opportunities

The above are the important improvements of the NEST system that require deep community participation and discussion. In addition, the NEST CORE team also proposed future positioning and overall development route for community discussion:

1. NEST is not only positioned as a price oracle, but a generator of native assets on the chain. The NEST system will generate more native assets on chain like NEST and Ntoken (the value capture is entirely on the chain, and the entire process is completely decentralized). Different from secured assets such as USDT, it enriches the types and quantities of assets on the chain, and prepares for true decentralized finance or applications.

2. In version 3.5, NEST will fully launch voting and other decentralized governance models to achieve comprehensive decentralization. All subsequent modifications will strictly implement the voting process.

3. The Core team will continue to propose two new versions for the NEST system: 

* NEST 4.0, which might realize the random choice of miners for quotations, thereby alleviating the current community’s concerns about the concentration of miners.

* NEST 5.0, to solve the problem of insufficient incentives for verifiers, that is, to improve the mandatory and effective price verification. In these two versions, what also needs to be solved is the automatic adaptation of quotation fees, scale and Gas to ensure the stability and the continuity of high quotation density. The above three problems are still under development, and these ideas are not set in stones yet, but the NEST Core team will carry out continuous research and development around these problems.

4. The NEST Core team will propose more brand-new financial designs on the chain as a community participant. The information stream trading, game-theory asset management and equilibrium digital asset currently at the conceptual design level are completely different from traditional financial products and will bring new concepts and ideas to this ever-changing world.

5. The development lifecycle of each version of NEST could take about 1-2 years, through it could progress faster.

## Closing words

Finally, NEST Core once again expresses our belief in the value of blockchain: we firmly believe that a set of completely decentralized native assets, combined with a new financial model, will create an unprecedented order on the chain, completely dominated by algorithms and non-cooperative games. This is a subversive change in the entire history of human value creation and organization structure.


