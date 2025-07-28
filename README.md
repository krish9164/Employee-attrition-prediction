# Employee Attrition Prediction Project

This project focuses on analyzing and predicting employee attrition using machine learning techniques. It explores the key factors that contribute to employee turnover and uses multiple models to identify patterns and build a predictive system.

---

## 📁 Dataset

- **Source**: IBM HR Analytics Employee Attrition dataset  
- **Size**: 1470 rows × 35 columns  
- **Target Variable**: `Attrition` (Yes/No)

After cleaning and feature engineering:
- Final columns: 29  
- Binary encoding and one-hot encoding applied to categorical features  
- Created a new feature `YearsInOneCompany` for deeper insight

---

## 📊 Exploratory Data Analysis (EDA)

- Analyzed attrition patterns based on:
  - Business travel
  - Department
  - Education field
  - Job role
  - Marital status
  - Overtime
  - Income
  - Distance from home
  - Years at company/with manager/etc.

- Key insights:
  - Higher attrition for single employees, frequent travelers, and those with no stock options
  - Employees with lower monthly income or shorter tenure tend to leave more often

---

## 📦 Feature Engineering

- Dropped irrelevant or constant columns: `EmployeeCount`, `EmployeeNumber`, `StandardHours`, `Over18`, `HourlyRate`, `DailyRate`, `MonthlyRate`
- Added `YearsInOneCompany` = `TotalWorkingYears` / (`NumCompaniesWorked` + 1)
- Converted binary categories into 0/1 (e.g., `Attrition`, `OverTime`, `Gender`)
- Applied one-hot encoding to nominal categorical features

---

## 🤖 Models Trained

1. **Decision Tree**
   - Accuracy: 87.1%
   - AUC: 0.67

2. **Logistic Regression**
   - Accuracy: 85.7%
   - AUC: 0.82

3. **Linear Discriminant Analysis (LDA)**
   - Accuracy: 86.7%
   - AUC: 0.82

4. **K-Nearest Neighbors (KNN)**
   - Accuracy: 86.0%
   - AUC: 0.76

5. **XGBoost**
   - Accuracy: 86.7%
   - AUC: 0.83

6. **Random Forest**
   - Accuracy: 85.7%
   - AUC: 0.83

Models were tuned using GridSearchCV with cross-validation.

---

## 📈 Evaluation Metrics

- Accuracy, Precision, Recall, F1 Score
- Confusion Matrices
- ROC Curves
- Precision-Recall Curves
- Feature Importance via Information Gain (for Decision Tree)

---

## 🧪 Libraries Used

- `pandas`, `numpy`, `matplotlib`, `seaborn`
- `scikit-learn` (classification models, preprocessing, evaluation)
- `xgboost`

---

## 📌 Key Takeaways

- Attrition prediction can be improved using behavioral and demographic features.
- `YearsInOneCompany` was the most informative feature according to Information Gain.
- Models like XGBoost and LDA achieved strong performance across multiple metrics.

---
