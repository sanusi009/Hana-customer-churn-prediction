# 📉 Customer Churn Prediction with SAP HANA & Python

![Python](https://img.shields.io/badge/Python-3.12-blue)
![SAP HANA](https://img.shields.io/badge/SAP%20HANA-Cloud-orange)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML-green)
![License](https://img.shields.io/badge/License-MIT-yellow)

A complete end-to-end **Customer Churn Prediction** pipeline using SAP HANA Cloud as the data backend and Python for ML modeling.

---

## 📌 Project Overview

This project predicts which telecom customers are likely to churn using classification models, with all data stored in SAP HANA Cloud.

### Pipeline
```
SAP HANA Cloud (Data Storage)
        │
        ▼
Generate Telco Customer Data (5,000 customers)
        │
        ▼
Exploratory Data Analysis
  ├── Churn rate analysis
  ├── Tenure & charges distribution
  └── Contract type impact
        │
        ▼
Feature Engineering & Train/Test Split
        │
        ▼
Classification Models
  ├── Logistic Regression  (Baseline)
  ├── Random Forest        (Ensemble)
  └── Gradient Boosting    (Best Model)
        │
        ▼
Evaluation (ROC-AUC, F1, Confusion Matrix)
        │
        ▼
Risk Segmentation → Save to SAP HANA
  ├── 🔴 High Risk Customers
  ├── 🟡 Medium Risk Customers
  └── 🟢 Low Risk Customers
```

---

## 📊 Results

| Model | Accuracy | F1 Score | ROC-AUC |
|---|---|---|---|
| Logistic Regression | ~0.78 | ~0.62 | ~0.84 |
| Random Forest | ~0.84 | ~0.71 | ~0.91 |
| **Gradient Boosting** | **~0.86** | **~0.74** | **~0.93** |

---

## 🔑 Key Findings

- **Contract Type** is the #1 churn driver — month-to-month customers churn 3x more
- **Tenure** — customers with < 12 months tenure are highest risk
- **Support Calls** — 5+ calls strongly correlates with churn
- **Monthly Charges** > $70 significantly increases churn probability

---

## 🛠️ Tech Stack

- **Database:** SAP HANA Cloud (Free Tier)
- **Language:** Python 3.12
- **Libraries:** `hana_ml`, `hdbcli`, `scikit-learn`, `pandas`, `matplotlib`, `seaborn`
- **Environment:** Google Colab




## 📁 Project Structure

```
hana-customer-churn-prediction/
│
├── 📓 customer_churn_prediction.ipynb   # Main notebook
├── 📋 README.md                         # This file
├── 📦 requirements.txt                  # Dependencies
└── 🖼️  screenshots/
    ├── churn_eda.png
    ├── churn_evaluation.png
    └── churn_drivers.png
```

---

## 📝 License
MIT License
