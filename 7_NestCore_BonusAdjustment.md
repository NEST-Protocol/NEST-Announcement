# Dividend adjustment
## Revenue leveling threshold Q:

> Q = 100 * (1 + 3%) ^ n

> N in the above algorithm: the number of NESTs that have been mined is n billion, and n is an integer.

## Leveling Algorithm

> Define this week's dividend income as: E;

> The cumulative total of ETH in the stabilization fund is: M;

> If E ≥ Q:

> The amount of ETH entered into the stabilization fund this week is: E * 10%;

> If E * 90% <Q:

> (Q-E) ETH will be taken from the leveling fund, the amount will be filled up to Q ETH, and then dividends will be paid. At this time, the number of dividends this week is Q ETH;

> If E * 90% ≥ Q:

> The actual number of ETH dividends this week is: E * 90%;

> If E <Q:

> The amount of ETH entered into the stabilization fund this week is: 0;

> Will be taken from the leveling fund M: (Q-E) ETH, make up the amount to Q ETH, and then pay dividends. At this time, the number of dividends this week is Q ETH;

> If it cannot be filled, the number of dividends this week is: M + E ETH.

> NEST level contract address: 0xc2CdF3457819A61720166d524F6E320C5451092C

---

# 分红调整
## 收益平准阈值 Q ：

> Q = 100 * (1 + 3%)^n

> 上面算法中的 n 代表：已经被挖出来的 NEST 数量为 n 亿，n 取整数。

## 平准算法

> 定义本周的分红收益为 ：E；

> 平准基金中的 ETH 累积总量为：M；

> 如果 E ≥ Q ：

> 本周进入平准基金中的 ETH 数量为：E * 10%；

> 如果 E * 90% < Q：

> 会从平准基金中取出（Q - E）个 ETH，补齐数量至 Q ETH，然后进行分红。此时，本周的分红数量为 Q ETH；

> 如果 E * 90% ≥ Q：

> 本周的 ETH 实际分红数量为： E * 90%；

> 如果 E < Q：

> 本周进入平准基金中的 ETH 数量为：0 ；

> 会从平准基金 M 中取出：（Q - E）个 ETH，补齐数量至 Q ETH，然后进行分红。此时，本周的分红数量为 Q ETH；

> 如果无法补齐，本周的分红数量为：M + E 个 ETH。

> NEST 平准合约地址：0xc2CdF3457819A61720166d524F6E320C5451092C
