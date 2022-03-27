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
The recall score will provide the best indicator of the number of high risk cases that are caught. Using this figure may label some low risk cases as high risk, but a higher recall score ensures that the highest number of high risk cases are identified.
<br><br>
<b>Native Random Oversampling</b>
<img src="Images/native_oversampling.png"><br>
High risk recall score of 0.72<br><br>
<b>SMOTE Oversampling</b>
<img src="Images/smote_oversampling.png"><br>
High risk recall score of 0.61<br><br>
<b>Cluster Centroids Undersampling</b>
<img src="Images/clustercentroids_undersampling.png"><br>
High risk recall score of 0.69<br><br>
<b>SMOTEENN Combination Sampling</b>
<img src="Images/smoteenn_combination.png"><br>
High risk recall score of 0.78<br><br>
<b>Balanced Random Forest Classifier</b>
<img src="Images/randomforest_ensemble.png"><br>
High risk recall score of 0.70<br><br>
<b>Easy Ensemble AdaBoost Classifier</b>
<img src="Images/adaboost_ensemble.png"><br>
High risk recall score of 0.92<br>
<br><br>
## Recommendation
The Easy Ensemble AdaBoost Classifier algorithm is the obvious choice, because it correctly identified 92% of the fraudulent cases.