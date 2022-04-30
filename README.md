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
