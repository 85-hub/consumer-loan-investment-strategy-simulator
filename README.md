# Investing in Consumer Loans: An Algorithmic Approach

This library is designed to train and test machine learning models that will assist investors in choosing more profitable loans to invest in. 

## Table of Contents
* [Introduction to Consumer Loans and Lending Club](#an-introduction-to-crowd-funded-consumer-loans-and-lending-club)
  * [Personal History](#personal-history)
* [Data Sources](#data-sources)
  * [Lending Club]
  * [Supplemental Sources]
* [Data Preparation](#data-preparation)
* [Modeling](#modeling)
* [Usage](#usage)
* [Future Work](#future-work)
* [References](#references)

## An Introduction to Crowd-Funded Consumer Loans and Lending Club



### Personal History

Back in 2014 I discovered Lending Club and soon afterwards several family members and friends were interested in investing. They opened up and funded accounts but quickly discovered that loan supply was far lower than investor demand. As a result, loans were becoming fully-funded nearly as soon as they were listed on the platform. This made it difficult to make any investments, even if they were on the website at the exact times new loans became available (6 AM, 9 AM, 12 PM, and 3 PM PST) each day. 

I knew there had to be a better way to purchase loans and saw Lending Club had an API for investors. At the time I only knew VBA so I decided to learn enough C# to help my friends and family. I was eventually able to write the code needed to pull in information about new loans, filter them according to each investor's preferred criteria for choosing loans, and then submit purchase orders (see code [here](https://github.com/Booleans/Lending_Club_Automated_Investing)). Everyone was happy, for a time...

Eventually though returns dropped to the point where they no longer seemed like a viable asset to invest in, especially compared to the performance of the S&P 500 over the same period. 

## Motivation
Consumer loans are a relatively new asset class available for private citizens to invest in. They potentially offer returns similar to traditional investments while offering lower portfolio volatility. However, a significant number of consumer loans are defaulted on by the borrowers. A significant amount of capital can be lost to defaults if a portfolio invests in loans based off of poor criteria. The goal of this project is to construct a model to predict the ROI of a loan in order to determine if it would be a good investment. Once a model is built it can be run through a portfolio simulation of historical loan payment data to analyze how the model's strategy would have performed.


## Data Sources
Please see Lending Club's [statistics page](https://www.lendingclub.com/info/download-data.action) for data on loans that have been issued.Files containing all payments that borrowers have made on their loans can be found at Lending Club's [additional statistics page](https://www.lendingclub.com/company/additional-statistics).

Supplemental data comes from the Federal Reserve Economic Database, [FRED](https://fred.stlouisfed.org/). The supplemental data currently used are the monthly values for the bank prime loan rate ([MPRIME](https://fred.stlouisfed.org/series/MPRIME)), the 30-year fixed rate mortgage average ([MORTGAGE30US](https://fred.stlouisfed.org/series/MORTGAGE30US)), as well as the University of Michigan inflation expectation rate ([MICH](https://fred.stlouisfed.org/series/MICH)).
