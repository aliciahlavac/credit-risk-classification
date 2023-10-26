# Module 12 Report Template

## Overview of the Analysis

* The purpose of this analysis is to develop a machine learning model that can predict credit risks for loans, specifically loans that are healthy (with a low risk of default) and high-risk loans (with a high risk of default). 
* The financial information included categories such as interest rate, the borrower's income, the debt to income ratio, the number of accounts a potential borrower has open, the total debt they have, and the if the potential borrower had any derogatory marks on their account (such as a late payment).  We wanted to look at the loan_status category, which tells us if the loan is healthy or is high-risk.  
* We can see that there is an imbalance in number of obsevations of healthy loans and high-risk loans, found when we ran value_counts.  We can see that healthy loans have 75,036 observations while high-risk loans have 2.500 observations.  This is important to know because it helps guide how we handle the data.
* The machine learning process I went through had the following stages:
  - Pre-processing where I read the data from a .csv file into a data frame
  - Training the model/Creating a logistic regregression model which then had the original data fit into the model
  - Used testing features to make predictions on testing labels with the fitted model
  - Finally, I evaluated how well the model performed by calculating statistics like balanced accuracy scores, confusion matrices, and classifiction reports.
* I used LogisticRegression on the original data that was fitted.  Then, I used the RandomOverSampler module to resample the data.  This was done to address the class imbalance we saw in the original fitted data.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Balanced accuracy score: The balanced accuracy score for this model is 95.2%, telling us that the model is doing a good job of distinguishing between healthy loan and high-risk loan classes. This number is especially important in this model because our two classes are imbalanced.
  
    ![2023-10-25](https://github.com/aliciahlavac/credit-risk-classification/assets/127240852/7c543080-4c2b-4225-b9ee-948e16ad4ee1)

  * Precision: When the model predicts the healthy loan class (class 0), it is almost always correct, with a precision score of 1.0. For the high-risk loans (class 1), when the model predicts this class it is right about 85% of the time.  
  * Recall: The model correctly identifies 99% of the actual healthy loans, and correctly identifies 91% of the actual high-risk loans.



* Machine Learning Model 2:
   * Balanced accuracy score: The balanced accuracy score for this model is 99.3%, telling us that the model is doing a great job of distinguishing between healthy loan and high-risk loan classes.
 
      ![2023-10-25 (2)](https://github.com/aliciahlavac/credit-risk-classification/assets/127240852/39bcc3bb-7aeb-42ad-ba65-8e0dd8550b4a)

  * Precision: When the model predicts the healthy loan class, it is almost always correct, with a precision score of 1. For the high-risk loans, when the model predicts this class it is right 84% of the time.  
  * Recall: The model correctly identifies 99% of the actual healthy loans, and correctly identifies 99% of the actual high-risk loans.

## Summary

* Using our analysis above, it seems that model 2 is the better model.  In using model 2, the recall for the high-risk loans was higher than in using model 1, meaning that model 2 is better at correctly identifying high-risk loans.  In addition, model 2 has a better balanced accuracy score, meaning this model does a better job at distinguishing between the two classes in the dataset.  In addition, model 1 had highly imbalanced classes, where model 2 dealt with this issue.  While it is true that model 1 had a higher precision for the high-risk loan class (meaning that it may produce fewer false positives), the trade-off between precision and recall isn't enough to sway in favor for model 1.  For those reasons, model 2 is better.  
* Performance definitely depends on the problem we are trying to solve.  We perhaps want to focus on predicting the high-risk loan class (the minority class), meaning we would want to minimize false negatives even if that means accepting more false positives.  It's also important to note that in credit risk assessment, it's often important to maximize precision (correctly identifying high-risk applicants), but at the same time maximize recall (and thus minimize the number of low-risk applicants classified as high risk applicants). In this case, the model is heavily dependent on the class you are trying to analyze and the problem you are trying to solve.  
