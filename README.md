# Mod18_Challenge

"Job loss, illness and natural disaster are common reasons for default" (https://money.usnews.com/loans/articles/what-happens-if-you-default-on-a-loan#:~:text=%22A%20loan%20may%20go%20into,are%20common%20reasons%20for%20default.)

Deliverable 4: Written Report on the Credit Risk Analysis
For this deliverable, you’ll write a brief summary and analysis of the performance of all the machine learning models used in this Challenge.

The report should contain the following:

Overview of the analysis: Explain the purpose of this analysis.

Results: Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all six machine learning models. Use screenshots of your outputs to support your results.

Summary: Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. If you do not recommend any of the models, justify your reasoning.


Analysis
The written analysis has the following:

Overview of the loan prediction risk analysis:

The purpose of this analysis is well defined (4 pt)
Results:

There is a bulleted list that describes the balanced accuracy score and the precision and recall scores of all six machine learning models (15 pt)
Summary:

There is a summary of the results (2 pt)
There is a recommendation on which model to use, or there is no recommendation with a justification (3 pt)


# Credit Risk Analysis

## Overview

The five major risks for banks are credit, operational, market, and liquidity risks (https://corporatefinanceinstitute.com/resources/risk-management/major-risks-for-banks/). Operational risks are lose and damages caused in day to day operations due to errors, property damage, or fraud.  These risks are minimal for most banks.  Market risk are only relevant to banks who participate in market trading and are due to the unpredictablity of the markets.  Liquidity risks are one risk that has been in the news lately and occur when banks do not have enough funds on hand to deal with customers taking money out of the banks.  Credit risk is the largest risk for banks.  This is a risk that cannot be avoided because lending money and issuing credit cards is the primary way that banks make money.  It is essintial to the business model of banks.  Creating a machine learning model to determine the whether a person is a risk on not repaying is the goal of this project.  

One of the major difficulties in creating a good model is the imbalance of the data.  The vast majority of individuals repay their debts.  Simple machine learning techniques are not able to predict the small number of defaults.  Therefore, resampling techniques designed to deal with imbalanced data will be used including oversampling, undersampling, and combined over/undersampling approaches to generate balanced data for that will then be used in machine learning algorthms.  In addition, two machine learning models that reduce bias will be run.  All the results will be compared and equaluated to redetermine how well they preformed in predicting credit risk.

## Results

| Algorthm | balanced accuracy | precision | recall |
| :---     |          ---: |          ---: |         ---: |
| Naive Random Oversampling |0.66 |0.01   |   0.72 |
| SMOTE Oversampling | 0.66 | 0.01   |   0.61 |
| Undersampling | 0.60 | 0.01   |   0.61  |
| #Combination (Over and Under) Sampling | 0.65 | 0.01  |    0.70 |
| Balanced Random Forest Classifier | 0.76 | 0.03  |    0.63 | 
| Easy Ensemble AdaBoost Classifier | 0.92 | 0.09   |   0.89 |

