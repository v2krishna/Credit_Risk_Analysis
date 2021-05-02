# # Credit_Risk_Analysis

## Purpose:
The purpose of this use case is to evaluate different models to predict default of the payments which indirectly affects credit risk, used oversampling (randomoversampler & SMOTE), undersampling ( ClusterCentroids) and SMOTEENN alogrithms for combination of both oversampling and undersampling. Along with that we used RandomForest and EasyEnsmeble Classifier.

we can compare different models by comparing their accuracy scores and classification reports.

## Resources:
1. Data Source : LoanStatus_2019_Q1.csv
2. Python 3.7.9. Anaconda Navigator, Jupyter Notebook


## Results 

### OverSampling Model Results:

#### RandomOverSample Model:
 ![randomoversampleaccuracyscore](/images/01_randomoversample_acc_score.PNG) 
 ![randomversample-confusionmatrix-classificationreport](/images/02_randomoversampling_confusionMatrix.PNG)
 <br/>
 1. Balanced Accuracy Score is 66%
 1. High Risk Precision is around 1% which is very less 
 1. The Low Risk Precision is 100% which is way high to believe the accuracy and we can confirm its been biased on the dataset.
This technique to predict the accuracy is not much helpful because of the predict is baised on the data patterns.

### SMOTE Model Results:

 ![smote-accuracyscore](/images/03_smote_acc_score.PNG) 
 ![smote-confusionmatrix-classificationreport](/images/04_smote_confusionMatrix.PNG)
 <br/>
 1. Balanced Accuracy Score is 65%
 1. High Risk Precision is around 1% which is very less 
 1. The Low Risk Precision is 100% which is way high to believe the accuracy and we can confirm its been biased on the dataset.
 1. Recall or Sensitvitiy of High Risk and Low Risk is almost around 65 % which.

This technique to predict the accuracy is not much helpful because High-risk is same as oversampling.

### UnderSampling Model Results:

#### ClusterCentroids
 ![undersampling-accuracyscore](/images/05_undersampling_acc_score.PNG) 
 ![undersampling-confusionmatrix-classificationreport](/images/06_undersampling_confusionMatrix.PNG)
 <br/>
 1. Balanced Accuracy Score is 54%
 1. High Risk Precision is around 1% which is very less 
 1. The Low Risk Precision is 100% which is way high to believe the accuracy and we can confirm its been biased on the dataset.
 1. Recall or Sensitvitiy of low Risk is almost around 40 % which is very less to use.

This technique to predict the accuracy is not much helpful because Low-risk recall is very less which and also on high-risk also might not be accurate as we might have reduced less data in this sample.


### Combination Model (Over Sampling and Under Sampling) Results:

#### SMOTEENN
 ![SMOTEENN-accuracyscore-cm-classificationreport](/images/07_combo_all.PNG) 
 
 1. Balanced Accuracy Score is 54%.
 1. High Risk Precision is around 1% which is very less.
 1. The Low Risk Precision is 100% which is way high to believe the accuracy and we can confirm its been biased on the dataset.
 1. Recall or Sensitvitiy of low Risk is almost around 57 % which is very less to use.

This technique to predict the accuracy is not much helpful because Low-risk recall is very less but where as the high risk recall is around 70 % which helps to predict the default is around 70%.

### BalancedRandomForestClassifier model
![RandomForestClassifier-accuracyscore-cm-classificationreport](/images/08_RandomForest_results.PNG) 

 1. Balanced Accuracy Score is 78%.
 1. High Risk Precision is around 3% which is very less.
 1. The recall or sensitivity is almost high for both Low Risk and High-Risk, but is the  recall is higher than the low risk then it will be much helpful to use this model.
<br/>
Sorted Features which are highly affecting the Defaulting the payments.
![RandomForestClassifier-sortedfeatures](/images/09_sorted_features.PNG)
Based on the above results, we can say total_rec_prncp feature is highly effecting the results, followed by total_payment features.

### BalancedRandomForestClassifier model
![EasyEnsembleClassifier-accuracyscore-cm-classificationreport](/images/10_esayEnsemble.PNG) 

 1. Balanced Accuracy Score is 93%.
 1. High Risk Precision is around 9% which is still very less but to other models the value is little higher.
 1. The recall or sensitivity is almost 92% for both Low Risk and High-Risk , with this we can atleast use this model to predict the status correctly.
 
## Summary
All the above mentioned models to perform the credit risk has very weak precision which will not help in predicting the credit risk is high or not.
Out of all the models used EasyEnsemble model has more accuracy score and the recall or sensitivity of both high risk and low risk is also very high.
Even though the recall or sensitivity are high, precision is 9% which is very less for predicting high risk , because of this reason cannot completely use this model to predict the credit risk.
