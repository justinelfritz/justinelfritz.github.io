---
layout: page
title: interest_calculators
description: calculations for compound interest
---

#### Motivation

One of the most common personal finance tasks is to compute long-term compounded interest accrual and corresponding payoff times. The fundamental iteration for an interest accrual event is:

<img src="https://render.githubusercontent.com/render/math?math=P`=P(1+r/r_c)">,

where <img src="https://render.githubusercontent.com/render/math?math=r"> is the annual interest rate, <img src="https://render.githubusercontent.com/render/math?math=r_c"> is the interest compounding rate, <img src="https://render.githubusercontent.com/render/math?math=P"> is the principal prior to interest accrual, and <img src="https://render.githubusercontent.com/render/math?math=P`"> is the new principal.  Assuming payments of amount <img src="https://render.githubusercontent.com/render/math?math=x"> are made at the same frequency as <img src="https://render.githubusercontent.com/render/math?math=r_c">, the total interest paid over the lifetime of payments is: 

<img src="https://render.githubusercontent.com/render/math?math=Q=x\left(1+K+\frac{1-R^{1+K}}{1-R}\right)-P(1-R^K)">,

and the payoff time <img src="https://render.githubusercontent.com/render/math?math=K"> measured in compounding periods (inverse frequency) is

<img src="https://render.githubusercontent.com/render/math?math=K=-ln(1+\frac{P}{x}\left(1-R\right))/ln(R)">.

Alternatively we may specify the desired payoff time ... 

Is there native support now for inline equations like $`\sigma = \sqrt{1-x^2}`$ or a standalone equation such as: 

$$\left(l^2-m^2 + \frac{\mathrm{d}\theta}{\mathrm{sin}\theta}\right) = y^2$$

and continue with more text here



