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
