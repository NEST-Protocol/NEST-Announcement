# Mining

NEST2.0 mining system changed from using mining to quote mining, incentivizing price providers

### Block attenuation factor

> Attenuation interval: 2400000 blocks (one year)

> Attenuation: 10%

### Block output
> The initial value of block mining volume is 400NEST / block, and it will decrease by 10% after every 2,400,000 blocks. After the launch of NEST2.0, the block output is 360NEST / block (1 billion has been mined)

### The number of mining this time

> Total mining output of this block: (this block-last mining block) * block mining amount

> Trading pair mining volume: this block contains multiple trading pair quotes, each trading pair splits the total mining volume of this block

> Individual quoted ore output: The proportion of the individual quoted commission fee to the total transaction pair transaction fee fee ratio

# Quote
### Currently supports trading pairs
1. USDT / ETH
2. HT / ETH

### Quote
> Assets: Generate a quotation and transfer it into the corresponding asset (the asset is in the quotation), and charge 1% of the ETH amount in the asset as a handling fee and transfer it to the dividend pool.

> Price takes effect: After the quotation is created, the price takes effect more than 25 blocks (5 minutes)

> Price calculation: multiple quotes for the same transaction in the same block, calculated by weighted average

### Trade offer

> Transaction: After the target quotation is created, before 25 blocks (including 25 blocks), the quotation can be selected to trade assets in any direction. At the same time, a quotation that is twice the transaction ETH is sent and transferred to the asset (a new quote).

> Price calculation: There is no part that is traded in the quote, participate in the weighted average calculation of the current block price

### Take Asset

> Retrieval: After the inspection report is in effect (more than 25 blocks), it can be retrieved and mined.

---

# 挖矿

NEST2.0挖矿体系由使用挖矿变为报价挖矿，激励价格提供者

### 区块出矿量衰减系数

> 衰减间隔: 2400000区块(一年)

> 衰减程度: 10%

### 区块出矿量
> 区块出矿量初始值为400NEST/区块，每过2400000区块衰减10%。NEST2.0上线后，区块出矿量为360NEST/区块(已挖出10亿)

### 本次挖矿数量

> 本次区块总出矿量: (本次区块 -上次挖矿区块) * 区块出矿量

> 交易对出矿量:本次区块中包含多种交易对报价，各个交易对平分本次区块总出矿量

> 个人报价出矿量: 个人报价手续费占交易对交易量手续费总和比例，占比交易对出矿量

# 报价
### 目前支持交易对
1. USDT/ETH
2. HT/ETH

### 报价
> 资产: 生成报价单并转入对应资产(资产在报价单中)，收取资产中ETH数量1%作为手续费转入分红池。

> 价格生效: 报价单创建后，超过25区块(5分钟)，价格生效

> 价格计算: 同一区块中, 同一交易对多笔报价，以加权平均方式计算

### 交易报价

> 交易: 在目标报价单创建后，25区块前(包含25区块)，可选择该报价单任意方向资产交易。同时发出一个是交易ETH两倍的报价单并转入资产(一个新报价)。

> 价格计算: 报价中没有被交易部分，参与当前区块价格的加权平均计算

### 取回报价资产

> 取回: 报检单生效后(超过25区块)，可以取回，并挖矿。





