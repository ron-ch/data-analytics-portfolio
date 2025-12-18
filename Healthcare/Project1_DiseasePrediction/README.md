# Project 1 - Disease Prediction (Diabetes Dataset)

## 📌 Problem Statement
Predict the likelihood of diabetes in patients based on clinical features.  
This project demonstrates end‑to‑end data cleaning, imputation, and modeling using the **Pima Indians Diabetes Dataset** (768 records).

## 📊 Dataset
- **Source**: Kaggle – Diabetes Dataset by Mehmet Akturk (mathchi)  
- **Size**: 768 rows × 9 columns  
- **Features**:
  - Pregnancies
  - Glucose
  - BloodPressure
  - SkinThickness
  - Insulin
  - BMI
  - DiabetesPedigreeFunction
  - Age
  - Outcome (target: 0 = non‑diabetic, 1 = diabetic)

## 🛠 Tools & Workflow
- **Alteryx Designer**: Data cleaning, imputation, workflow automation
- **Python (Pandas, Scikit‑Learn)**: Modeling and evaluation
- **Power BI**: Dashboard visualization
- **Git & GitHub**: Version control and portfolio publishing

## 🔄 Process Steps
1. **Input Data** – Load raw CSV (768 records).
2. **Browse** – Inspect dataset, identify hidden missing values (zeros).
3. **Summarize** – Compute median values for Glucose, BloodPressure, SkinThickness, Insulin, BMI.
4. **Formula + Join** – Add JoinKey, merge medians into dataset.
5. **Formula** – Replace 0’s with median values.
6. **Select** – Clean schema, drop helper fields.
7. **Browse** – Verify cleaned dataset.
8. **Output Data** – Export `data_diabetes_clean.csv`.
9. **Modeling** – Train baseline classifiers (Logistic Regression, Random Forest).
10. **Dashboard** – Visualize patient risk distribution in Power BI.

## ✅ Results
- Cleaned dataset with no biologically impossible values (e.g., BMI = 0).
- Baseline model accuracy ~75–80% (to be refined).
- Dashboard showing risk factors and prediction outcomes.

## 🧩 Workflow Diagram
![Diabetes Cleaning Workflow](../images/diabetes_cleaning_workflow.png)

The workflow includes Input, Browse, Summarize, Formula, Join, Select, and Output tools.

data-analytics-portfolio/
│── README.md                        # Portfolio overview (root)
│── Healthcare/
│   └── Project1_DiseasePrediction/
│       ├── README.md                # Project-specific documentation
│       ├── data/
│       ├── workflows/
│       ├── notebooks/
│       └── dashboard/
│       └── images/
