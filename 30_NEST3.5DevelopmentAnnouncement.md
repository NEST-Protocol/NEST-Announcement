## NEST3.5 Development Announcement

### Current progress

The development of the core code has been completed, and has been deployed on the test network. Everyone is welcome to participate in the test.

Github: https://github.com/NEST-Protocol/NEST-Oracle-V3.5

The audit will be carried out at the end of December, and the audit is expected to be completed in 2 weeks.

### Important updates
#### Quote

Update the NEST quotation mechanism. Quotation mining requires simultaneous quotation of two trading pairs and NEST staking. Any quotation will require two denominated assets to quote the price instead of using a single denominated asset. Currently, one with ETH and another with the Quotation Pool Token.


Namely: ETH/USDT, ETH/NEST or ETH/HBTC, ETH/NHBTC...

> Since other tokens have not released enough quotation vouchers (QP Token) after opening, two quotations cannot be made at the same time. The single quotation interface is still reserved. When the corresponding quotation certificate (QP Token) exceeds 1 million, the interface automatically becomes invalid.

- Quotation needs to be mortgaged NEST, take orders need to mortgage 2 times NEST.
- The maximum block cumulative reward for QP Token quotation mining is 300 blocks.

#### Quotation certificate- QP Token
##### Open QP Token

You can open quotation pairs freely, you need to pay a fee in NEST, and fee goes to DAO。

Cancel auction, cancel 5% auctioneer allocation (the previous QP Token remains unchanged).

##### Quotation document allocation
###### NEST Token

- Guardian Node: 15%
- NEST DAO: 5%
- Quotation Miner: 80%

###### QP Token

- Quotation Miner: 100%

#### Income

You can deposit, withdraw, and receive income anytime.

#### Fund allocation
##### Quotation fee
###### NEST Token
- 20% goes to the NEST DAO
- 80% goes to the revenue pool

###### QP Token

- 20% goes to the QPToken_DAO
- 20% goes to the NEST_DAO
- 60% goes to the the QP Token revenue pool

##### Call fee

All into their respective DAO.

#### Output Data

In addtion to the current price feed, providing the volatility rate, the average price and the real-time price

#### DAO

- Repurchase: Anyone can sell assets to DAO according to the NEST (QP Token) price of the NEST (QP Token) oracle machine.
- Income: All the NEST (QP Token) of the DAO account are deposited into the income contract to receive the income.

