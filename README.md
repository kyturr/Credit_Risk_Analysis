# Credit_Risk_Analysis

## Overview of Analysis

The purpose of this projet is to create machine learning models that can predict whether a loan application is low risk or high risk based on various other application variables. From this data set we are able to use 86 columns of data and indicators in order to train each machine learning model and test the preditions versus a testing portion of the data. One problem with the data set is that there is a large class imbalance between low risk and high risk loan applications. Low risk applications outnumber high risk appications 68470 to 347. This will afect the preceision and recall of the machine learning algorithms.

## Results
### Individual results
* Naive Randome Oversampling had an accuracy score 64.39%. For low risk, it had an precision of 1.00 and recall of 0.58, resulting in an F1 of 0.73 while high risk had a precision of 0.01 and recall of 0.71 resulting in an F1 of 0.02.
* SMOTE Oversampling had an accuracy score 65.86%. For low risk, it had an precision of 1.00 and recall of 0.68 resulting in an F1 of 0.81 while high risk had a precision of 0.01 and recall of 0.63 resulting in an F1 of 0.02.
* Tandom undersampling had an accuracy score 60.19%. For low risk, it had an precision of 1.00 and recall of 0.52 resulting in an F1 of 0.68 while high risk had a precision of 0.01 and recall of 0.68 resulting in an F1 of 0.02.
* SMOTEEN combined sampling had an accuracy score 64.80%. For low risk, it had an precision of 1.00 and recall of 0.57 resulting in an F1 of 0.73 while high risk had a precision of 0.01 and recall of 0.72 resulting in an F1 of 0.02.
* Balannced Random Forest Classifier had an accuracy score 82.82%. For low risk, it had an precision of 1.00 and recall of 0.92 resulting in an F1 of 0.96 while high risk had a precision of 0.05 and recall of 0.74 resulting in an F1 of 0.08.
* Easy Ensemble AdaBoost Classifier had an accuracy score 92.54%. For low risk, it had an precision of 1.00 and recall of 0.94 resulting in an F1 of 0.97 while high risk had a precision of 0.07 and recall of 0.91 resulting in an F1 of 0.14.
### Combined Results
![image](https://user-images.githubusercontent.com/103979048/199362027-f31d1b68-9539-4cad-ae3c-35928aa5fa19.png)
![image](https://user-images.githubusercontent.com/103979048/199362048-8f0b74d8-58b4-4c76-8754-d7777c52d923.png)
![image](https://user-images.githubusercontent.com/103979048/199362068-c392a09b-444d-4de7-95a0-fa938dd79a87.png)

## Summary
Machine learning can be a useful tool to classify data using various features to predict the outcome. However, each MLM will deal with different obstacles in their own unique ways. In this data set there was a large class imbalance that the MLMs had to deal with. In terms of accuracy, the Easy Ensemble AdaBoost Classifier performed best with an accuracy of 92.54%. This is especially evident in the confusion matrix where it had the least false positives (979) and least false negatives (8) in comparison to the other MLMs confusion matrices. This means it only let 8 high risk applications pass through as low risk and only denied 979 low risk applications as high risk. While these numbers seem large in comparison to the other confusion matrices they are relatively small. When taking into account the classsification report, the Easy Ensemble AdaBoost Classifier also performs best. Therefore, this model is recommended for use in this data set. The precision for classifying high risk applications could use some improvement but given the class imbalance and the implication of consequences it is acceptable to have that low precession as the recall is very high at 0.91.
