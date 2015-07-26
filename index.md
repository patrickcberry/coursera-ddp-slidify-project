---
title       : Loan Calculator
subtitle    : 
author      : Patrick Berry
job         : Coursera - Developing Data Products Project
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : publish_selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## The questions
* Do you need a new house?
* Do you need a new car?
* How much can you afford to borrow?

---
## How much can you borrow
* Common style of loan in Australia is principle and interest
* How can you determine the loans size that you are able to borrow?
* How can you determine the impact if future changes in interest rates?

---
## The application
* This application calculates principle and interest payments for a loan given the following inputs
    * Loan inital value
    * Loan term
    * Interst rate
    * Payment frequency

---
## The calculations
The loan repayment is calculated as follows,

```r
    pv <- 250000            # inital loan value
    n  <- 20 * 12           # number of periods 20 years, monthly payments
    r  <- 4.5 / 100 / 12    # rate per period, 4.5%
    
    # Payment per period
    p <- (r * pv) / ( 1 - (1 + r)^-n)
    p
```

```
## [1] 1581.623
```
In this example a loan of 250,000 at 4.5% with monthly repayments over a 20 year will require fixed monthly payments of 1581.6234405.

---
## Dislaimer
* This application will calculate repayments only and dosn't predict affordability




