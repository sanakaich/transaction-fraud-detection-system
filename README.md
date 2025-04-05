# Fraud Detection Using Machine Learning

## Project Overview
This project aims to build a machine learning model to proactively detect fraudulent financial transactions using a dataset containing 6,000,000 rows. The model leverages advanced techniques such as feature engineering, handling class imbalance, and hyperparameter tuning to achieve high accuracy in distinguishing fraudulent transactions from legitimate ones. The ultimate goal is to provide actionable insights for fraud prevention and mitigation.

---

## Dataset Description
The dataset contains transaction information with the following columns:
- **step**: Time unit (1 step = 1 hour)
- **type**: Type of transaction (e.g., CASH_OUT, TRANSFER, PAYMENT)
- **amount**: Transaction amount
- **nameOrig**: Identifier for the sender account
- **oldbalanceOrg**: Sender's balance before the transaction
- **newbalanceOrig**: Sender's balance after the transaction
- **nameDest**: Identifier for the recipient account
- **oldbalanceDest**: Recipient's balance before the transaction
- **newbalanceDest**: Recipient's balance after the transaction
- **isFraud**: Binary label indicating whether the transaction is fraudulent (1) or not (0)
- **isFlaggedFraud**: Binary label indicating whether the system flagged the transaction as potentially fraudulent

---

## Key Features of the Project

### 1. Data Cleaning:
- Removal of null values and handling missing data.
- Identification and treatment of outliers in transaction amounts.
- Addressing multi-collinearity among numerical features.

### 2. Feature Engineering:
- Creation of derived features such as time-based attributes (hour, day), balance differences, and transaction-to-balance ratios.
- Flags for suspicious patterns like zero balances after transactions or exact balance withdrawals.

### 3. Class Imbalance Handling:
- Application of SMOTE (Synthetic Minority Over-sampling Technique) to oversample fraudulent transactions and balance the dataset.

### 4. Model Development:
- Implementation of an XGBoost classifier optimized for binary classification.
- Hyperparameter tuning for improved performance.
- Early stopping to prevent overfitting during training.

### 5. Evaluation Metrics:
- Accuracy, precision, recall, F1-score, AUC-ROC curve, and confusion matrix.
- Threshold optimization using precision-recall curves for better fraud detection.

### 6. Visualization:
- Correlation matrix for feature relationships.
- ROC and precision-recall curves to evaluate model performance.
- Feature importance analysis for interpretability.

---

## Results & Insights
The model successfully identifies fraudulent transactions with high accuracy and recall. Key predictors include:
- Transaction type (e.g., CASH_OUT and TRANSFER are more likely associated with fraud).
- Unusual transaction amounts relative to account balances.
- Sequential patterns like transfers followed by cash-outs.
- Time-based anomalies such as transactions during unusual hours.

---
