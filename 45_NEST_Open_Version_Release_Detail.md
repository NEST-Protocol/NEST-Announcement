## NEST open version detail

NEST open version will be released on BSC on November 20, 2021. The details are as follows:

1. Everyone can specify a quotation pair and open the quotation channel. When opening the quotation channel, you can specify pricing token, quotation token and mining token address, and set parameters such as rewardPerBlock, singleFee and reductionRate;

2. The signatures of interfaces such as post, close and price query are adjusted accordingly, but the core mechanism of nest price formation remains unchanged;

3. The same quotation pair can be opened multiple times and compete with each other;

4. Optimize and adjust some parameters of nest, the following are the specific parameter values:

| Name | Value | Remark |
| ---- | ---- | ---- |
| Attenuation gradient array | 400, 320, 256, 204, 163, 131, 104, 83, 67, 53, 40 | Attenuation once every 10000000 blocks |
| Number of blocks in one year | 10000000 |
| Block  time | 3 seconds | |
| Verification block number | 50 | |
| Number of nests mortgaged per unit quotation | 100000 | |
| Doubling times of eating order | 4 | |

5. When released, ETH/usdt quotation channel will be opened through PETH and PUSD. The specific parameters are as follows:

| Name | Value | Remark |
| ---- | ---- | ---- |
| token0 | PUSD | |
| token1 | PETH | |
| reward | NEST | |
| token0 unit | 2000PUSD | |
| total reward number | 100000000NEST | |
| post fee | 0 | |
| single fee | 0.005BNB	| |
| Standard reward per block | 4NEST | Note that the attenuation will be calculated from the opening block, that is, this parameter is the ore yield of the block in the first attenuation interval after opening |
| reduction rate | 0.8 |	

Nest Core

2021-11-19
