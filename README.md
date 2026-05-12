# Credit Risk Prediction — ML Classification

<div align="center">

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Sklearn](https://img.shields.io/badge/Scikit--Learn-ML-orange?style=for-the-badge)
![XGBoost](https://img.shields.io/badge/XGBoost-Boosting-red?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)

**Predicting loan default using Logistic Regression, Random Forest, XGBoost, and KNN.**

[Overview](#-overview) · [Workflow](#-workflow) · [Models](#-models) · [Results](#-results)

</div>

---

## Overview

Credit risk assessment is critical for financial institutions to minimise loan defaults. This project builds and compares **4 ML classification models** to predict whether a loan applicant is likely to default — using thorough data preprocessing, outlier treatment, and model evaluation on the Credit Risk Dataset from Kaggle.

---

## Dataset

- **Source:** [Credit Risk Dataset — Kaggle](https://www.kaggle.com/datasets/laotse/credit-risk-dataset)
- **Target:** `loan_status` (0 = Non-default, 1 = Default)
- **Features:** Age, Income, Loan Amount, Interest Rate, Loan Intent, Loan Grade, Credit History Length, Home Ownership, and more

---

## Workflow

### Step 1 — Exploratory Data Analysis
- Scatter plots coloured by loan status
- Age vs. Income, Loan Amount vs. Interest Rate analysis
- Key observations:
  - Higher income & age → lower default likelihood
  - Higher loan amount & interest rate → higher default risk

### Step 2 — Handling Missing Values
- Identified missing values across all features
- Corrected obvious errors (unrealistic age/employment length values → NaN)
- Imputation using `SimpleImputer`

### Step 3 — Outlier Detection & Treatment
Features treated: `person_age`, `person_income`, `loan_amnt`, `loan_int_rate`, `loan_percent_income`, `cb_person_cred_hist_length`

Winsorization applied using `scipy.stats.mstats`

### Step 4 — Modelling
- Label encoding for categorical features
- Standard scaling / Robust scaling
- Train-test split
- 4 models trained and compared

---

## Models

| Model | Type |
|-------|------|
| Logistic Regression | Linear Classifier |
| Random Forest | Ensemble (Bagging) |
| XGBoost | Ensemble (Boosting) |
| K-Nearest Neighbors (KNN) | Instance-based |

---

## Evaluation Metrics

- Accuracy
- ROC-AUC Score
- Confusion Matrix (for all 4 models)

---

## Libraries Used

| Library | Purpose |
|---------|---------|
| pandas, numpy | Data manipulation |
| matplotlib, seaborn | Visualisation |
| scikit-learn | ML models & preprocessing |
| xgboost | Gradient boosting |
| scipy | Winsorization / outlier treatment |

---

## Setup

```bash
git clone https://github.com/AmithaMahesh/credit-risk-prediction.git
cd credit-risk-prediction
pip install -r requirements.txt
```

---

## Team
By:
- Amitha Mahesh
- Nitheka A
- Shivvanni Senthil
- Vivethasri
  
Built at Amrita Vishwa Vidyapeetham, Coimbatore.

Guided by **Dr. Vipin Venugopal**, Amrita Vishwa Vidyapeetham.

---

## Tags

`Machine Learning` `Classification` `Credit Risk` `XGBoost` `Random Forest` `Logistic Regression` `KNN` `Python` `Scikit-Learn` `Data Preprocessing` `EDA` `Finance`
