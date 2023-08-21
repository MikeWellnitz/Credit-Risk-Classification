# Credit-Risk-Classification Assignment

## Overview of the Analysis

The purpose of this analysis is to use bank loan data and modeling to predict the accuracy of the statuses of those loans. 

Data provided for this analysis was a CSV file containing over 77,500 different loans. The models being used against this information are to check the accuracy of the "loan_status" label being either 0 (Healthy Loan) or 1 (High-Risk Loan). We would like to predict the accuracy of a logistic regression model in determining that "loan_status" (variable "y"). The rest of the dataframe information was contained in variable "X", and together, "X" and "y" were used for training and testing the model.  

After reading in the CSV and creating the "lending_df" dataframe, it was determined how many loans we were looking at using "value_counts" and then creating the variables mentioned above. The "train_test_learn" module from SciKitLearn was imported to split the data between testing and training. After another SciKitLearn import was done for LogicRegression, the model was "fit" for training and assiged to the "lr_model" variable. Finally, in comparison with the testing data, the fitted model was used to make predictions to see how accurate it was in getting the accurate "loan_status". This resulted in a 94.4% balanced accuracy score. 

The starter code for this assignment indicated trying to use RandomOverSampler to see predictions using that method. While that section was not required for this Module assignment for grading (based off of the BCS Requirements), I also attempted to create a model using RandomOverSampler, and the predictions/results seem to indicate better validity that the data is pretty good for both the "0-Healthy Loans" and the "1-High-Risk" loans based on the 99.6% balanced accuracy score. 


## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1: Linear Regression
  * This model resulted in a 94.4% balanced accuracy score. Regarding the "Healthy Loans" (0), the model's precision and recall scores show it did a perfect job of both predicting this "loan_status" and also everything else. However, regarding the "High-Risk Loans" (1), this model demonstrated less accuracy as it's precision for predicting the correct "loan_status" was only 87% and when recalling the items we did not predict, it returned an 89% success rate. 
     
* Machine Learning Model 2: RandomOverSampler
  * This model resulted in a 99.6% balanced accuracy score. Regarding the "Healthy Loans" (0), the model's precision and recall scores also show that it did a perfect job of both predicting this "loan_status" and also everything else. Regarding the "High-Risk Loans" (1), this model demonstrated the same precision (87%) as the prior model, but the recall was an amazing 100%. 

## Summary

While not required, the Logistic Regression Model that used the RandomOverSampler for Resampled Training Data seems to be the better method based off its Balance Accuracy Score and metrics from it's Classification Report. Being that it is more imporant to predict the "High-Risk" (1) loans, Resampled model did also have the higher Recall numbers compared to the first model, making it a slightly better option. It would be great to boost the Precision score from both models to something higher than 87%.