# Credit-Risk-Classification Assignment

## Overview of the Analysis

The purpose of this analysis was to use bank loan data and modeling to predict the accuracy of the statuses of those loans. 

Data provided for this analysis was a CSV file containing over 77,500 different loans. Fromo this information, we are basing our models on each of those loan's "loan_status" of either 0 (Healthy Loan) or 1 (High-Risk Loan). We would like to predict the accuracy of a logistic regression model in determining that "loan_status" (variable "y"). The rest of the dataframe information was contained in variable "X", and together, "X" and "y" were used for training and testing the model.  

After reading in the CSV and creating "lending_df" dataframe, it was determined how many loans we were looking at using "value_counts" and then creating the variables mentioned above. The "train_test_learn" module from SciKitLearn was imported to split the data between testing and training. After another SciKitLearn import was done for LogicRegression, the model was "fit" for training and assiged to the "lr_model" variable. Finally, in comparison with the testing data, the fitted model was used to make predictions to see how accurate it was in getting the accurate "loan_status". This resulted in a 94.4% balanced accuracy score. 

The starter code for this assignment indicated trying to use RandomOverSampler to see predictions using that method. While that section was not required for this Module assignment for grading (based off of the BCS Requirements), I also attempted to create a model using RandomOverSampler, and the predictions/results seem to indicate better validity that the data is pretty good for both the "0-Healthy Loans" and the "1-High-Risk" loans based on the 99.6% balanced accuracy score. 


## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1: Linear Regression
  * This model resulted in a 94.4% balanced accuracy score. Regarding the "Healthy Loans" (0), the model's precision and recall scores show it did a perfect job of both predicting the correct "loan_status" and also everything else. However, regarding the "High-Risk Loans" (1), this model demonstrated less accuracy as it's precision for predicting the correct "loan_status" was only 87% and when recalling the items we did not predict, 
     
* Machine Learning Model 2: RandomOverSampler
  * Description of Model 2 Accuracy, Precision, and Recall scores.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.
