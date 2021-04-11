# Credit_Risk_Analysis
Module 17 Challenge

### Overview
The intent of this exercise was to use multiple machine learning modeling techniques to classify credit applicants as high or low risk.  Given the unbalanced nature of loans - there significantly more safe loans than risky loans - different techniques need to be employed in order to improve the quality of modeling outcomes in order to overcome the heavily skewed training dataset.

### Results:
For each model, we reviewed the following: 
- the Balanced Accuracy score produced by the sklearn.metrics model
- the accuracy calculation to understand the percentage of correct predictions (TP + TN / (TP + TN + FP + FN))
- the precision score to understand the percentage of positive predictions that are correct (TP / (TP + FP))
- the recall or sensitivity score to understand the percentage of actual positive results that are predicted correctly (TP / (TP + FN))
We reviewed Precision and Recall scores for both Low- and High-risk predictions.


- **Naive Random Oversampling**
- Balanced Accuracy Score: 0.6296
- Calculated Accuracy Score: 0.6615
- Precision Score (Low-risk): 0.6615
- Precision Score (High-risk): 0.5977
- Recall Score (Low-risk): 0.0089
- Recall Score (High-risk): 0.9969

![Naive_Random.png](https://github.com/benclark62/Credit_Risk_Analysis/blob/main/1naive_random.png)


- **SMOTE Oversampling**
- Balanced Accuracy Score: 0.6209
- Calculated Accuracy Score: 0.6438
- Precision Score (Low-risk): 0.6440
- Precision Score (High-risk): 0.5977
- Recall Score (Low-risk): 0.0085
- Recall Score (High-risk): 0.9968

![SMOTE.png](https://github.com/benclark62/Credit_Risk_Analysis/blob/main/1SMOTE.png)


- **Undersampling**
- Balanced Accuracy Score: 0.5293
- Calculated Accuracy Score: 0.4503
- Precision Score (Low-risk): 0.4495
- Precision Score (High-risk): 0.6092
- Recall Score (Low-risk): 0.0056
- Recall Score (High-risk): 0.9956

![Undersampling.png](https://github.com/benclark62/Credit_Risk_Analysis/blob/main/1Undersampling.png)


- **SMOTEENN**
- Balanced Accuracy Score: 0.6375
- Calculated Accuracy Score: 0.5745
- Precision Score (Low-risk): 0.5739
- Precision Score (High-risk): 0.7012
- Recall Score (Low-risk): 0.0083
- Recall Score (High-risk): 0.9974

![SMOTEENN.png](https://github.com/benclark62/Credit_Risk_Analysis/blob/main/1SMOTEENN.png)


- **Balanced Random Forest Classifier**
- Balanced Accuracy Score: 0.9959
- Calculated Accuracy Score: 0.9959
- Precision Score (Low-risk): 0.9994
- Precision Score (High-risk): 0.3333
- Recall Score (Low-risk): 0.725
- Recall Score (High-risk): 0.9966

![brfc.png](https://github.com/benclark62/Credit_Risk_Analysis/blob/main/1BRFC.png)

- **AdaBoost Classifier**
- Balanced Accuracy Score: 0.9964
- Calculated Accuracy Score: 0.9935
- Precision Score (Low-risk): 0.9964
- Precision Score (High-risk): 0.4138
- Recall Score (Low-risk): 0.3711
- Recall Score (High-risk): 0.9970

![adaboost.png](https://github.com/benclark62/Credit_Risk_Analysis/blob/main/1ADA.png)

Summary:

There is a summary of the results (2 pt)
There is a recommendation on which model to use, or there is no recommendation with a justification (3 pt)
