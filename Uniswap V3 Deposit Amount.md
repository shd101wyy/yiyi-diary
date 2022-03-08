---
created: 2021-11-07T06:07:35.165Z
modified: 2021-11-07T06:12:07.991Z
---
> https://ethereum.stackexchange.com/questions/99425/calculate-deposit-amount-when-adding-to-a-liquidity-pool-in-uniswap-v3

To answer the question, first you need to calculate the liquidity `Liquidity_x` that is provided by the asset `x` given the current price and price range. From the [whitepaper](https://uniswap.org/whitepaper-v3.pdf) it can be derived that if the current price is within the range then:

```
Liquidity_x = x * sqrt(price) * sqrt(price_high) / (sqrt(price_high) - sqrt(price))
```

See [this article](http://atiselsts.github.io/pdfs/uniswap-v3-liquidity-math.pdf) for more details. Alternatively, this is the formula for `Liquidity_y` if you have the amount of `y` known:

```
Liquidity_y = y / (sqrt(price) - sqrt(price_low))
```

Then you should use the fact that the goal is to have an optimally balanced position, where `Liquidity_y` == `Liquidity_x`. (Explanation: to calculate the liquidity of a position where the current price is within the price range, Uniswap uses the minimum of the liquidities provided by the two tokens in that position. If the amount of one token is more than necessary, the extra liquidity provided is essentially ignored from a LP perspective. So your goal to have such an amount of `y` in the pool such that the liquidity of `y` exactly matches the liquidity of `x` : `Liquidity_x` is equal to `Liquidity_y`.)

Solving the second equation above for y you get:

```
y = Liquidity_y * (sqrt(price) - sqrt(price_low))
```

In the example:

```
x = 1
price = 2486.8
price_high = 2998.9
price_low = 1994.2
L = x * sqrt(price) * sqrt(price_high) / (sqrt(price_high) - sqrt(price))
# L = 557.9599554712883 in the example
y = L * (sqrt(price) - sqrt(price_low))
```

The result `y` value is 2907.729524805772 USDC which is pretty close to what UI shows.








