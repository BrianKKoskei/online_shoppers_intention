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
<img width="669" height="494" alt="ROC Curves" src="https://github.com/user-attachments/assets/e03d6efc-ce39-44a7-96a4-7108fabe4342" />

### Confusion Matrices Evaluation
<img width="999" height="419" alt="Confusion Matrices" src="https://github.com/user-attachments/assets/9b255be9-4106-4687-8148-590f2d4ea6a9" />


### Feature Importance Breakdown
<img width="842" height="502" alt="Feature Importance" src="https://github.com/user-attachments/assets/989831d0-d689-4ad4-87d0-7b3ded125624" />

---

## 🛠️ Installation & Environment Setup

1. **Clone Repository:**
   ```bash
   git clone [https://github.com/BrianKKoskei/online_shoppers_intention.git](https://github.com/BrianKKoskei/online_shoppers_intention.git)
   cd online_shoppers_intention
