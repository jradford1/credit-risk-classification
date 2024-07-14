# credit-risk-classification

## Overview of the Analysis
The purpose of this analysis is to predict from the given dataset whether or not a person(s) is likely to default on their loan. 
Data provided was: loan_size,interest_rate,borrower_income,debt_to_income,num_of_accounts,derogatory_marks,total_debt and loan_status. These markers were used to train, test and predict whether or not a loan is likely to default (loan_status). 

As this final data of loan_status is categorical ("yes" or "no", 0 or 1, etc) the best model to use is the logistic regression model which takes the Sigmoid function, which is a much more accurate model than linear regression.

## Results
Results were accurate using the logistic regression model with the following results for the clasification report:

Classification Report
              precision    recall  f1-score   support

           0       1.00      0.99      1.00     18765
           1       0.85      0.95      0.89       619

    accuracy                           0.99     19384
   macro avg       0.92      0.97      0.94     19384
weighted avg       0.99      0.99      0.99     19384

The precision value is 1 (100%) for 0 (The loan is healthy) and 0.85 (85%) for 1 (the loan is likely to default). Recall is also very close to 1 (100%) in both cases. This then leads to a good score for F1 which takes into account both precision and recall.

The recall value un this situation should be considered with more weight. The possible worst case scenario for this situation is if a prediction occurs where a person is unlikely to default on their loan, when in actual fact they are likely to default. This increases financial risk to the lender. 

 To conclude the prediction, the .score function was used to give an accuracy of the model which returned 0.9927, further adding weight to the models accuracy.

## Summary
Logistic regression model in this instance returns positive results for predictions with the lowest value of 0.85 for precision for a loan likely to default and 1 for predictions on whether a loan is safe. 

There is an imbalance between the classes which needs to be noted with majority of instances being 0 (healthy loan) with 18658 cases compared to 619. Despite this imbalance, the model performs well shown by the weighted average value of 0.99 which combines all metrics (precision, recall and F1).

However, it is more important to predict the 1's where a loan is likely to default. Given the data is categorical, it is likely the best model is the linear regression. Some improvements may want to be considered here to increase this 0.85 value for the minority class. 