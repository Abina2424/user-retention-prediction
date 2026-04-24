# user-retention-prediction
ML project to predict user retention using classification models

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Latest-orange)](https://scikit-learn.org/)
[![Status](https://img.shields.io/badge/Status-Completed-success)](#)

## 📌 Project Overview
This project addresses the critical challenge of user churn by developing a predictive framework for user retention. Using market engagement data from the Google Play Store, the system identifies behavioral patterns that differentiate successful, high-retention products from those at risk of churn.

The goal is to move from a reactive strategy to a **proactive intervention model**, allowing teams to identify at-risk users/apps before they exit the platform.

## 🎯 Objectives
* **Predict Retention Probability:** Assign a 0-1 score to each user/app to quantify the likelihood of staying.
* **Identify Churn Signals:** Pinpoint which engagement metrics (ratings, interaction volume) drive loyalty.
* **Support Targeted Strategies:** Provide actionable insights for personalized retention campaigns.

## 📊 Dataset & Feature Engineering
**Dataset:** [Google Play Store Apps](https://www.kaggle.com/datasets/gauthamp10/google-playstore-apps)

**Key Transformations:**
* **Target Definition:** Retention was modeled as a binary classification where `1` (Retained) represents apps crossing the **10,000+ installs** threshold.
* **Feature Selection:** Focused on **Rating** and **Rating Count** as primary proxies for engagement.
* **Preprocessing:** Handled missing values, standardized numeric inputs, and cleaned string-based categorical data.

## 🛠️ Technical Stack
* **Languages:** Python
* **Libraries:** Pandas, NumPy, Scikit-learn
* **Visualization:** Matplotlib, Seaborn
* **Models:** Logistic Regression, Random Forest, Gradient Boosting

## 📈 Model Performance
To ensure reliability, **Stratified K-Fold Cross-Validation** was used to evaluate all models.

| Model | ROC-AUC Score | Key Strength |
| :--- | :--- | :--- |
| **Logistic Regression** | 0.95 | Baseline interpretability |
| **Random Forest** | 0.95 | Robustness to non-linear data |
| **Gradient Boosting** | **0.96** | **Highest predictive accuracy** |

> **Result:** The system achieved a near-excellent **ROC-AUC of 0.96**, indicating a high capability to distinguish between retained and churned users.

## 💡 Key Insights
1. **Social Proof > Sentiment:** Analysis of **Feature Importance** revealed that **'Rating Count'** is a significantly stronger predictor of retention than the **'Rating'** score itself. 
2. **Engagement Thresholds:** Apps with high interaction volume show exponentially higher retention rates, suggesting that getting users to perform "recurring actions" (like rating) is the primary driver of loyalty.

## 🚀 How to Run
1. Clone the repository:
   ```bash
   git clone [https://github.com/your-username/user-retention-prediction.git](https://github.com/your-username/user-retention-prediction.git)
