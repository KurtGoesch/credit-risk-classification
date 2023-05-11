# credit-risk-classification

# Module 12 Report

## Overview of the Analysis

* This analysis was intended to find a model that would accurately predict loan risk by identifying 'healthy' and 'high-risk' loans.
* To build the model we analyzed loan data from a financial institution. This data included information about the loan (loan amount and interest rate) as well as the borrower's information (income, debt-to-income ratio, number of accounts, etc.) and the rating of the loan defined as a binary with 0 being healthy and 1 being high-risk.
* Once the models were built we could compare the predicted results to the actual loan ratings from the original data. Using the value-counts function I broke down how many of the predictions were accurate or had been mis-predicted.
* I had split my data into training and test variables and used those to fit the model and then test the model for accuracy. Once tested I reviewed the balanced accuracy score, viewed the predictions in a confusion matrix, and finally ran a classification report.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1: Logistic Regression Model
  
  * Balanced Accuracy Score: 0.9520479254722232
  * Precision: 0: 1.00, 1: 0.85
  * Recall:    0: 0.99, 1: 0.91



* Machine Learning Model 2: Random Oversample Model

  * Balanced Accuracy Score: 0.9936781215845847
  * Precision: 0: 1.00, 1: 0.84
  * Recall:    0: 0.99, 1: 0.99

## Summary

* Based on these results it appears the Random Oversample Model is better for the predictions needed in this analysis. The balanced accuracy is over 99% vs just 95% for the Logistic Regression Model. While the precision and recall are the same for the 0 (healthy) loans in both models the ROS Model gives similar precision and improved recall for the 1 (high-risk) loans.
* If I was using this model for a real world financial institution I would be satisfied that we weren't going to be approving a large number of loans that would turn out to have really been high-risk. However it's possible the institution could be missing out on potential loan revenue by declining inaccurately predicted high-risk loans that should have been approved. If the goal is to minimize risk in the loan portfolio then this model should be fine, but if the goal is to maximize revenue then a model that better predicts the high-risk loans would need to be found.

