---
title       : Fixed Loan Payment Amortizer
subtitle    : Developing Data Products Project
author      : Matthew Bender
job         : Johns Hopkins Student
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      #
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Problem 1

Consumers would rather select the amouth money to pay each month for a loan & 
have the loan term calculated for that payment. Traditionally, a consumer 
selects the term of the loan and the payment is calculated for that term. 

## Problem 2

Consumers prefer to pay a monthly payment that is rounded to the nearest 25
dollars than pay an unremember amount each month. $275 is much easier to 
remember, than $263.81.

---

## Solution

_Fixed Loan Payment Amortizer_ is a fixed payment amortization calculator, that
allow the consumer to select the loan amount, interest rate, & monthly payment 
they want to make adjustable in increaments of $25.

---

## Features
#### Calculations
Loan Term, Finance Change (Total interest paid over the life of the loan), Total of Payments

#### Plot


```r
ggplot(schedule, aes(x=period, y=endingPrincipalBalance)) +
    geom_bar(stat="identity") +
    labs(list(title = "Loan Remaining Balance over time",
      x = "Number of payment period", y = "Remaining Balance (Dollars)"))
```

![plot of chunk unnamed-chunk-2](assets/fig/unnamed-chunk-2-1.png) 

---

## Features
#### Amortization Table


```r
head(schedule, n=10)
```



| period| beginningPrincipalBalance| interestPayment| principalPayment| totalPayment| endingPrincipalBalance|
|------:|-------------------------:|---------------:|----------------:|------------:|----------------------:|
|      1|                   5000.00|           11.82|           463.18|          475|                4536.82|
|      2|                   4536.82|           10.72|           464.28|          475|                4072.54|
|      3|                   4072.54|            9.62|           465.38|          475|                3607.16|
|      4|                   3607.16|            8.52|           466.48|          475|                3140.68|
|      5|                   3140.68|            7.42|           467.58|          475|                2673.10|
|      6|                   2673.10|            6.32|           468.68|          475|                2204.42|
|      7|                   2204.42|            5.21|           469.79|          475|                1734.63|
|      8|                   1734.63|            4.10|           470.90|          475|                1263.73|
|      9|                   1263.73|            2.99|           472.01|          475|                 791.72|
|     10|                    791.72|            1.87|           473.13|          475|                 318.59|

