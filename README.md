# Loan_Default_Prediction_Using_ML

This project aims to predict whether a borrower will **default on a loan** based on features such as credit grade, employment length, loan purpose, and more. We used supervised machine learning techniques on real-world data from Lending Club to build and evaluate models that can help lenders reduce risk.

---

##  Objective

To identify potential loan defaulters **before** issuing loans, enabling better credit risk assessment and minimizing financial losses for lending institutions.

---

##  Dataset

- **Source**: Lending Club (public datasets)
- **Used**: `accepted_loans.csv`
- **Target Variable**: `loan_status` (0 = Fully Paid, 1 = Charged Off)
- **Default Rate**: ~13%

---

##  Workflow

1. **Data Cleaning**: Removed data leakage features and irrelevant columns  
2. **Exploratory Data Analysis (EDA)**: Analyzed trends behind defaults  
3. **Feature Encoding**: Converted categorical variables using One-Hot and Label Encoding  
4. **Class Imbalance Handling**: Applied SMOTE to balance the target variable  
5. **Model Training**: Trained Logistic Regression, Decision Tree, Random Forest, and XGBoost  
6. **Evaluation**: Compared models based on Recall, Precision, F1-score, and ROC-AUC  

---

##  Models Compared

| Model            | Recall (Default) | Precision | ROC-AUC |
|------------------|------------------|-----------|---------|
| Logistic Regression (SMOTE) | 0.03              | 0.40      | 0.66    |
| Decision Tree (SMOTE)       | 0.26              | 0.21      | 0.65    |
|  Random Forest (SMOTE)     | 0.20              | 0.27      | **0.68** |
|  XGBoost (SMOTE)           | 0.01              | **0.43**  | **0.69** |

---

##  Best Performing Model

> **Random Forest after SMOTE** was selected as the best model due to its balance of recall and ROC-AUC — critical in catching actual defaulters.

---

##  Visualizations

Plots include:
- Confusion Matrix
- ROC Curve
- Feature Importances

You can find them in the `plots/` folder.

---

## 🛠 Requirements

Install packages using:

```bash
pip install -r requirements.txt
