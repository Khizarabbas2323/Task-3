# Task-3
Churn Modelling

# Customer Churn Prediction

## 🧠 Task Objective

The goal of this project is to build a machine learning model that can predict whether a bank customer will **churn** (i.e., leave the bank). Accurately predicting churn helps banks take proactive measures to retain customers and improve satisfaction.

---

## 🔍 Approach

### 1. **Data Preparation**
- Loaded the dataset `Churn_Modelling.csv`
- Dropped unnecessary columns: `RowNumber`, `CustomerId`, and `Surname`
- Handled categorical variables:
  - `Gender`: Label Encoding (Male/Female → 1/0)
  - `Geography`: One-Hot Encoding (France, Germany, Spain)

### 2. **Model Training**
- Used `RandomForestClassifier` from Scikit-learn
- Split dataset into training and test sets (80/20)
- Trained the model on customer demographic and account-related features

### 3. **Model Evaluation**
- Evaluated using:
  - Accuracy Score
  - Confusion Matrix
  - Classification Report (Precision, Recall, F1-score)
- Analyzed feature importances to understand which factors most influence churn

---

## 📊 Results and Insights

### 🔹 Model Performance
- **Accuracy:** ~86% on test data (depending on train/test split)
- **Precision and Recall:** High precision for detecting non-churners; room for improvement on recall for churners

### 🔹 Key Feature Importances
- **Age**: Older customers tend to churn more
- **Balance**: Customers with high balance but no activity are more likely to churn
- **Geography**: Customers from certain regions (e.g., Germany) showed higher churn rates
- **IsActiveMember**: Inactive members churn more frequently
- **CreditScore**: Somewhat important but less than expected

### 🔹 Insight
- The model identifies important churn drivers effectively
- Could be further improved with more features (e.g., customer support interactions, complaints)

---

## 🚀 Next Steps (Optional Enhancements)

- Try advanced models (e.g., XGBoost, CatBoost)
- Use SHAP or LIME for explainable AI
- Deploy as a REST API or Streamlit dashboard

---

## 📁 Project Structure

```text
churn-prediction/
│
├── Churn_Modelling.csv
├── churn_prediction.py
├── README.md
└── requirements.txt


