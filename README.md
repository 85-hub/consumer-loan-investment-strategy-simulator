# Investing in Personal Loans: An Algorithmic Approach

This library was made to train and test machine learning models that can accurately predict the return on investment of a personal loan. This will assist investors in boosting the returns of their portfolios by avoiding poor-performing loans.

## Table of Contents
* [Introduction to Personal Loans and Lending Club](#an-introduction-to-crowd-funded-consumer-loans-and-lending-club)
  * [What is a Personal Loan?](#what-is-a-personal-loan)
  * [Why Do People Get Personal Loans?](#why-do-people-get-personal-loans)
  * [What is Lending Club?](#what-is-lending-club)
  * [My History](#personal-history)
* [Data Sources](#data-sources)
  * [Lending Club]
  * [Supplemental Sources]
* [Data Preparation](#data-preparation)
* [Modeling](#modeling)
* [Usage](#usage)
* [Future Work](#future-work)
* [References](#references)

## An Introduction to Crowd-Funded Personal Loans and Lending Club

### What is a Personal Loan?

A personal loan is money borrowed from a credit union, brick-and-mortar bank, or through an online lending marketplace, and can be used for just about anything you want. Loans are paid back in fixed, regular monthly installments over a set period of time. Current average APRs for personal loans range from 10% to 28%. Repayment terms generally vary from one to seven years in length. Individual personal loan rates, terms, and eligibility are based on several factors, including your credit score, payment history, ability to repay the loan, and the lender.

### Why Do People Get Personal Loans?

Depending on what the money is for and your borrowing history, there may be multiple benefits to obtaining a personal loan. If you have outstanding credit card balances, medical bills, or other high-interest debt, a personal loan can help you pay down your debts faster at an interest rate and monthly payment that you can responsibly afford. 

Converting high-interest debt into low(er)-interest debt can significantly reduce the time needed to pay off debt. 

### What is Lending Club?



### Personal History

Back in 2014 I discovered Lending Club and soon afterwards several family members and friends were interested in investing. They opened up and funded accounts but quickly discovered that loan supply was far lower than investor demand. As a result, loans were becoming fully-funded nearly as soon as they were listed on the platform. This made it difficult to make any investments, even if they were on the website at the exact times new loans became available (6 AM, 9 AM, 12 PM, and 3 PM PST) each day. 

I knew there had to be a better way to purchase loans and saw Lending Club had an API for investors. At the time I only knew VBA so I decided to learn enough C# to help my friends and family. I was eventually able to write the code needed to pull in information about new loans, filter them according to each investor's preferred criteria for choosing loans, and then submit purchase orders (see code [here](https://github.com/Booleans/Lending_Club_Automated_Investing)). Everyone was happy, for a time...

Eventually though returns dropped to the point where they no longer seemed like a viable asset to invest in, especially compared to the performance of the S&P 500 over the same period. 

**insert ROI chart here**

This repository is my attempt at using machine learning in order to remedy that situation. The goal is to create a model that will accurately predict a loan's future ROI in order to avoid poorly-performing loans and choose the more profitable options. 

## Motivation
Consumer loans are a relatively new asset class available for private citizens to invest in. They potentially offer returns similar to traditional investments while offering lower portfolio volatility. However, a significant number of consumer loans are defaulted on by the borrowers. A significant amount of capital can be lost to defaults if a portfolio invests in loans based off of poor criteria. The goal of this project is to construct a model to predict the ROI of a loan in order to determine if it would be a good investment. Once a model is built it can be run through a portfolio simulation of historical loan payment data to analyze how the model's strategy would have performed.


## Data Sources
Please see Lending Club's [statistics page](https://www.lendingclub.com/info/download-data.action) for data on loans that have been issued.Files containing all payments that borrowers have made on their loans can be found at Lending Club's [additional statistics page](https://www.lendingclub.com/company/additional-statistics).

Supplemental data comes from the Federal Reserve Economic Database, [FRED](https://fred.stlouisfed.org/). The supplemental data currently used are the monthly values for the bank prime loan rate ([MPRIME](https://fred.stlouisfed.org/series/MPRIME)), the 30-year fixed rate mortgage average ([MORTGAGE30US](https://fred.stlouisfed.org/series/MORTGAGE30US)), as well as the University of Michigan inflation expectation rate ([MICH](https://fred.stlouisfed.org/series/MICH)).
