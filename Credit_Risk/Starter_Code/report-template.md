# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
A= The purpose of the analysis is to build and evaluate a machine learning model that can predict the risk level of loans, specifically identifying high-risk loans. This helps financial institutions make informed decisions about lending, ensuring they can minimize financial risk by accurately classifying loans as either healthy (low-risk) or high-risk.

* Explain what financial information the data was on, and what you needed to predict.
A= The data contains financial information about loans, including features like loan amount, borrower income, credit history, and other related factors. The goal was to predict whether a loan is "healthy" (low-risk) or "high-risk" based on these features, helping lenders identify potential risks before approving loans.

* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
A= he variable we are trying to predict is the loan status or credit risk label, which has two classes:

0: Healthy loan (low-risk)
1: High-risk loan
Here’s an example of how you could get the basic information about the target variable using value_counts:

# Get value counts for the target variable
y.value_counts()

0    15001
1      507

This shows that there are 15,001 healthy loans (label 0) and 507 high-risk loans (label 1).

* Describe the stages of the machine learning process you went through as part of this analysis.

A= 1.Data Preprocessing: Cleaned and prepared the data (handled missing values, encoded categories, scaled features).
2.Data Splitting: Split the data into training and testing sets.
3.Model Selection: Chose Logistic Regression for binary classification.
4.Model Training: Trained the model on the training data.
5.Prediction: Made predictions using the test data.
6.Model Evaluation: Evaluated the model's performance using accuracy, precision, recall, and the confusion matrix.
7.Analysis: Analyzed the results to assess model performance.

* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any other algorithms).
A= I used the Logistic Regression algorithm, which is commonly used for binary classification tasks. It models the relationship between input features and the probability of a certain class (in this case, predicting whether a loan is healthy or high-risk). This method was chosen for its simplicity, interpretability, and effectiveness in binary classification problems.

## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.
A= Logistic Regression Model:
Accuracy: 99%
Precision for Class 0 (Healthy Loan): 1.00
Recall for Class 0 (Healthy Loan): 0.99
Precision for Class 1 (High-Risk Loan): 0.86
Recall for Class 1 (High-Risk Loan): 0.94
This is based on the evaluation of the logistic regression model's performance. Let me know if you need details on any other models!

* Machine Learning Model 1:
    * Description of Model 1 Accuracy, Precision, and Recall scores.
    A= Accuracy: 99% (correctly predicted 99% of loans)
Precision for Class 0 (Healthy Loan): 1.00 (perfect precision)
Recall for Class 0 (Healthy Loan): 0.99 (correctly identified 99% of healthy loans)
Precision for Class 1 (High-Risk Loan): 0.86 (some false positives)
Recall for Class 1 (High-Risk Loan): 0.94 (identified 94% of high-risk loans)
This describes the performance of the Logistic Regression model.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.

ANSWER FOR THE ABOVE: 

Logistic Regression performs very well with 99% accuracy. It has perfect precision for healthy loans and good recall for high-risk loans, though precision for high-risk loans is a bit lower at 0.86.

Recommendation: I recommend using Logistic Regression because it accurately predicts both healthy and high-risk loans. The slightly lower precision for high-risk loans is acceptable, as high recall (94%) for these loans is more important to minimize financial risk.
