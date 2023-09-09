# credit-risk-classification
Using machine learning to predict the risk of default of loans

## Overview of the Analysis

In this repository we analyzed financial information on whether a loan was considered a healthy loan (where the borrower would pay back the loan) or a high-risk loan (where the borrower might default). This can be used to help determine whether or not a loan at a bank is able to be given with confidence that the borrower will pay back the loan.
The process we used to analyze the data is supervised machine learning. We started by identifying what our target category was, then splitting the data into features and the target category. We then split the data into training and testing data using sklearn's train_test_split ability. Fitting a logisic regression model to the data, we generated testing predicitons of the data, using reports such as balanced_accuracy_score and confusion_matrix to determine how well the machine learning performe in evaluating whether a loan is healthy or high-risk.

## Results
*Machine Learning Model 1 (without oversampled data):

** Balanced accuracy score: 0.94427
** Precision and recall (healthy loan): 1.00 and 1.00
** Precision and recall (high-risk loan): 0.87 and 0.89
** The precision and recall of the healthy loans were spectacular, and the precision and recall of the high-risk loans were also very good.

*Machine Learning Model 2 (with oversampled data):

** Balanced accuracy score: 0.94453
** Precision and recall (healthy loan): 0.90 and 0.99
** Precision and recall (high-risk loan): 0.99 and 0.89
** The precision of the healthy loans drops off in this data set, though the precision of the high-risk loans increased dramatically, so there is tradeoff between the two. Both are still near or over 90% accuracy, which would be incredible in a real world data set.

## Summary
Both models seem to perform nearly the same (as determined by their high accuracy scores). As far as which model to recommend, it depends: if you are trying to determine whether a loan is healthy, I would use the first model, however, if you are trying to determine whether a loan is high-risk (which is more likely for banks and lenders) I would recommend the second model, as there is not only more data but a lower risk of false positives and negatives with the second data set. Not to say that there isn't a tradeoff between the two, but those are my recommendations.
