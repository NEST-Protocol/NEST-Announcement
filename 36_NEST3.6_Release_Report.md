# NEST 3.6 released on Ethereum mainnet

Upgrade time: Apr-27-2021 09:00 AM +UTC

github: https://github.com/NEST-Protocol/NEST-Oracle-V3.6

## Contract Addresses

### 2021-04-27@mainnet
| Name | Interfaces | mainnet |
| ---- | ---- | ---- |
| nest | IERC20 | 0x04abEdA201850aC0124161F037Efd70c74ddC74C |
| nn | IERC20 | 0xC028E81e11F374f7c1A3bE6b8D2a815fa3E96E6e |
| nestGovernance | INestGovernance | 0xA2eFe217eD1E56C743aeEe1257914104Cf523cf5 |
| nestLedger | INestLedger | 0x34B931C7e5Dc45dDc9098A1f588A0EA0dA45025D |
| nestMining | INestMining, INestQuery | 0x03dF236EaCfCEf4457Ff7d6B88E8f00823014bcd |
| ntokenMining | INestMining, INestQuery | 0xC2058Dd4D55Ae1F3e1b0744Bdb69386c9fD902CA |
| nestPriceFacade | INestPriceFacade, INestQuery | 0xB5D2890c061c321A5B6A4a4254bb1522425BAF0A |
| nestRedeeming | INestRedeeming | 0xF48D58649dDb13E6e29e03059Ea518741169ceC8 |
| nestVote | INestVote | 0xDa52f53a5bE4cb876DE79DcfF16F34B95e2D38e9 |
| nnIncome | INNIncome | 0x95557DE67444B556FE6ff8D7939316DA0Aa340B2 |
| nTokenController | INTokenController | 0xc4f1690eCe0145ed544f0aee0E2Fa886DFD66B62 |

# NEST Protocol v3.6 will continue the repurchase model of v3.5 on the basis of the following functionally：

1. Add a voting governance module which will remove system maintenance accounts by voting after v3.6 launches. Decentralize developer rights to the community and require 51% votes for any changes of the protocol.

2. Completely elimination of dividends with all income used for repurchase.

3. Quotation scale adjustment: NEST Token dual-track quotation scale 30 ETH unchanged, nToken quotation scale adjusted to 10 ETH.

4. Both quotation fees are adjusted from 0.33% of the scale to positive integer multiples of a fixed unit fee and up to 255 times. The unit fee of NEST is 0.1ETH and the unit fee of nToken is 0.05ETH.

5. The rate of NEST ming by launching enters the next damping period when 204 NEST will be mined in each block.

6. The upper limit of the block interval of nToken mining is adjusted to 300.

7. Charges for opening nToken oracle are adjusted to 1000 NEST.

8. The quantity of verification blocks is adjusted from 25 to 20.

9. NestNode Token independent mining separates from NEST miner mining and gets NEST Token by block with the 15% speed of all NEST Token mining.

Non-functional adjustments:

1. Adjust the contract structure and redefine the contracts that are allowed to change and need to be fixed this time and in the future.

2. Split DAO into ledger and application (currently there is only one application: repurchase and in the future there may be more DAO applications) which is equivalent to reinventing a Snapshot governed functional contract within NEST Protocol that fully executes on-chain.

3. Adjust the contract data structure mainly to save Gas consumption and part of the calculation will have accuracy loss which is controlled within one part per trillion after the adjustment.

After the official launch of NEST Protocol v 3.6, a series of financial products developed based on NEST Protocol will also be launched one after another during this period. By that time, oracle will serve as the core function of NEST Protocol and the whole protocol will be transformed into an on-chain non-cooperative game system.

NestCore

2021.04.27
