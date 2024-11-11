# Finance Notes

## Interest Rates

### Continuously Compounded Interest Rate

$$
  R_c = m \ln \left(1 + \frac{R_m}{m}\right)
$$

$$
  R_m = m \left(\mathrm{e}^\frac{R_c}{m} - 1\right)
$$

- $R_c$ is the continuously compounded interest rate
- $R_m$ is the equivalent interest rate with compounding $m$ times per annum

### Forward Interest Rate

$$
  R_F = R_2 + (R_2 - R_1) \frac{T_1}{T_2 - T_1}
$$

- $R_F$ is the forward interest rate for the period of time between $T_1$ and $T_2$
- $R_1$ and $R_2$ are the zero rates for maturities $T_1$ and $T_2$, respectively
- $T_1$ and $T_2$ are the numbers of years

### Instantaneous Forward Rate

$$
  R_F = -\frac{\partial}{\partial T} \ln P(0, T)
$$

- $R_F$ is the instantaneous forward rate for a maturity of $T$
- $T$ is the number of years
- $P(0, T) = \mathrm{e}^{- R T}$ is the price of a zero-coupon bond maturing at time $T$ wherein $R$ is the zero rate
for a maturity of $T$

### Bond Price and Bond Yield

$$
  B = \sum_{i = 1}^n c_i \mathrm{e}^{-y t_i}
$$

- $B$ is the bond price
- $c_i$ is the cash flow at time $t_i$
- $y$ is the bond yield with continuously compounding
- $t_i$ is the number of years

### Bond Duration

$$
  D = \sum_{i = 1}^n t_i \frac{c_i \mathrm{e}^{-y t_i}}{B}
$$

$$
  \frac{\Delta B}{B} = -D \Delta y
$$

- $D$ is the bond duration
- $t_i$ is the number of years
- $c_i$ is the cash flow at time $t_i$
- $y$ is the bond yield with continuously compounding
- $B$ is the bond price

### Modified Bond Duration

$$
  D^* = \frac{D}{1 + \frac{y}{m}}
$$

$$
  \Delta B = - B D^* \Delta y
$$

- $D^*$ is the modified bond duration
- $D$ is the bond duration
- $y$ is the bond yield with compounding $m$ times per annum
- $B$ is the bond price

### Convexity

$$
  \Delta B = \frac{\mathrm{d} B}{\mathrm{d} y} \Delta y + \frac{1}{2} \frac{\mathrm{d}^2 B}{\mathrm{d} y^2} \Delta y^2
$$

- $B$ is the bond price
- $y$ is the bond yield with continuous compounding

## Interest Rate Futures

### Futures Price

$$
  F_0 = (S_0 - I) \mathrm{e}^{r T}
$$

- $F_0$ is the futures price
- $S_0$ is the spot price
- $I$ is the present value of the coupons during the life of the futures contract
- $r$ is the risk-free interest rate applicable to a period of length $T$
- $T$ is the time to maturity in years

### Zero Curve

$$
  R_2 = \frac{R_F (T_2 - T_1) + R_1 T_1}{T_2}
$$

- $R_1$ and $R_2$ are the zero rates for maturities $T_1$ and $T_2$, respectively
- $R_F$ is the forward rate applicable to the period between $T_1$ and $T_2$
- $T_1$ and $T_2$ are the number of years

### Duration-Based Hedge Ratio

$$
  N^* = \frac{P D_P}{V_F D_F}
$$

- $N^*$ is the duration-based hedge ratio
- $P$ is the forward value of the portfolio being hedged at the maturity of the hedge
- $D_P$ is the duration of the portfolio at the maturity of the hedge
- $V_F$ is the contract price for one interest rate futures contract
- $D_F$ is the duration of the asset underlying the futures contract at the maturity of the futures contract

## XVAs

### CVA

$$
  \text{CVA} = \sum_{i = 1}^N q_i v_i
$$

- $\text{CVA}$ is the credit valuation adjustment, which is estimate of the present value of the expected cost of a
counterparty default
- $N$ is the number of intervals in the period of the longest outstanding derivatives transaction with the counterparty
- $q_i$ is the probability of default by the counterparty during the $i$th interval
- $v_i$ is the present value of the expected loss if there is a counterparty default at the midpoint of the $i$th
interval

### DVA

$$
  \text{DVA} = \sum_{i = 1}^N q^*_i v^*_i
$$

- $\text{DVA}$ is the debit valuation adjustment, which is the present value of the expected gain of the bank itself
defaulting
- $N$ is the number of intervals in the period of the longest outstanding derivatives transaction with the counterparty
- $q_i$ is the probability of default by the bank itself during the $i$th interval
- $v_i$ is the present value of the expected gain if there is a bank default at the midpoint of the $i$th interval
