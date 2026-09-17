# Online Shopper Purchasing Intention Prediction

A machine learning pipeline to predict real-time e-commerce transaction completions (`Revenue`) using session-level browsing behavior, engagement metrics, calendar attributes, and user demographics.

## 📌 Executive Summary
* **Clean Dataset:** 12,205 unique sessions (10,312 non-converting / 1,893 converting) following duplicate removal.
* **Class Imbalance:** Handled 15.47% positive class ratio using cost-sensitive class weighting (`class_weight='balanced'`) and SMOTE oversampling.
* **Top Predictor:** `PageValues` serves as the primary driver of conversion intent, contributing over 40% of feature importance.

## 📊 Model Performance Comparison

| Model Pipeline | Class Weighting | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **Random Forest** | **Balanced** | **89.8%** | **0.6318** | **0.7277** | **0.6764** | **0.9253** |
| **Logistic Regression** | Balanced | 87.2% | 0.5164 | 0.7853 | 0.6231 | 0.9109 |
| **Decision Tree** | Default | 85.1% | 0.5210 | 0.5420 | 0.5313 | 0.7240 |

## 🛠️ Installation & Setup

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/BrianKKoskei/online_shoppers_intention.git](https://github.com/BrianKKoskei/online_shoppers_intention.git)
   cd online_shoppers_intention
