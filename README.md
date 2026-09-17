<div align="center">

# 🛒 Online Shopper Purchasing Intention Prediction

[![Python 3.10+](https://img.shields.io/badge/Python-3.10%2B-blue.svg)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

*An end-to-end machine learning pipeline predicting real-time e-commerce transaction completions (`Revenue`) based on session behavior, analytics, and temporal attributes.*

</div>

---

## 📌 Executive Summary
* **Dataset Audit:** 12,205 unique sessions (10,312 non-converting / 1,893 converting) after removing 125 exact duplicates.
* **Class Imbalance:** Solved severe 15.47% positive conversion imbalance using cost-sensitive weighting (`class_weight='balanced'`) and SMOTE oversampling.
* **Top Predictor:** `PageValues` accounts for >40% of Gini importance in distinguishing active buyers from casual browsers.
* **Production Model:** Cost-sensitive Random Forest achieved an **ROC-AUC of 0.9253** and an **F1-Score of 0.6764**.

---

## 📊 Model Performance Comparison

| Model Pipeline | Imbalance Strategy | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **Random Forest** | **Balanced Class Weight** | **89.8%** | **0.6318** | **0.7277** | **0.6764** | **0.9253** |
| **Random Forest** | SMOTE Resampling | 88.6% | 0.6410 | 0.7199 | 0.6782 | 0.9249 |
| **Logistic Regression** | Balanced Class Weight | 87.2% | 0.5164 | 0.7853 | 0.6231 | 0.9109 |
| **Decision Tree** | Default Weights | 85.1% | 0.5210 | 0.5420 | 0.5313 | 0.7240 |

---


## 📈 Visualizations & Key Analytics

### Model ROC-AUC Performance
<img src="ml project screenshots/ROC Curves.png" alt="ROC Curves" width="100%">

### Confusion Matrices Evaluation
<img src="ml project screenshots/Confusion Matrices.png" alt="Confusion Matrices" width="100%">

### Feature Importance Breakdown
<img src="ml project screenshots/Feature Importance.png" alt="Feature Importance" width="100%">
---

## 🛠️ Installation & Environment Setup

1. **Clone Repository:**
   ```bash
   git clone [https://github.com/BrianKKoskei/online_shoppers_intention.git](https://github.com/BrianKKoskei/online_shoppers_intention.git)
   cd online_shoppers_intention
