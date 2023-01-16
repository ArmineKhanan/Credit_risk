# Credit Card Risk
## Overview: Purpose Definition
Within the challenge, our goal is to develop a statistical model capable of classifying loans as safe or fraudulent. In other words, we are confronted with a binary classification problem. In the search for the most suitable model, we will first deploy the logistic regression model and, afterward, try out the ensemble learning approach for better results.

## Logistic regression
### Data Preparation
After removing missing values from the initial dataset  ([LoanStats_2019Q1.csv.zip](https://github.com/ArmineKhanan/Credit_risk/tree/main/Resources)), we plan to leverage a labeled set of 68817 records. The models will be trained on 75% of the data and tested on the rest 25%.

### Naive Random Oversampling
Credit risk is an unbalanced classification problem, as good loans easily outnumber risky loans. That's why we will implement resampling techniques first. The first resampling strategy implemented is naive random oversampling, presented below: 

<kbd><img src="https://github.com/ArmineKhanan/Credit_risk/blob/main/Images/Logistic%20Regression%20model.png" width="800" /></kbd>

The balanced accuracy score, ranging from 0 to 1, indicates the fairness of the classification model. 0.62 is a moderate result and urges us to seek better solutions. The other measure worth our attention to is the low recall rate for high-risk loans: 58%.

### Other resampling techniques
To yield better results, we tried out a few more resampling solutions:
* Synthetic Minority Oversampling
* Cluster Centroids Undersampling
* Combination over- and under-sampling: SMOTEENN algorithm

Nevertheless, alternative resampling strategies increased neither the balanced accuracy score nor the recall rate for high-risk loans of the logistic regression model sufficiently. Ultimately we went for ensemble learning algorithms.

## Ensemble Learning 
### Balanced Random Forest Classifier

With the hope of finding a more suitable solution with the help of a large number of small decision trees, we ran a random forest ensemble learning algorithm in the same dataset. This time we achieved 0.78 for the balanced accuracy score and obtained the list of features by their prominence for prediction.

### Easy Ensemble AdaBoost Classifier
This last approach gave a better result with a 0.93 balanced accuracy score and 92% recall for high-risk loans.

<kbd><img src="https://github.com/ArmineKhanan/Credit_risk/blob/main/Images/Ensemble%20AdaBoost%20Classifier.png" width="800" /></kbd>


## Summary
Because of unbalanced data, we had to implement several resampled techniques before running statistical models which would classify the loans as 'good' or 'bad.'  First, we tried out the logistic regression model for data resampled in different ways. After failing to achieve satisfying results, we turned to ensemble learning algorithms. Easy Ensemble AdaBoost Classifier has been proven to be the best out of all models we implemented.
