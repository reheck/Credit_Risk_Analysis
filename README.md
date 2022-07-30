# Credit_Risk_Analysis
## Overview
### The purpose of this analysis was to determine if there is a suitable supervised machine learning model that can best predict the risk for a lending agency to provide a loan to a certain person/business. Using a credit card dataset from LendingClub different techniques were used to train and evaluate models with unbalanced classes. The results of the models were evaluated and suggestions for use provided.
## Results
### Oversampling
#### >>> Naive Random Oversampling

![image](https://user-images.githubusercontent.com/102757676/181925871-233153ff-49b8-4f46-9391-488ff2347639.png)

#### ~ balanced accuracy score is approximately 0.66 which means the model is correct only 66% percent of the time
#### ~ precision score is 0.01 for predicting high-risk loans which means there is only a 1% chance the prediction of a high-risk loan is in reality a high-risk loan; precision score is 1.00 for predicting low-risk loans which means there is a 100% chance the prediction of a low-risk loan is in reality a low risk loan
#### ~ recall score is 0.71 for high-risk loans which means the model is correct in predicting a high-risk loan only 71 out of every 100 loans that are actually high risk; recall score is 0.60 for low-risk loans which means the model is correct in predicting a low-risk loan only 60 out of every 100 loans that are actually low-risk

#### >>> SMOTE Oversampling

![image](https://user-images.githubusercontent.com/102757676/181933766-399dca05-56c3-460a-b9da-646ef10421c4.png)

#### ~ balanced accuracy score is approximately 0.66 which means the model is correct only 66% percent of the time
#### ~ precision score is 0.01 for predicting high-risk loans which means there is only a 1% chance the prediction of a high-risk loan is in reality a high-risk loan; precision score is 1.00 for predicting low-risk loans which means there is a 100% chance the prediction of a low-risk loan is in reality a low risk loan
#### ~ recall score is 0.63 for high-risk loans which means the model is correct in predicting a high-risk loan only 63 out of every 100 loans that are actually high risk; recall score is 0.69 for low-risk loans which means the model is correct in predicting a low-risk loan only 69 out of every 100 loans that are actually low-risk

### Undersampling

![image](https://user-images.githubusercontent.com/102757676/181933837-548dfc51-2a75-419f-8a0d-60e12c0b9257.png)

#### ~ balanced accuracy score is approximately 0.54 which means the model is correct only 54% percent of the time
#### ~ precision score is 0.01 for predicting high-risk loans which means there is only a 1% chance the prediction of a high-risk loan is in reality a high-risk loan; precision score is 1.00 for predicting low-risk loans which means there is a 100% chance the prediction of a low-risk loan is in reality a low risk loan
#### ~ recall score is 0.69 for high-risk loans which means the model is correct in predicting a high-risk loan only 69 out of every 100 loans that are actually high risk; recall score is 0.40 for low-risk loans which means the model is correct in predicting a low-risk loan only 40 out of every 100 loans that are actually low-risk

### Combination Over and Under Sampling
#### SMOTEENN

![image](https://user-images.githubusercontent.com/102757676/181933902-dbaf7d01-5d6e-4aee-93ad-991f4fc61409.png)

#### ~ balanced accuracy score is approximately 0.64 which means the model is correct only 64% percent of the time
#### ~ precision score is 0.01 for predicting high-risk loans which means there is only a 1% chance the prediction of a high-risk loan is in reality a high-risk loan; precision score is 1.00 for predicting low-risk loans which means there is a 100% chance the prediction of a low-risk loan is in reality a low risk loan
#### ~ recall score is 0.72 for high-risk loans which means the model is correct in predicting a high-risk loan only 72 out of every 100 loans that are actually high risk; recall score is 0.57 for low-risk loans which means the model is correct in predicting a low-risk loan only 57 out of every 100 loans that are actually low-risk

### Ensemble Learners

#### >>> Balanced Random Forest Classifier

![image](https://user-images.githubusercontent.com/102757676/181933952-c7d58b06-833c-495f-9805-8916f494fa2f.png)

#### ~ balanced accuracy score is approximately 0.79 which means the model is correct only 79% percent of the time
#### ~ precision score is 0.03 for predicting high-risk loans which means there is only a 3% chance the prediction of a high-risk loan is in reality a high-risk loan; precision score is 1.00 for predicting low-risk loans which means there is a 100% chance the prediction of a low-risk loan is in reality a low risk loan
#### ~ recall score is 0.70 for high-risk loans which means the model is correct in predicting a high-risk loan only 70 out of every 100 loans that are actually high risk; recall score is 0.87 for low-risk loans which means the model is correct in predicting a low-risk loan only 87 out of every 100 loans that are actually low-risk

#### >>> Easy Ensemble AdaBoost Classifier

![image](https://user-images.githubusercontent.com/102757676/181934020-6de597fa-1227-4da4-871f-c4964aba3e13.png)

#### ~ balanced accuracy score is approximately 0.93 which means the model is correct 93% percent of the time
#### ~ precision score is 0.09 for predicting high-risk loans which means there is only a 9% chance the prediction of a high-risk loan is in reality a high-risk loan; precision score is 1.00 for predicting low-risk loans which means there is a 100% chance the prediction of a low-risk loan is in reality a low risk loan
#### ~ recall score is 0.92 for high-risk loans which means the model is correct in predicting a high-risk loan 92 out of every 100 loans that are actually high risk; recall score is 0.94 for low-risk loans which means the model is correct in predicting a low-risk loan 94 out of every 100 loans that are actually low-risk

## Summary

### The Oversampling and Undersampling models had lower accuracy and recall scores than the Ensemble Learners models. All models had extremely similar precision results with a score of 1.00 for the low-risk category for all. Though both Ensemble Learners models performed well, the best model to use for predicting credit risk is the Easy Ensemble AdaBoost Classifier. The Easy Ensemble AdaBoost Classifier had a 93% accuracy score, a 92% recall score for high-risk loans, and a 94% recall score for low-risk loans. The precision score for low-risk loans is 100%. Overall, the Easy Ensemble AdaBoost Classifier has the best chance of consistently predicting which loans are high-risk and which loans are low-risk. 
