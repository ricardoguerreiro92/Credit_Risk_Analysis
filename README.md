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
1. Balanced Accuracy Score: 65.33%
2. True Negative: 48, False Positive: 26
3. False Negative: 5,860 True Positive: 11,271
4. Precision High Risk: 1%
5. Precision Low Risk: 100%
6. Recall High Risk: 65%
7. Recall Low Risk: 66%

### SMOTE
![smote](/resources/smote.png)
1. Balanced Accuracy Score: 67.88%
2. True Negative: 50, False Positive: 24
3. False Negative: 5,449 True Positive: 11,682
4. Precision High Risk: 1%
5. Precision Low Risk: 100%
6. Recall High Risk: 68%
7. Recall Low Risk: 68%

### Cluster Centroids
![cc](/resources/clustercentroids.png)
1. Balanced Accuracy Score: 52.13%
2. True Negative: 45, False Positive: 29
3. False Negative: 9,688 True Positive: 7,443
4. Precision High Risk: 0%
5. Precision Low Risk: 100%
6. Recall High Risk: 61%
7. Recall Low Risk: 43%

### SMOTEENN
![smoteenn](/resources/smoteenn.png)
1. Balanced Accuracy Score: 67.86%
2. True Negative: 58, False Positive: 16
3. False Negative: 7,309 True Positive: 9,822
4. Precision High Risk: 1%
5. Precision Low Risk: 100%
6. Recall High Risk: 78%
7. Recall Low Risk: 57%

### Balanced Random Forest Classifier
![brfc](/resources/balanced_random_forest_classifier.png)
1. Balanced Accuracy Score: 76.65%
2. True Negative: 47, False Positive: 27
3. False Negative: 1,750 True Positive: 15,381
4. Precision High Risk: 3%
5. Precision Low Risk: 100%
6. Recall High Risk: 64%
7. Recall Low Risk: 90%

### Easy Ensemble AdaBoost Classifier
![eeac](/resources/easy_ensemble_adaboost_classifier.png)
1. Balanced Accuracy Score: 93.00%
2. True Negative: 68, False Positive: 6
3. False Negative: 1,008 True Positive: 16,123
4. Precision High Risk: 6%
5. Precision Low Risk: 100%
6. Recall High Risk: 92%
7. Recall Low Risk: 94%

## Summary
We want our analysis to try and predict if a loan/credit is high risk or not so we performed a few tests with different supervised machine learning models to see which one would be a good one for future predictions.<br>In summary the models we tested performed as such:
    - Naive Random Oversampling - Balanced Accuracy Score: 65.33% / Recall High Risk: 65%
    - SMOTE - Balanced Accuracy Score: 67.88% / Recall High Risk: 68%
    - Cluster Centroids - Balanced Accuracy Score: 52.13% / Recall High Risk: 61%
    - SMOTEENN - Balanced Accuracy Score: 67.86% / Recall High Risk: 78%
    - Balanced Random Forest Classifier - Balanced Accuracy Score: 76.65% / Recall High Risk: 64%
    - Easy Ensemble AdaBoost Classifier - Balanced Accuracy Score: 93.00% / Recall High Risk: 92%

Being able to have a good prediction score on high risk credits is one of the most important things for a bank/lender. If we want a model to not allow as many high risk credits to pass through we need to check the recall rate for the high risk.<br>As you can see the top recall is Easy Ensemble AdaBoost Classifier with 92% score.<br>It is also important if we can dive a little deeper and also get a model that sucessfully predict low risk credits that pass as high risk, for this we will need the recall rate for the low risk. Retrieving the recalls for low risk credits we see that two of the models shine in this matter, Balanced Random Fores Classifier with a 90% recall Low risk and Easy Ensemble AdaBoost Classifier with a 94%.

#### Balanced Accuracy Score
Furthermore we can check the balanced accuracy score to have a general idea on how well the model performs over others. When checking this we see Easy Ensemble AdaBoost Classifier with a 93% balanced accuracy score. With everything from balanced accuracy scires to recall rates I can confidently say that Easy Ensemble AdaBoost Classifier performs with stunning 90+% numbers which is a very good prediction rate!
