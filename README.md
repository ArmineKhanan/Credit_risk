# Credit Card Risk
## Overview: Purpose Definition
Within the challenge, our goal is to develop a statistical model which is capable to classify loans as safe or fradulent. In other words we are confronted to binary classification problem.
In the search for the most suitible model we will first deploy logistic regression model and, afterwards try out ensemble learning approach for the better results.

## Logistic regression
The logistic regression is the most intuitive pick as the dependent variable (either safe or fradulent loan) we aim to predict is dichotomous (binary). Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. That's why we will implement resempling techniques first. 
### Data preperation
After remove missing values from the initial dataset ([LoanStats_2019Q1.csv.zip](https://github.com/ArmineKhanan/Credit_risk/tree/main/Resources)), we are going to leverage a labeled set of 68817 records. The models will be trained on 75% of data and be tested on the rest 25%.

### Naive Random Oversampling
Below the results 

<kbd><img src="https://github.com/ArmineKhanan/Credit_risk/blob/main/Images/Logistic%20Regression%20model.png" width="800" /></kbd>

### Other resampling techniques

## Ensemble Learning 

### Balanced Random Forest Classifier

### Easy Ensemble AdaBoost Classifier

<kbd><img src="https://github.com/ArmineKhanan/Credit_risk/blob/main/Images/Ensemble%20AdaBoost%20Classifier.png" width="800" /></kbd>


## Summary
