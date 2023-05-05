low_risk     68470
high_risk      347

Precision — What percent of your predictions were correct?
Recall — What percent of the positive cases did you catch? True Positive Rate
Specificity - True Negative Rate

F1 score — What percent of positive predictions were correct?

index balanced accuracy -  mean of Sensitivity (True Positive Rate) and Specificity (True Negative Rate) 

geometric mean - the square root of the product of sensitivity and specificity.


#Oversampling

##Naive Random Oversampling
balanced_accuracy_score - 0.6620175698580149

                  pre       rec       spe        f1       geo       iba       sup

  high_risk       0.01      0.72      0.60      0.02      0.66      0.44       101
   low_risk       1.00      0.60      0.72      0.75      0.66      0.43     17104

avg / total       0.99      0.60      0.72      0.75      0.66      0.43     17205


##SMOTE Oversampling
balanced_accuracy_score - 0.6568196079430206

                   pre       rec       spe        f1       geo       iba       sup

  high_risk       0.01      0.61      0.70      0.02      0.66      0.43       101
   low_risk       1.00      0.70      0.61      0.82      0.66      0.43     17104

avg / total       0.99      0.70      0.61      0.82      0.66      0.43     17205


#Undersampling
balanced_accuracy_score - 0.6027679241263696

                   pre       rec       spe        f1       geo       iba       sup

  high_risk       0.01      0.61      0.59      0.02      0.60      0.36       101
   low_risk       1.00      0.59      0.61      0.74      0.60      0.36     17104

avg / total       0.99      0.59      0.61      0.74      0.60      0.36     17205

##Combination (Over and Under) Sampling
balanced_accuracy_score - 0.6461148570422992

                   pre       rec       spe        f1       geo       iba       sup

  high_risk       0.01      0.70      0.58      0.02      0.64      0.41       101
   low_risk       1.00      0.58      0.70      0.73      0.64      0.40     17104

avg / total       0.99      0.58      0.70      0.73      0.64      0.40     17205


#Ensemble Learners

#Balanced Random Forest Classifier
balanced_accuracy_score - 0.75576409663885

top 5

[(0.07480819356976856, 'total_rec_prncp'),
 (0.063403927433907, 'total_pymnt'),
 (0.06025001404579047, 'total_rec_int'),
 (0.05476153343055574, 'total_pymnt_inv'),
 (0.05235733392264809, 'last_pymnt_amnt'),
 


                   pre       rec       spe        f1       geo       iba       sup

  high_risk       0.03      0.63      0.88      0.06      0.75      0.54       101
   low_risk       1.00      0.88      0.63      0.93      0.75      0.57     17104

avg / total       0.99      0.88      0.64      0.93      0.75      0.57     17205


##Easy Ensemble AdaBoost Classifier
balanced_accuracy_score - 0.9201119071214886


                   pre       rec       spe        f1       geo       iba       sup

  high_risk       0.09      0.89      0.95      0.17      0.92      0.84       101
   low_risk       1.00      0.95      0.89      0.97      0.92      0.85     17104

avg / total       0.99      0.95      0.89      0.97      0.92      0.85     17205
