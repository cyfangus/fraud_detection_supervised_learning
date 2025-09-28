# Credit Card Fraud Detection – Supervised Learning (Portfolio Project)

## Project Summary
Detecting costly credit card fraud using supervised machine learning (Logistic Regression, Random Forest, Naïve Bayes, MLP) and SMOTE for class imbalance. Results benchmarked against published peer-reviewed study. Clear business context, actionable results, and model interpretability highlighted. 
Referencing Varmedja, Dejan, et al. "Credit card fraud detection-machine learning methods." 2019 18th International Symposium INFOTEH-JAHORINA (INFOTEH). IEEE, 2019. [see here](https://github.com/cyfangus/fraud_detection_supervised_learning/blob/main/Credit_Card_Fraud_Detection_-_Machine_Learning_methods.pdf)

## Dataset
[Kaggle European credit card transactions](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud), anonymized for privacy. Highly imbalanced (284,807 transactions; 492 fraud).

## Key Results
- [b]Best model: Random Forest (Resampled with SMOTE)[/b] (scoring F1 = 0.8705, Precision = 0.8842, Recall = 0.8571, and Accuracy = 0.9996.
  This model provides the strongest balance between correctly identifying fraud and minimizing false positives, outperforming other tested approaches in this highly imbalanced dataset.)
- Feature importance: [Top drivers]
- ROC AUC: [Value]; PR AUC: [Value]

## Business Impact
Emphasizes cost savings, risk compliance, and importance of recall over accuracy for operational fraud detection.

## Next Steps
- Try insurance/open banking datasets
- Integrate explainability tools (SHAP)
- Simulate cost/benefit of thresholds

*Full [notebook]((https://github.com/cyfangus/fraud_detection_supervised_learning/blob/main/fraud_detection_supervised_learning.ipynb)) and summary PDF inside this repo.*

![output](https://github.com/user-attachments/assets/0114c055-37ae-4532-89fc-a8eb2513c833)

