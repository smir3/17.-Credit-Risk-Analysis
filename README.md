# Credit-Risk-Analysis

## Background, Purpose and Task

Background and Purpose: 

LendingClub is a peer-to-peer lending services company. LendingClub management is seeking to improve the reliability and efficiency of their loan experience. Jill-the lead Data Scientist-would like to use machine learning to predict credit risk. Using a good machine learning model to predict credit risk will lead to a more accurate identification of good candidates for loans, which will in turn lead to low default rates. 

Task:
I have been tasked with assisting Jill in implementing this plan. Using the credit care dataset from LendingClub, I will first oversample the data using RandomOverSampler and SMOTE algorithms, and then undersample the data using the the ClusterCentroids algorithm. Next, I will use the SMOTEENN algorithm to implement a combinatorial approach of over and undersampling. I will then compare the BalancedRandomForestClassifier machine learning model with the EasyEnsembleClassifier to predict credit risk.

Once these analyses are complete, I will evaluate the performance of these models to conclude whether its advisable to use them for predicting credit risk. 

## Results
There were six machine learning models tested in this analysis.
recall (sensitivity) for predicting diabetes is much lower than it is for predicting an absence of diabete

Goal is to predict if a loan appliation is worthy of approval. good loan application is 0, and bad loan application is 1. 
precision for bad loan application low means large number of false positives so unreliable positive classification, recall low for bad loan application means alot of false negatives. F1 score also low. 

precision is the measure of how reliable a positive classification is. low precision is indicative of a large number of false positives. Recall is the ability of the classifier to find all the positive samples. A low recall is indicative of a large number of false negatives. f1 best score is 1, and worst is 0.

***recall is predicting this is a high_risk group (higher value is good), prediction is saying this is not a high risk group (low value means likely to take non risk group and group as high risk). low group recall mean probability of predicting this is a low-risk group (high value means likelihood that high risk will be grouped as lowrisk), high prediction mean low-risk will not be identified.

1. Naive Random Oversampling: The balanced accuracy score was 65.7%, the precision and recall score for the high_risk group was 1% and 71% respectively, and for the low_risk group it was 100% and 60%.
2. SMOTE Oversampling: The balanced accuracy score was 66.2%, the precisionn and recall score for the high_risk group was 1% and 63% respectively, and for the low_risk group it was 100% and 69%.
3. Undersampling: The balanced accuracy score was 54.4%, the precision and recall score for the high_risk group was 1% and 69% respectively, and for the low_risk group it was 100% and 40%.
4. Combinatation (Over and Under) Sampling: The balanced accuracy score was 64.5%, the precision and recall score for the high_risk group was 1% and 72% respectively, and for the low_risk group it was 100% and 57%.
5. Balanced Random Forest Classifier: The balanced accuracy score was 78.8%, the precision and recall score for the high_risk group was 3% and 70% respectively, and for the low_risk group it was 100% and 87%.
6. Easy Ensemble AdaBoost Classifier

 balanced accuracy score and the precision and recall scores of all six machine learning models

## Summary and Recommendations:

The precision score for the high-risk group was consistently very low (1%-3%) for all models. Low precision is indicative of a large number of false positives, i.e many good candidates for loans will be marked as high-risk. The precision for the low-risk group was very high (100%) which means that there is a low chance of false positives - so candidates that are marked as low-risk are most probably low-risk. 

The recall score for the high risk group was moderatly high (63%-72%) for all models. Recall is the ability of the classifier to find all the positive samples. A high recall score means that high-risk candidates will often be identified. The recall score for low-risk groups was very low for the first four models (40%-69%), however it was higher for the BalancedRandomForestClassifier (87%). This means the BalancedRandomForestClassifier model will often identify low risk candidates.

In summary, the BalancedRandomForestClassifier had the best scores for accuracy, precision, and recall. The balanced accuracy score was considerable high (78.8%), and the recall scores for both the high-risk and low-risk group were good (70% and 87%) meaning that the model will identify most high-risk and low-risk candidates accurately. The precision value for the low-risk group is also really high at (100%) therefore all candidates marked as low-risk will actually be low-risk. However, the precision value generated by this model for high-risk candidates is higher than that of other models but it is still very low (3%). This low precision value means that many low-risk candites will be marked as high-risk.  Since this is an analysis of credit risk, it is better to have high sensitivty and low precision rather than high precision and low sensitivty. This is because it is better to be mor elikely to label candidates as high-risk than low-risk since this it is safer for the bank to be more selective in labelling candidates as good so that it does not not easily give out loans. 




There is a recommendation on which model to use, or there is no recommendation with a justification (3 pt)

