# Credit_Risk_Analysis

## Overview of the loan prediction risk analysis:

The purpose of this analysis was to use supervised machine learning models to predict credit risk. Because credit risk is an inherently unbalanced classification problem, we employed undersampling, oversampling, and a combination of both with the goal of finding a model that will best predict credit risk. To oversample, we used the `RandomOverSampler` and `SMOTE` algorithms. For undersampling we used the `ClusterCentroids` algorithm. For our combinatorial approach of over and undersampling, we used the `SMOTEEN` algorithm. Finally, we used two ensemble algorithms: the `BalancedRandomForestClassifier` and the `EasyEnsembleClassifier`.

## Results:
The following is the balanced accuracy score and the precision/recall for determining high risk loans for each of the six models used.

- `RandomOverSampler` results:
    - Balanced accuracy score: 0.645
    - Precision: 0.01
    - Recall: 0.69
- `SMOTE` results:
    - Balanced accuracy score: 0.662
    - Precision: 0.01
    - Recall: 0.63
- `ClusterCentroids` results:
    - Balanced accuracy score: 0.662
    - Precision: 0.01
    - Recall: 0.69
- `SMOTEEN` results:
    - Balanced accuracy score: 0.645
    - Precision: 0.01
    - Recall: 0.78
- `BalancedRandomForestClassifier` results:
    - Balanced accuracy score: 0.789
    - Precision: 0.03
    - Recall: 0.70
- `EasyEnsembleClassifier` results:
    - Balanced accuracy score: 0.932 
    - Precision: 0.09 
    - Recall: 0.92 

## Summary:
After running our models, we had very low precision, but much higher recall. Because our data is extremely unbalanced, we had a lot more false positives which caused our precision to be very low. Our best performing model was the `EasyEnsembleClassifier` with 93% of classified cases classified correctly. The `EasyEnsembleClassifier` returned a 0.09 precision, so of those classified as high risk, 9% of them were actually high risk. The `EasyEnsembleClassifier` had a recall of 0.92, so of the high risk cases, 92% of them were picked up. I would recommend this model to classify high risk and low risk loans because it had high accuracy and recall, and a much higher precision than the other models.