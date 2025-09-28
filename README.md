# Credit Card Fraud Detection – Supervised Learning (Portfolio Project)

## Project Summary
Detecting costly credit card fraud using supervised machine learning (Logistic Regression, Random Forest, Naïve Bayes, MLP) and SMOTE for class imbalance. Results benchmarked against published peer-reviewed study. Clear business context, actionable results, and model interpretability highlighted. 
Referencing Varmedja, Dejan, et al. "Credit card fraud detection-machine learning methods." 2019 18th International Symposium INFOTEH-JAHORINA (INFOTEH). IEEE, 2019. [see here](https://github.com/cyfangus/fraud_detection_supervised_learning/blob/main/Credit_Card_Fraud_Detection_-_Machine_Learning_methods.pdf)

## Dataset
[Kaggle European credit card transactions](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud), anonymized for privacy. Highly imbalanced (284,807 transactions; 492 fraud).

## Key Results
- **Best model: Random Forest (Resampled with SMOTE)** (scoring F1 = 0.8705, Precision = 0.8842, Recall = 0.8571, and Accuracy = 0.9996.
  This model provides the strongest balance between correctly identifying fraud and minimizing false positives, outperforming other tested approaches in this highly imbalanced dataset.)
- Feature importance analysis revealed that several principal components, including V17, V14, and V12, were the most influential predictors, although individual features are anonymized due to PCA transformation.
- The model achieved a high accuracy of 99.96%, while ROC AUC and PR AUC metrics demonstrate strong discriminatory power in identifying fraudulent transactions in this highly imbalanced dataset.
- Feature engineering proactively removed redundant and low-importance features, reducing the data to 20 key components without impacting model performance, improving training efficiency and model clarity.

## Business Impact
By employing SMOTE to effectively balance highly imbalanced fraud datasets, this project demonstrates that traditional machine learning models such as Random Forest can achieve fraud detection performance comparable to complex deep learning models like neural networks. For financial institutions and insurers, this represents a cost-saving advantage by reducing the need for expensive computational infrastructure, lengthy model tuning, and specialized skillsets required for neural networks. It also allows the model to be more explainable and transparent. These efficiencies accelerate deployment timelines and reduce operational overhead while maintaining robust detection accuracy, ultimately helping organizations minimize fraud losses, optimize investigation workflows, and comply with stringent regulatory standards more efficiently.

## Next Steps
- Try insurance/open banking datasets
- Integrate explainability tools (SHAP)
- Simulate cost/benefit of thresholds

*Full [notebook]((https://github.com/cyfangus/fraud_detection_supervised_learning/blob/main/fraud_detection_supervised_learning.ipynb)) and summary PDF inside this repo.*

![output](https://github.com/user-attachments/assets/0114c055-37ae-4532-89fc-a8eb2513c833)

