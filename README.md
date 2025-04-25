# 💳 LendingClub Loan Default Prediction: Machine Learning Project

This project aims to predict the likelihood of loan default for borrowers using the LendingClub public dataset. The analysis applies an end-to-end machine learning pipeline including data preprocessing, feature engineering, model training, and evaluation, with the goal of enabling better credit risk management and informed lending decisions.

---

## 🎯 Objective

The primary objective is to use historical loan application and payment data to classify whether a loan is likely to default or be fully paid. Accurate prediction of defaults can help financial institutions minimize risk and improve portfolio quality.

---

## 📊 Dataset

This project uses aggregated public datasets from Kaggle, based on LendingClub's historical loan performance data. These datasets include issued loans, borrower profiles, and loan status from multiple contributors:

- [`wordsforthewise/lending-club`](https://www.kaggle.com/datasets/wordsforthewise/lending-club)
- [`husainsb/lendingclub-issued-loans`](https://www.kaggle.com/datasets/husainsb/lendingclub-issued-loans)
- [`janiobachmann/lending-club-first-dataset`](https://www.kaggle.com/datasets/janiobachmann/lending-club-first-dataset)
- [`ethon0426/lending-club-20072020q1`](https://www.kaggle.com/datasets/ethon0426/lending-club-20072020q1)
- [`jeandedeieunyandwi/lending-club-dataset`](https://www.kaggle.com/datasets/jeandedeieunyandwi/lending-club-dataset)
- [`adarshsng/lending-club-loan-data-csv`](https://www.kaggle.com/datasets/adarshsng/lending-club-loan-data-csv)

> The final working dataset used in the analysis was compiled, cleaned, and filtered from these sources to focus on core financial variables and target classification labels (e.g., Fully Paid vs Charged Off).


---

## 🔁 Workflow Overview

### ✅ 1. Data Preprocessing
- Handled missing values
- Dropped irrelevant columns (e.g., IDs, long text fields)
- Encoded categorical variables

### ✅ 2. Exploratory Data Analysis (EDA)
- Distribution of loan status
- Loan amount vs interest rate correlation
- Default rates by grade, employment length, and home ownership

### ✅ 3. Feature Engineering
- Created new features like `income_to_loan_ratio`
- Binarized `loan_status` into 0 (Fully Paid) and 1 (Default)

### ✅ 4. Model Training
- Logistic Regression
- Random Forest Classifier
- XGBoost Classifier (boosting method for better performance)

### ✅ 5. Model Evaluation
- Confusion matrix
- Precision, Recall, F1-score
- ROC-AUC curve


---

## 🧰 Tech Stack

- Python
- pandas, numpy
- scikit-learn
- XGBoost
- matplotlib, seaborn

---

## 🔬 Key Insights

- Higher interest rates correlate strongly with loan defaults
- Lower credit grades (Grade D, E, F) have significantly higher default rates
- Annual income, debt-to-income (DTI) ratio, and credit history are strong predictors

---

## 🚀 Possible Enhancements

- Hyperparameter tuning with GridSearchCV
- Feature selection with Recursive Feature Elimination (RFE)
- Model explainability using SHAP values
- Deploying the best model via a Flask API or Streamlit app
