## Module 12. Report

## Overview of the Analysis
The main purpose of the analysis is to identify loan risk using Logistic Regression, a Supervised Machine Learning. 
The set of data that was used on the analysis had the following variables: `loan_size, interest_rate, borrower_income, debt_to_income, num_of_accounts, derogatory_marks, total_debt, loan_status`

To proceed with the regression, I used the labels 0 (healthy loan) and 1 (high-risk loan) from the variable `loan_status` (y). The rest of the variables from the dataset were used as independent variables (X). 

The following process was followed up to get the desired results: 
1.	Read the data into a dataframe.
2.	Separate the labels and features. 
a.	Separate the `loan_status` variable to be the dependent variable (y).
b.	Save the rest of the variables in X.
3.	Split the data into training and testing datasets, using `train_test_split` function.
4.	Create a model based on the logistic regression method.
5.	Fit the model using training data.
6.	Save the training predictions into an object.
7.	Make predictions using features data X_test and save them into an object.
8.	Evaluate the model’s performance, generating a confusion matrix and printing the classification report.

Logistic Regression is a method used for predicting binary outcomes from data. Each observation receives a probability of being in category 1 of the outcome variable. If the probability of being in category 1 is over a threshold, then that observation is predicted to be a 1.

## Results
 
The model has an accuracy of 0.99, which means that the model classifies correctly 99% of the observations. Besides, the precision for `0` (healthy loan) and `1` (high-risk loan) are 1 and 0.87, respectively, which also means that the model has a low false positive rate. 
Additionally, the recall measures show that the model has a low false negative rate, because the measures are 1 and 0.95, respectively for the `0` (healthy loan) and `1` (high-risk loan) labels.

![image](https://github.com/user-attachments/assets/82c5c1d0-9677-44ff-b14a-a8145d2317f8)

The confusion matrix shows the following:

|         | Predicted 0 | Predicted 1     |
|---------|-------------|-----------------|
|Actual 0 | 18,673      |   86            |
|Actual 1 |   32        |       593       |


## Conclusions
In short, the model has a low rate of false positives and false negative. Because it wants to identify the probability of high-risk loan observation, I reckon that this model could be enough to predict that within the data with the features that were used in the model. However, it could have ethical implications if there were correlations between income and other social variables such as ethnical origin. Because of that, I would suggest using the model with the correct warnings.
