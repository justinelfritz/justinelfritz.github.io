---
layout: page
title: interest_calculators
description: calculations for compound interest
---

#### Motivation

One of the most common personal finance tasks is to compute long-term compounded interest accrual and corresponding payoff times. The fundamental iteration for an interest accrual event is $$P'=P(1+r/r_c)$$, where $$r$$ is the annual interest rate, $$r_c$$ is the interest compounding rate, $$P$$ is the principal prior to interest accrual, and $$P'$$ is the new principal.  Assuming payments of amount $$x$$ are made at the same frequency as $$r_c$$, the total interest paid over the lifetime of payments is: 


$$Q=x\left(K-R\frac{1-R^K}{1-R}\right)-P(1-R^K)$$,


and the payoff time $$K$$ measured in compounding periods (inverse frequency) is


$$K=-\frac{1}{\mathrm{ln}(R)}\mathrm{ln}(1+\frac{P}{x}\left(1-R\right))$$.


Alternatively we may specify the desired payoff time and deduce the ...