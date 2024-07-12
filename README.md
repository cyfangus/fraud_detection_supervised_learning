# fraud_detection_supervised_learning
This contains python codes to utilise several supervised machine learning algorithm to identify fraudulent transactions from a dataset with 284,807 European credit card transactions with 492 fraudulent transactions that occurred over two days in September 2013. The dataset is obtained from Kaggle, see more from https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud.

Due to the imbalanced class in the dataset, Synthetic Minority Over-sampling Technique (SMOTE) has been applied to oversample the minority class in our dataset. And then, I have trained Logistic Regression, XGBoost, and Neural Network to predict fraudulent transactions. 

Without much fine tuning and preprocessing, the results show that XGBoost had the best performance among the models, with Accuracy: 0.9994, Precision: 0.8019, Recall: 0.8673, F1 score: 0.8333. It performs the best in terms of recall and F1 score, which are often more important matrics in the context of fruad detection.

<img width="669" alt="Screenshot 2024-07-12 at 11 56 14" src="https://github.com/user-attachments/assets/7a2e8184-bcfd-4614-9229-728e16c452fc">

<img width="707" alt="Screenshot 2024-07-12 at 11 56 43" src="https://github.com/user-attachments/assets/8ae773af-616a-4617-89e2-66efcae70675">
