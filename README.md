# Credit Risk Analysis

## Overview
- In this project we will be diving into supervised machine learning to try predict credit card risk.<br>To do this, we will be going through different models and approaches such as:
    1. Oversample data using RandomOverSampler and SMOTE
    2. Undersample data using ClusterCentroids
    3. Combine approach of over and undersampling with SMOTEENN
    4. Compare two machine learning models that reduce bias BalancedRandomForestClassifier and EasyEnsembleClassifier

## Results
### Naive Random Oversampling
![naive_oversample](/resources/nro.png)
1. Accuracy Score: 65.33%
2. Precision High Risk: 1%
3. Precision Low Risk: 100%
4. Recall High Risk: 65%
5. Recall Low Risk: 66%