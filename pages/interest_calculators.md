---
layout: page
title: Compound Interest
description: calculations for compound interest
---

#### Motivation

One of the most common personal finance tasks is to compute long-term compounded interest accrual and corresponding payoff times. The objective here is to present closed analytical forms for the total interest paid over an asset's lifetime (*e.g.,* a loan), and **either** the required monthly payment amount as a function of the desired lifetime or the resultant lifetime as a function of the desired monthly payment.

#### Results

The fundamental iteration for an interest accrual event is $$P'=P(1+r/r_c)$$, where $$r$$ is the annual interest rate, $$r_c$$ is the interest compounding rate (*i.e.,* $$r_c=12$$ for monthly compounding), $$P$$ is the principal amount, and $$P'$$ is the updated principal. The iterator shorthand is $$R=(1+r/r_c)$$.


#### Case 1: Input desired payment amount
Assuming payments of amount $$x$$ are made at the same frequency as $$r_c$$, the payoff time $$K$$ measured in compounding periods is

$$K=-\frac{1}{ln(R)}ln(1+\frac{P}{x}\left(1-R\right))$$.


*Case 1 calculator*:
<div>
  <input type="number" id="apr1" placeholder="APR (%)" />
  <input type="number" id="rc1" placeholder="Compounding Periods Per Year" />
  <input type="number" id="principal1" placeholder="Principal ($)" />
  <input type="number" id="payment1" placeholder="Payment Amount ($)"/>
  <button onclick="calculateCase1()">Calculate Payoff Time</button>
  <p id="case1Result"></p>
  <p id="int1Result"></p>
</div>

<script>
  function calculateCase1() {
    const apr = parseFloat(document.getElementById('apr1').value);
    const rc = parseFloat(document.getElementById('rc1').value);
    const princ = parseFloat(document.getElementById('principal1').value);
    const pmt = parseFloat(document.getElementById('payment1').value);
    
    if (apr >= 0 && rc > 0 && princ >= 0 && pmt > 0) {
      // Scale APR from percentage (e.g. 5% -> 0.05) and divide by compounding periods
      const ratePerPeriod = (apr / 100) / rc;
      const aprscaled = 1.00 + ratePerPeriod; 
      
      // Safety check: Is the payment large enough to cover accruing interest?
      const interestAccrued = princ * ratePerPeriod;
      if (pmt <= interestAccrued) {
        document.getElementById('case1Result').innerText = 
          `Payment is too small. Minimum required to cover interest is $${interestAccrued.toFixed(2)}.`;
        return;
      }

      // Calculate number of payments using the loan payoff formula
      const prefix = -1.00 / Math.log(aprscaled);
      const y = Math.log((princ / pmt) * (1.00 - aprscaled) + 1.00);
      const periods = prefix * y;
      
      //const fac1 = pmt*(periods - aprscaled*((1.00-aprscaled**periods)/(1-aprscaled)))
      //const fac2 = princ*(1.00 - aprscaled**periods)
      //const interest = fac1 - fac2
      const interest = (pmt * periods) - princ;

      document.getElementById('case1Result').innerText = 
        `Number of payments: ${periods.toFixed(2)}`;
      document.getElementById('int1Result').innerText = 
        `Total Interest Paid: ${interest.toFixed(2)}`;
    } else {
      document.getElementById('case1Result').innerText = "Please provide valid inputs.";
      document.getElementById('int1Result').innerText = "";
    }
  }
</script>

#### Case 2: Input desired payment duration
Alternatively we may specify the desired payoff time $$K$$ and deduce the required payment amount, which is

$$x=-P\frac{1-R}{1-R^{-K}}$$.


Using a mixture of the above inputs, the total interest paid over the lifetime of payments is finally

$$Q=x\left(K-R\frac{1-R^K}{1-R}\right)-P(1-R^K)$$.

*Case 2 calculator*:
<div>
  <input type="number" id="apr2" placeholder="APR (%)" />
  <input type="number" id="rc2" placeholder="Compounding Periods Per Year" />
  <input type="number" id="principal2" placeholder="Principal ($)" />
  <input type="number" id="periods2" placeholder="Number Of Payments"/>
  <button onclick="calculateCase2()">Calculate Payment Amount</button>
  <p id="case2Result"></p>
  <p id="int2Result"></p>
</div>

<script>
  function calculateCase2() {
    const apr = parseFloat(document.getElementById('apr2').value);
    const rc = parseFloat(document.getElementById('rc2').value);
    const princ = parseFloat(document.getElementById('principal2').value);
    const periods = parseFloat(document.getElementById('periods2').value);
    
    if (apr >= 0 && rc > 0 && princ >= 0 && periods > 0) {
      // Scale APR from percentage (e.g. 5% -> 0.05) and divide by compounding periods
      const ratePerPeriod = (apr / 100) / rc;
      const aprscaled = 1.00 + ratePerPeriod; 
      
      const pmt = -princ*(1.00 - aprscaled)/(1.00 - aprscaled**(-periods))

      //const fac1 = pmt*(periods - aprscaled*((1.00-aprscaled**periods)/(1-aprscaled)))
      //const fac2 = princ*(1.00 - aprscaled**periods)
      //const interest = fac1 - fac2
      const interest = (pmt * periods) - princ;
      document.getElementById('case2Result').innerText = 
        `Payment Amount: ${pmt.toFixed(2)}`;
      document.getElementById('int2Result').innerText = 
        `Total Interest Paid: ${interest.toFixed(2)}`;
    } else {
      document.getElementById('case2Result').innerText = "Please provide valid inputs.";
      document.getElementById('int2Result').innerText = "";
    }
  }
</script>
