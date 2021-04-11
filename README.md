# Credit_Risk_Analysis
Module 17 Challenge

### Overview
The intent of this exercise was to use multiple machine learning modeling techniques to classify credit applicants as high or low risk.  Given the unbalanced nature of loans - there significantly more safe loans than risky loans - different techniques need to be employed in order to improve the quality of modeling outcomes in order to overcome the heavily skewed training dataset.

### Results:
For each model, we reviewed the following: 
- the Balanced Accuracy score produced by the sklearn.metrics computation
- the Accuracy calculation to understand the percentage of correct predictions (TP + TN / (TP + TN + FP + FN))
- the Precision score to understand the percentage of positive predictions that are correct (TP / (TP + FP))
- the Recall (or sensitivity) score to understand the percentage of actual positive results that are predicted correctly (TP / (TP + FN))

We reviewed Precision and Recall scores for both Low- and High-risk predictions to understand each model's ability to effectively predict High-risk 


**Naive Random Oversampling**
- Balanced Accuracy Score: 0.6296
- Calculated Accuracy Score: 0.6615
- Precision Score (Low-risk): 0.6615
- Precision Score (High-risk): 0.5977
- Recall Score (Low-risk): 0.9969
- Recall Score (High-risk): 0.0089

![Naive_Random.png](https://github.com/benclark62/Credit_Risk_Analysis/blob/main/1naive_random.png)


**SMOTE Oversampling**
- Balanced Accuracy Score: 0.6209
- Calculated Accuracy Score: 0.6438
- Precision Score (Low-risk): 0.6440
- Precision Score (High-risk): 0.5977
- Recall Score (Low-risk): 0.9968
- Recall Score (High-risk): 0.0085

![SMOTE.png](https://github.com/benclark62/Credit_Risk_Analysis/blob/main/1SMOTE.png)


**Undersampling**
- Balanced Accuracy Score: 0.5293
- Calculated Accuracy Score: 0.4503
- Precision Score (Low-risk): 0.4495
- Precision Score (High-risk): 0.6092
- Recall Score (Low-risk): 0.9956
- Recall Score (High-risk): 0.0056

![Undersampling.png](https://github.com/benclark62/Credit_Risk_Analysis/blob/main/1Undersampling.png)


**SMOTEENN**
- Balanced Accuracy Score: 0.6375
- Calculated Accuracy Score: 0.5745
- Precision Score (Low-risk): 0.5739
- Precision Score (High-risk): 0.7012
- Recall Score (Low-risk): 0.0083
- Recall Score (High-risk): 0.9974

![SMOTEENN.png](https://github.com/benclark62/Credit_Risk_Analysis/blob/main/1SMOTEENN.png)


**Balanced Random Forest Classifier**
- Balanced Accuracy Score: 0.9959
- Calculated Accuracy Score: 0.9959
- Precision Score (Low-risk): 0.9994
- Precision Score (High-risk): 0.3333
- Recall Score (Low-risk): 0.9966
- Recall Score (High-risk): 0.725

![brfc.png](https://github.com/benclark62/Credit_Risk_Analysis/blob/main/1BRFC.png)

**AdaBoost Classifier**
- Balanced Accuracy Score: 0.9964
- Calculated Accuracy Score: 0.9935
- Precision Score (Low-risk): 0.9964
- Precision Score (High-risk): 0.4138
- Recall Score (Low-risk): 0.9970
- Recall Score (High-risk): 0.3711

![adaboost.png](https://github.com/benclark62/Credit_Risk_Analysis/blob/main/1ADA.png)


### Summary
The very low number of high-risk loans included in the datasets limits some models from accurately predicting high-risk loans going forward.  The ensemble methods helped provide higher accuracy scores due to creating more balanced training and testing datasets. 

- Naive Random Oversampling: Overall accuracy of ~63-66% is not high enough to rely on this model going forward; very low High-risk Recall scores (0.0089) due to high prevalence of false negatives (predicted high-risk, but actually low-risk)
- SMOTE Oversampling: Overall accuracy of ~62-64% is not high enough to rely on this model going forward; very low High-risk Recall scores (0.0085) due to high prevalence of false negatives (predicted high-risk, but actually low-risk)
- Undersampling: Very low accuracy scores (~45-53%)is not high enough to rely on this model going forward; very low High-risk Recall scores (0.0056) due to high prevalence of false negatives (predicted high-risk, but actually low-risk)
- SMOTEEN: Overall accuracy scores of ~57-64% is not high enough to rely on this model going forward; very low High-risk Recall scores (0.0083) due to high prevalence of false negatives (predicted high-risk, but actually low-risk)
- Balanced Random Forest Classifier: High accuracy score (99%+) make this a reliable model; higher precision (33.3%) and recall (72.5%) scores for high-risk loans greatly outperforms prior models.
- AdaBoost Classifier: High accuracy score (99%+) makes this a reliable model; higher precision (41.4%) and recall (37.1%) scores for high-risk loans greatly outperforms prior models.

**Recommendation**
The ensemble methods (Balanced Random Forest and AdaBoost Classifiers) both greatly outperformed prior modeling techniques.  The improved performance was tied primarily to these models' ability to nearly eliminate the occurence of false negatives (predicted high-risk, but actually low-risk).  Due to the stronger high-risk recall performance, I would recommend moving forward with the Balanced Random Forest Classifier.
