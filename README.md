# Binary-Classification-with-a-Bank-Dataset
# Bank Term Deposit Prediction (Kaggle Playground 2025)

## 📌 Overview
This project tackles a **binary classification challenge** from the Kaggle Playground Series (August 2025).  
The goal is to predict whether a bank client will subscribe to a term deposit, using a synthetically generated dataset inspired by the UCI Bank Marketing dataset.

- **Competition Link**: [Kaggle Playground Series - Aug 2025](https://www.kaggle.com/competitions/playground-series-s4e8)
- **Evaluation Metric**: ROC AUC
- **Submission Format**: Probability predictions (`id,y`)

---

## 🛠️ Approach
1. **Data Preprocessing**
   - Encoded categorical features (`job`, `marital`, `education`, `contact`, `month`, `poutcome`).
   - Converted binary columns (`default`, `housing`, `loan`) to numerical (0/1).
   - Engineered `contacted_before` from `pdays`.
   - Standardized numerical features for linear models.

2. **Models Used**
   - Logistic Regression (baseline) → ROC AUC ~ **0.943**
   - XGBoost (tuned) → ROC AUC ~ **0.966**
   - Blending Logistic + XGBoost for experimentation.

3. **Pipeline**
   - Cross-validation with **Stratified K-Fold**.
   - Feature scaling with **StandardScaler** (for linear models).
   - Automated preprocessing & alignment for train/test sets.

---

## 📊 Results
- **Logistic Regression**: ROC AUC ≈ 0.943  
- **XGBoost**: ROC AUC ≈ 0.966  
- **Final Submission**: Probability predictions in required Kaggle format (`submission.csv`).

---

## 📂 Repository Structure
