# Credit Risk Analysis
Supervised ML evaluation of credit risk data

## Purpose
This analysis uses machine learning to train a model to predict high risk credit loans. The number of low risk loans in the dataset far outweigh the number of high risk loans. Therefore, the imblanced learn library was used to deal with this asymmetry. 
<br><br>
## Methods
Several algorithms were used in order to determine the best performance for the model. In particular, resampling and ensemble techniques were used.
### Resampling
Oversampling from the high risk cases using <b>RandomOverSampler</b> and <b>SMOTE</b> algorithms were used to balance the number of cases being analyzed. The <b>ClusterCentroids</b> algorithm was used to undersample the low risk cases for the same purpose. Additionally, a combination of oversampling and undersampling, <b>SMOTEENN</b> was used to balance the inputs.
###Ensemble Classifiers
The <b>BalancedRandomForestClassifier</b> and <b>AdaBoost</b> algorithms were used to employ decision tree techniques to produce a more robust and accurate model.
<br><br>
## Analysis
When detecting fraud, the most important measurement to pay attention to is not the overall accuracy of the model, but the sensitivity. Sensitivity is measured by the recall score and means that a high percentage of the true positives will be identified, even if there are more false positives as a result. Let's see how these six algorithms perform with regard to sensitivity.<br>
<b>Native Random Oversampling</b>
<img src="Images/native_oversampling.png">
High risk recall score of 0.72<br>
<b>SMOTE Oversampling</b>
<img src="Images/smote_oversampling.png">
High risk recall score of 0.61<br>
<b>Cluster Centroids Undersampling</b>
<img src="Images/clustercentroids_undersampling.png">
High risk recall score of 0.69<br>
<b>SMOTEENN Combination Sampling</b>
<img src="Images/smoteenn_combination.png">
High risk recall score of 0.78<br>
<b>Balanced Random Forest Classifier</b>
<img src="Images/randomforest_ensemble.png">
High risk recall score of 0.70<br>
<b>Easy Ensemble AdaBoost Classifier</b>
<img src="Images/adaboost_ensemble.png">
High risk recall score of 0.92<br>
<br><br>
## Recommendation
The Easy Ensemble AdaBoost Classifier algorithm is the obvious choice, because it correctly identified 92% of the fraudulent cases.