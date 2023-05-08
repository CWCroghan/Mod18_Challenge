# Credit Risk Analysis

# Overview

The five major risks for banks are credit, operational, market, and liquidity risks (https://corporatefinanceinstitute.com/resources/risk-management/major-risks-for-banks/). Operational risks are losses and damages caused in day-to-day operations due to errors, property damage, or fraud.  These risks are minimal for most banks.  Market risks are only relevant to banks who participate in the market trading and are due to the unpredictability of the markets.  Liquidity risks are one risk that has been in the news lately and occurs when banks do not have enough funds on hand to deal with customers taking money out of the banks.  Credit risk is the largest risk for banks.  This is a risk that cannot be avoided because lending money and issuing credit cards is the primary way that banks make money.  It is essential to the business model of banks.  Creating a machine learning model to determine whether a person is a risk of not repaying is the goal of this project.  

One of the major difficulties in creating a good model is the imbalance of the data.  The vast majority of individuals repay their debts.  Simple machine learning techniques are not able to predict the small number of defaults.  Therefore, resampling techniques designed to deal with imbalanced data will be used including oversampling, under-sampling, and combined over/sampling-sar-sampling approaches to generate balanced data for that will then be used in machine learning algorithms.  In addition, two machine learning models that reduce bias will be run.  All the results will be compared to redetermine how well they performed in predicting credit risk.

## Results

The models were trained on **% of the data with **% held back for testing. The models were trying to predict who would default.  Therefore, defaulting is the positive outcome.


To compare the six different models, we will be using the following scores:
    Precision — What percent of your predictions were correct?
    Recall — What percent of the positive (defaulting) cases did you catch? 
    Balanced Accuracy -  mean of Recall (True Positive Rate) and Specificity (True Negative Rate) 

The following table has all the scores for the six models and three measurements for easy comparison.

### Table of Performance Scores

| Algorithm | Balanced Accuracy | Precision | Recall |
| :---|---: |---: |---: |
| Naive Random Oversampling |0.66 |0.01   |   0.72 |
| SMOTE Oversampling | 0.66 | 0.01   |   0.61 |
| Under sampling | 0.60 | 0.01   |   0.61  |
| Combination (Over and Under) Sampling | 0.65 | 0.01  |    0.70 |
| Balanced Random Forest Classifier | 0.76 | 0.03  |    0.63 | 
| Easy Ensemble AdaBoost Classifier | 0.92 | 0.09   |   0.89 |

## Summary

Since the vast majority of the clients did not default, the Balanced Accuracy and Recall scores are overly inflated.  Therefore, we will concentrate on the Precision scores.  The highest precision score is 0.09 which means that of every 100 flagged applications it would successfully predict a default only 9 times.  The other 91 applications would not have defaulted.  

One of the primary manners in which banks make money is through credit cards via fees and interest on balances.  Eliminating 100 applications to remove the risk of only 9 is not good business sense.

In this day and age, it is crucial to have access to a credit card.  At no other time in history have there been so many stores that refuse to take cash from your local coffee shop to many high-end retailers (reference needed).  The movement away from cash and limit to credit only has even been taken up at the local bodegas, which in some neighborhoods are the only convenient place to buy groceries.  Denying people access to a credit card is no longer just denying them a luxury.  Credit cards have become a necessity.

In general, people do not plan on defaulting.  Circumstances outside of their control are the root cause of defaulting. These models fail because the models cannot predict bad luck.  The three top reasons why people default on debt are job loss, illness, and natural disasters (https://money.usnews.com/loans/articles/what-happens-if-you-default-on-a-loan#:~:text=%22A%20loan%20may%20go%20into,are%20common%20reasons%20for%20default).  In uncertain times with massive lay-offs and business closures, even job loss is out of the control of the client.  


None of the models perform well enough to be used in such an important decision for both the banks and the clients.

