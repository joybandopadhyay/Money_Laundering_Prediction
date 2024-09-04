# Money_Laundering_Prediction
(i) Step: Maps a unit of time in the real world. In this case 1 step is 1 hour of time. 
(ii) Type: Indicates the type of transaction being performed. 
(iii) Amount: Indicates the amount of money being transacted. 
(iv) nameOrg: It indicates the name of the sender from where the transaction is being initiated. 
(v) oldbalanceOrg: It indicates the balance of the sender of the amount before transaction. 
(vi) nameDest: It indicates the name of the receiver of the amount that is being transferred. 
(vii) oldbalanceDest: It indicates the old balance of the receiver before receiving the amount that is transferred. 
(viii) newbalanceDest: It indicates the new balance of the receiver after receiving the amount being transferred. 
(ix) isFraud: It indicates whether a transaction is fraudulent or not. If the outcome is 1 it means that the transaction is fraudulent and if the outcome is 0 is means that the transaction is not fraudulent. 
(x) isFlaggedFraud: It acts as an indicator that there is a potential possibility for a transaction to be a fraudulent one if it holds a value of 1 and otherwise if it holds zero.
This is a highly imbalanced dataset, with number of class 0 instances being 6354407 and number of class 1 instances being 8213. We apply smote, scaling after the train test split to avoid data leakage, still the models usually get heavily leaned towards the majority class in this sort of scenario. So here the classes have been balanced manually without smote and without causing any data leakage and then checked to ensure if there was any loss of information, since the models viz., Logistic Regression, Decision Tree Classifier, Random Forest Classifier performed well for both the majority and the minority classes hence it can be considered that there was no significant loss of information. Out of all these models, Random Forest Classifier yielded the superior results.
