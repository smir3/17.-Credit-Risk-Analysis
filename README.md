# Credit-Risk-Analysis

## Background, Purpose and Task

Background and Purpose: 

LendingClub is a peer-to-peer lending services company. LendingClub management is seeking to improve the reliability and efficiency of their loan experience. Jill-the lead Data Scientist-would like to use machine learning to predict credit risk. Using machine learning will lead to a more accuracte identification of good candidates for loans, which will in turn lead to low default rates. 

Task:
I have been tasked with assisting Jill in implementing this plan. Using the credit care dataset from LendingClub, I will first oversample the data using RandomOverSampler and SMOTE algorithms, and then undersample the data using the the ClusterCentroids algorithm. Next, I will use the SMOTEENN algorithm to implement a combinatorial approach of over and undersampling. I will then compare the BalancedRandomForestClassifier machine learning model with the EasyEnsembleClassifier to predict credit risk.

Once these analyses are complete, I will evaluate the performance of these models to conclude whether its advisable to use them for predicting credit risk. 

## Results
There were six machine learning models tested in this analysis.

1. Naive Random Oversampling: The balanced accuracy score was 65.7%, the prediction and recall score for the high_risk group was 1% and 71% respectively, and for the low_risk group it was 100% and 60%.
2. SMOTE Oversampling: The balanced accuracy score was 66.2%, the prediction and recall score for the high_risk group was 1% and 63% respectively, and for the low_risk group it was 100% and 69%.
3. Undersampling: The balanced accuracy score was 54.4%, the prediction and recall score for the high_risk group was 1% and 69% respectively, and for the low_risk group it was 100% and 40%.
4. Combinatation (Over and Under) Sampling: The balanced accuracy score was 64.5%, the prediction and recall score for the high_risk group was 1% and 72% respectively, and for the low_risk group it was 100% and 57%.
5. Balanced Random Forest Classifier: The balanced accuracy score was 78.8%, the prediction and recall score for the high_risk group was 3% and 70% respectively, and for the low_risk group it was 100% and 87%.
6. Easy Ensemble AdaBoost Classifier

 balanced accuracy score and the precision and recall scores of all six machine learning models

## Summary and Recommendations:

There is a summary of the results 


There is a recommendation on which model to use, or there is no recommendation with a justification (3 pt)

