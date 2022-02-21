# Credit_Risk_Analysis
Help Jill use machine learning to predict credit risk for loan applicants.

## Overview of the analysis: 
Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. We will help Jill employ different techniques to train and evaluate models with unbalanced classes. We will use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, we will oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, we will use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, we will compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Finally, we will evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.

## Results: 

### Naive Random Oversampling

<img width="453" alt="image" src="https://user-images.githubusercontent.com/92613639/154870648-a5a519cb-1723-49fa-a2bf-e11ea731f074.png">

- Balanced Accuracy Score - 0.64
- Low Risk Precision - 1.00
- Low Risk Recall - 0.59
- High Risk Precision - 0.01
- High Rish Recall - 0.69
- Precision is high for low risk, but extremely low for high risk. Recall for both is low.

### SMOTE Oversampling

![image](https://user-images.githubusercontent.com/92613639/154870616-d2d53b69-83cb-46d6-b676-d2353b234b39.png)

- Balanced Accuracy Score - 0.66
- Low Risk Precision - 1.00
- Low Risk Recall - 0.69
- High Risk Precision - 0.01
- High Rish Recall - 0.63
- Precision again is high for low risk, but still extremely low for high risk. Recall for low risk increased, but recall for high risk decreased slightly.

### Undersampling

![image](https://user-images.githubusercontent.com/92613639/154870547-574fc3f8-5fa2-49e4-809f-bf1ffe4edd7c.png)

- Balanced Accuracy Score - 0.54
- Low Risk Precision - 1.00
- Low Risk Recall - 0.69
- High Risk Precision - 0.01
- High Rish Recall - 0.40
- As with the above, low risk precision is extremely high, with a decent recall. High Risk precision is still the same with and even lower recall.

### Combination (Over and Under) Sampling

<img width="448" alt="image" src="https://user-images.githubusercontent.com/92613639/154867252-6e68e442-d35d-480b-a94f-563238cdf182.png">

- Balanced Accuracy Score - 0.64
- Low Risk Precision - 1.00
- Low Risk Recall - 0.57
- High Risk Precision - 0.01
- High Rish Recall - 0.72
- With precision unchanged, this sampling method appears to produce the overall highest recall for high and low risk.

### Balanced Random Forest Classifier

<img width="457" alt="image" src="https://user-images.githubusercontent.com/92613639/154867196-17f1cf53-0757-4de9-83c0-947c808ce22b.png">

- Balanced Accuracy Score - 0.79
- Low Risk Precision - 1.00
- Low Risk Recall - 0.87
- High Risk Precision - 0.03
- High Rish Recall - 0.70
- This method has a higher high risk precision, and both low risk and high risk recall. The higher recalls indicate lower false negatives.

### Easy Ensemble AdaBoost Classifier

![image](https://user-images.githubusercontent.com/92613639/154866899-04c5f5bd-3c29-417d-b702-2ec9d83cc7e7.png)

- Balanced Accuracy Score - 0.93
- Low Risk Precision - 1.00
- Low Risk Recall - 0.94
- High Risk Precision - 0.09
- High Rish Recall - 0.92
- This method appears to be over fit with extrememly high balanced accuracy score.


## Summary: 
All of the above models have extremely high low risk precision, meaning they are very good at predicting a low credit risk is actually low risk. However, they all have extremely low high risk precision, meaning they are very bad at prediction high credit risk is actually high risk. In terms of a loan company, I think that it is more important to be able to accurately label high risk so that you are able to avoid it. The varying recall rates are okay, but being so low may not be acceptable to the lender as the potential downside could make the loan not worth it.

I would recommend none of these models, even the ones with higher recalls and balanced accuracy scores because those could be overfit. I would recommend looking at additional data to get to a model that has decently high precision for high risk as that is really what a lender should be able to identify.
