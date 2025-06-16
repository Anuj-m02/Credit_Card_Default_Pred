# 💳 Credit Card Default Prediction

### 🏦 Finance Club — Open Project Summer 2025

This project aims to build a financially interpretable classification model to predict whether a credit card customer will default in the following month. It helps financial institutions like Bank A improve their credit risk management by enabling early intervention, better exposure management, and smarter lending decisions.

---

## 📁 Project Structure

```plaintext
📂 credit-default-model/
├── Credit_Card_Prediction.ipynb   # Main notebook (EDA + modeling + predictions)
├── train_dataset_final1.csv       # Training dataset (~25,000 records)
├── validate_dataset_final.csv     # Validation dataset (~5,000 records)
├── submission_23112018.csv        # Final submission file
├── REPORT.docx                    # Full analysis report
└── README.md                      # Project overview
```

---

## 📊 Problem Statement

> Predict whether a credit card customer will default in the upcoming month using their historical behavioral data — including bill amounts, payment history, credit utilization, and more.

---

## 🎯 Objectives

- Predict `next_month_default` (1 = default, 0 = no default)
- Perform advanced EDA and financial insight extraction
- Engineer meaningful behavioral features like:
  - Credit utilization ratio
  - Delinquency score
  - Payment ratios
- Handle class imbalance using **SMOTE**
- Evaluate and compare multiple models:
  - Logistic Regression
  - Decision Tree
  - Random Forest
  - XGBoost
  - LightGBM ✅ (final model)
- Optimize classification **threshold using F2-score**
- Generate predictions on validation dataset

---

## 📌 Key Features Engineered

- `UTILIZATION`: Average bill / credit limit
- `DELINQUENCY_SCORE`: Cumulative delay severity over 6 months
- `N_OVERDUE_MONTHS`: Count of months with overdue payments
- `PAY_RATIO1–6`: Payment-to-bill ratios per month
- `MAX_OVERDUE`: Highest delay observed

---

## 🧠 Final Model: LightGBM

| Metric       | Value   |
|--------------|---------|
| Accuracy     | 84%     |
| Recall (1)   | 35%     |
| F1 Score (1) | 46%     |
| ROC AUC      | 0.78    |
| Threshold    | ~0.38   |

**Why LightGBM?**
- High accuracy and AUC
- Supports early stopping and feature importance
- Good F1-recall tradeoff for defaulters
- Fast and scalable

---

## 📉 Business Justification

- **False negatives (missed defaulters)** are costlier than false positives
- Model prioritizes **recall** by optimizing for **F2-score**
- Enables:
  - Early warning systems
  - Credit limit adjustments
  - Risk-based segmentation and expected loss forecasting

---

## 🔎 Tools & Libraries Used

- Python
- Pandas, NumPy
- Seaborn, Matplotlib
- Scikit-learn
- Imbalanced-learn
- LightGBM, XGBoost
- SHAP (optional for interpretability)

---

## 📁 Deliverables

- `Credit_Card_Prediction.ipynb`: Complete notebook with code and analysis
- `submission_23112018.csv`: Final predictions on validation set
- `REPORT.docx`: Written report with EDA, insights, modeling and business interpretation

---

## 👨‍💻 Author

**Anuj**  
Enrollment Number: `23112018`

---

