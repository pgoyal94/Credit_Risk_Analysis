# Credit_Risk_Analysis
Help Jill use machine learning to predict credit risk for loan applicants.

## Overview of the analysis: 
Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. We will help Jill employ different techniques to train and evaluate models with unbalanced classes. We will use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, we will oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, we will use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, we will compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Finally, we will evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.

## Results: 

### Naive Random Oversampling
- Balanced Accuracy Score - 0.93
- Low Risk Precision - 
- Low Risk Recall - 
- High Risk Precision - 
- High Rish Recall - 
### SMOTE Oversampling
- Balanced Accuracy Score - 0.93
- Low Risk Precision - 
- Low Risk Recall - 
- High Risk Precision - 
- High Rish Recall - 
### Undersampling
- Balanced Accuracy Score - 0.93
- Low Risk Precision - 
- Low Risk Recall - 
- High Risk Precision - 
- High Rish Recall - 
### Combination (Over and Under) Sampling

<img width="448" alt="image" src="https://user-images.githubusercontent.com/92613639/154867252-6e68e442-d35d-480b-a94f-563238cdf182.png">

- Balanced Accuracy Score - 0.93
- Low Risk Precision - 
- Low Risk Recall - 
- High Risk Precision - 
- High Rish Recall - 
### Balanced Random Forest Classifier

<img width="457" alt="image" src="https://user-images.githubusercontent.com/92613639/154867196-17f1cf53-0757-4de9-83c0-947c808ce22b.png">

- Balanced Accuracy Score - 0.79
- Low Risk Precision - 1.00
- Low Risk Recall - 0.87
- High Risk Precision - 0.03
- High Rish Recall - 0.70
### Easy Ensemble AdaBoost Classifier

![image](https://user-images.githubusercontent.com/92613639/154866899-04c5f5bd-3c29-417d-b702-2ec9d83cc7e7.png)

- Balanced Accuracy Score - 0.93
- Low Risk Precision - 1.00
- Low Risk Recall - 0.94
- High Risk Precision - 0.09
- High Rish Recall - 0.92

## Summary: 


Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. If you do not recommend any of the models, justify your reasoning.

There is a summary of the results (2 pt)
There is a recommendation on which model to use, or there is no recommendation with a justification (3 pt)
