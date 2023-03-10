# Credit_Risk_Analysis

## Overview 
The purpose of this analysis is to help the client to decifer what and who can be considered for good loans versus risky loans; the dataset chosen for this endeavor is a credit card dataset from LendingClub. This analysis will be utilizing machine-learning models from imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling to predict credit risk. 

## Results 
For thoroughness 6 different machine learning models have been used to predict the credit risk.

**1.) RandomOverSample (Oversampling Resampling Model)**

The accuracy of the naive random oversampling model is 66.7% accurate with the precision being 11% and sensitivity being 71% for determining if the applicants are in the high risk loan category. While the low risk category the precision is about 100% and recall is 62%. This means that overall this model is very sensitive to low risk loans, but not very precise for determining high risk loans.

![1_CM](https://github.com/vanessaneang/Credit_Risk_Analysis/blob/main/Resources/1_CM.png)

**2.) SMOTE (Oversampling Resampling Model)**

The accuracy of prediction for the SMOTE oversampling model is 64%. For high risk loans the precision of predictions is about the same as the previous being 10% while the recall is 61%. Low risk loans have a higher precision and recall being 100% and 67% respectively. While this model does predict the low risk loans more preciscely it is not as accurate as the Naive Random Oversampling model.
![2_CM](https://github.com/vanessaneang/Credit_Risk_Analysis/blob/main/Resources/2_CM.png)

**3.) Cluster Centroids (Undersampling Resampling Model)**
This model was difficult for me to obtain, I was not able to run the code since I kept getting an error the table below is most likely using the same variables as the SMOTE resampling model. Thus this does not portray the undersampling model corrrectly.

![3_CM](https://github.com/vanessaneang/Credit_Risk_Analysis/blob/main/Resources/3_CM.png)

**4.) SMOTEENN (Combinatorial of Oversampling and Undersampling Model)**

The combination of overampling and undersampling with the SMOTEENN model gave an accuracy score of 64%. The recall rate for the high risk loans was greater than the previous models coming in at 75%, the precision remaining the same however at 10%. For the low risk loans the recall is less coming in at 57% and precision remaining constant at 100%. If we would like to determine high risk loans with a more sensitive model this model can do so, but the trade-off is having a less sensitive low risk loan.

![4_CM](https://github.com/vanessaneang/Credit_Risk_Analysis/blob/main/Resources/4_CM.png)


**5.) BalancedRandomForestClassifier (Ensemble Classifier)**

The accuracy score for Balanced Random Forest Classifier is 66.8%, which makes it more reliable to predict the credit risk than the other resampling models. The precision of the high risk loans is 88% while the recall is at 34%, but the low risk loans is 100% for both recall and precision. This makes this model best for identifying low risk loans precisely and with the highest amount of sensisitivity. 

![5_CM](https://github.com/vanessaneang/Credit_Risk_Analysis/blob/main/Resources/5_CM.png)

**6.) EasyEnsembleClassifier (Ensenble Classifier)**

This model has the highest accuracy score overall, with a 91.7% accuracy score. Both the high risk and low risk loans have a high recall rate; 89% for high risk and 94% for low risk. Overall this means this model can accurately find the true high risk and low risk loans with minimal false readings. 

![6_CM](https://github.com/vanessaneang/Credit_Risk_Analysis/blob/main/Resources/6_CM.png)


## Summary 
Overall most of the models had an accuracy score of 60% indicating that they can predict the credit risk at a moderate rate, but the main problem for many of the models is being sensitive to the high risk loans. This means that many lenders would give high risk loans to borrowers that should not be receiving these loans. If a less accurate model needs to be used than for low risk loans than the Naive Random Sampling should do, but if we need one that will be more sensitive for the high risk loans than it would be good to use the other ensemble classifier, the BalancedRandomForestClassifier.

In conclusion the EasyEnsembleClassifier seems to be the best predictor for both high and low risk loan, the accuracy score is 91.7% making it the most accurate machine learning model out of the six examined. The sensitivity for this model is high for both types of loans meaing that there is very minimal false readings. For the client it is better to have minimal false readings since it will reduce the amount of loans given to the wrong type of lenders. This will allow lenders to predict what type of borrowers to give out loans with minimal error of who will reveive high risk and low risk loans. 
