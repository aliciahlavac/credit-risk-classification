# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* The purpose of this analysis is to develop a machine learning model that can predict credit risks for loans, specifically loans that are healthy (with a low risk of default) and high-risk loans (with a high risk of default). 
* The financial information included categories such as interest rate, the borrower's income, the debt to income ratio, the number of accounts a potential borrower has open, the total debt they have, and the if the potential borrower had any derogatory marks on their account (such as a late payment).  We wanted to look at the loan_status category, which tells us if the loan is healthy or is high-risk.  
* We can see that there is an imbalance in number of obsevations of healthy loans and high-risk loans, found when we ran value_counts.  We can see that healthy loans have 75,036 observations while high-risk loans have 2.500 observations.  
* The machine learning process I went through had the following stages:
  - Pre-processing where I read the data from a .csv file into a data frame
  - Training the model/Creating a logistic regregression model which then had the original data fit into the model
  - Used testing feature data to make predictions on testing data labels using the fitted model
  - Finally, I evaluated how well the model performed by calculating statistics like balanced accuracy scores, confusion matrices, and classifiction reports.
* I used LogisticRegression on the original data that was fitted.  Then, I used the RandomOverSampler module to resample the data.  This was done to address the class imbalance we saw in the original fitted data.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.



* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.
