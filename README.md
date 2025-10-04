# Fraud Detection with Supervised Learning: SMOTE and Synthetic Data

## Overview

This project investigates whether **traditional machine learning algorithms** enhanced with **data augmentation** (SMOTE and generative synthetic data via SDV) can rival deeper models for fraud detection. It focuses on:

- **Imbalanced classification:** Real-world credit card fraud.
- **Data augmentation:** Using both SMOTE and generative synthetic data.
- **Modeling:** Benchmarking Random Forest, XGBoost, Logistic Regression, and an MLP.
- **Evaluation:** Precision, recall, F1, ROC-AUC, and domain-aware discussion.

## Dataset

- Uses the **Kaggle credit card fraud dataset** (`creditcard.csv`), featuring engineered PCA components (V1–V28), plus transaction time and amount.

## Workflow

1. **EDA:** Plots/analysis reveal extreme class imbalance, feature skewness, and weak simple correlations — motivating log transformation and custom scaling.
2. **Preprocessing:**
    - **Feature Scaling:** RobustScaler
    - **Amount Transformation:** Log (for stability and interpretability)
    - **Class Balancing:** (1) SMOTE oversampling; (2) SDV synthetic data
3. **Model Training:**
    - Models compared on original and augmented data
    - Random Forest, XGBoost, Logistic Regression (top 3 models used in fraud detection according to [Chen et al. (2025)](https://www.sciencedirect.com/science/article/pii/S2666764925000372?ref=pdf_download&fr=RR-2&rr=989454db9d666553)
    - Deep learning baseline (MLP)
4. **Evaluation:**
    - Detailed metrics: precision, recall, F1, ROC-AUC
    - ROC curve visualization for all models and setups

## Key Findings

- **SMOTE/synthetic data** dramatically improve recall (fewer missed frauds), especially for Logistic Regression and XGBoost.
- **Precision drops** for some models, increasing false positives—but this often aligns with business priorities in fraud prevention.
- **Random Forest & MLP** achieve a better balance of recall/precision for automated systems.
- **Feature engineering (log-amount), robust scaling, and more domain features are essential.**

## Domain-Specific Insights

- **Recall > Precision** for fraud: Missing fraud cases is riskier than investigating extra cases.
- **Threshold tuning and cost-sensitive evaluation** are critical in real production deployments.

## Next Steps

- **Tune class weighting and thresholds** to further balance false alarms vs missed fraud.
- **Add domain-relevant features** (velocity, merchant types, etc.).
- **Stratified cross-validation** and more robust evaluation metrics (PR-AUC, cost-based loss).
- **Model explainability (SHAP, LIME)** for analyst support.

## Conclusion

**Synthetic oversampling using SMOTE and generative AI significantly improves the minority class detection in classical machine learning models, narrowing the gap with deep learning methods—and proving essential for practical, scalable fraud prevention in imbalanced datasets.**

---

## Getting Started

1. Clone repo & install requirements:

```bash
git clone https://github.com/cyfangus/fraud_detection_supervised_learning.git
cd fraud_detection_supervised_learning
pip install -r requirements.txt
```

2. Run **FraudDetection.ipynb** in Jupyter or VSCode.

## Dependencies

- numpy, pandas, matplotlib, seaborn
- scikit-learn, imbalanced-learn (SMOTE)
- sdv (synthetic data generation)
- xgboost
- tensorflow (for deep learning/MLP)

## License

See LICENSE file in the repo.




