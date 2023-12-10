---
layout: page
title: Compound Interest
description: calculations for compound interest
---

#### Motivation

One of the most common personal finance tasks is to compute long-term compounded interest accrual and corresponding payoff times. The objective here is to present closed analytical forms for the total interest paid over an asset's lifetime (*e.g.,* a loan), and **either** the required monthly payment amount as a function of the desired lifetime or the resultant lifetime as a function of the desired monthly payment.

#### Results

The fundamental iteration for an interest accrual event is $$P'=P(1+r/r_c)$$, where $$r$$ is the annual interest rate, $$r_c$$ is the interest compounding rate (*i.e.,* $$1/12$$ for monthly compounding), $$P$$ is the principal amount, and $$P'$$ is the updated principal. The iterator shorthand is $$R=(1+r/r_c)$$.


#### Case 1: Input desired payment amount
Assuming payments of amount $$x$$ are made at the same frequency as $$r_c$$, the payoff time $$K$$ measured in compounding periods (inverse frequency) is

$$K=-\frac{1}{ln(R)}ln(1+\frac{P}{x}\left(1-R\right))$$.


#### Case 2: Input desired payment duration
Alternatively we may specify the desired payoff time $$K$$ and deduce the required payment amount $$x$$: 

$$x=-P\frac{1-R}{1-R^{-K}}$$


The total interest paid over the lifetime of payments is then

$$Q=x\left(K-R\frac{1-R^K}{1-R}\right)-P(1-R^K)$$.
