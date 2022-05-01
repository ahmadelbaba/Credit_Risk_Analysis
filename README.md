# Credit_Risk_Analysis

## Overview

We'll use and assess different Machine Learning models to help us Precit Credit Risk  based on a set of factors. Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore we will be employing different techniques to train and evaluate models with unbalanced classes.

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, we’ll oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, we’ll use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, we’ll compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk

## Results

### Balacened Accuracy Scores (Descending)
 
 -  Easy Ensemble AdaBoost Classifier  0.925427358175101
 -  Balanced Random Forest Classifier  0.7877672625306695
 -  Naive Random Oversampling          0.646602844334948
 -  SMOTEENN Over/Undersampling        0.6376117496807152
 -  SMOTE Oversampling                 0.6374415316001305
 -  ClusterCentroids Undersampling     0.5954832783397996

### Confusion Matrix by Model

 -  Easy Ensemble AdaBoost Classifier
 
    ![EEC](/images/EEC_CM.PNG)
 
 -  Balanced Random Forest Classifier
    
    ![BRFC](/images/BRFC_CM.PNG)
    
 -  Naive Random Oversampling  
    
    ![NRO](/images/NRO_CM.PNG)
    
 -  SMOTEENN Over/Undersampling
    
    ![SMOTEENN](/images/SMOTEENN_CM.PNG)
 
 -  SMOTE Oversampling
   
    ![SMOTE](/images/SMOTE_CM.PNG)
 
 -  ClusterCentroids Undersampling
    
    ![RUS](/images/RUS_CM.PNG)

### Imbalanced Classification Report

 -  Easy Ensemble AdaBoost Classifier
 
    ![EEC](/images/EEC_ICR.PNG)
 
 -  Balanced Random Forest Classifier
    
    ![BRFC](/images/BRFC_ICR.PNG)
    
 -  Naive Random Oversampling  
    
    ![NRO](/images/NRO_ICR.PNG)
    
 -  SMOTEENN Over/Undersampling
    
    ![SMOTEENN](/images/SMOTEENN_ICR.PNG)
 
 -  SMOTE Oversampling
   
    ![SMOTE](/images/SMOTE_ICR.PNG)
 
 -  ClusterCentroids Undersampling
    
    ![RUS](/images/RUS_ICR.PNG)
    
## Summary

### Balacened Accuracy Scores

Our two ensemble classifier models scored higher than out over/undersmapling models with accuracy scores of 92.5% for the AdaBoost Classifier and 78.77% for the Random Forest Classifier. The highest over/undersampling model (Naive Oversampling) had an accuracy score of 64.66%.

### Confusion Matrix and Inblanced Classifcation Reports

An accuracy score is not always an appropriate or a meaningful performance metric, however. So we look at Confusion matrices for more details and inbalanced classification reports. 

A quick scan of the matrices shoes that all models had high precision of detecting low risk and very low precision detecting high risk credit. Looking at recourse metrics, we ask knowing that a credit applicant is high risk, how likely is it that our model will predict it that they are? It appears that our Easy Ensemble AdaBoost Classifier did the best job at that with a 91% recall score. The model was also good at predicting low risk profiles with a 94% recall score. SMOTEENN was the second in line in terms of recall score for high risk candidates at 70%. Finally it's also worth mentioning Balanced Random Forest Classifier's low risk recall score at 91%.

### Recommendation

While the AdaBoost Classifier performed the best amongst the group its ability to predict high risk is still very low (7%). The model is sensitive enough (94% and 91% recall scores) but not precise enough. And this is made more apparent by the low f1 score of 14%. Even our best model didn't perform well enough, so we couldn't really recommend it. Our recomendation would be to test more data. 

