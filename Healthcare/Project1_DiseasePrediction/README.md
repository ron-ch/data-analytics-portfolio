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

## 🔄 Process Steps (Alteryx)
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

## 📊 Modeling and Evaluation (Python)
- Logistic Regression baseline accuracy: ~75–80%
- Random Forest baseline accuracy: ~78–82%
- Evaluation metrics included Precision, Recall, F1-score, and ROC curve

## Sections:
Data Import: Load data_diabetes_clean.csv
Exploratory Analysis: Quick stats, distributions
Train/Test Split: 70/30 or 80/20
Baseline Models: Logistic Regression, Random Forest
Evaluation Metrics: Accuracy, Precision, Recall, F1, ROC Curve

# Diabetes Prediction: Logistic Regression vs Random Forest

## 📌 Project Overview
This project applies machine learning to predict diabetes using patient health metrics.  
Two models were compared:
- **Logistic Regression** → interpretable, transparent coefficients.
- **Random Forest** → robust, nonlinear, higher recall and accuracy.

The notebook demonstrates end-to-end workflow: preprocessing, modeling, evaluation, ROC curves, and calibration curves.

---

## ⚙️ Workflow
1. **Data Preprocessing**
   - Class balance check
   - Scaling for Logistic Regression
   - Exploratory analysis (histograms, correlations)

2. **Modeling**
   - Logistic Regression baseline + threshold tuning
   - Random Forest with class balancing + feature importance

3. **Evaluation**
   - Confusion matrices
   - Classification reports
   - ROC curve comparison (AUC)
   - Calibration curves (probability reliability)

4. **Comparison**
   - Side-by-side metrics table
   - Grouped bar charts for precision, recall, F1, accuracy

---

## 📊 Key Results
- Logistic Regression: Accuracy **0.71**, Diabetic Recall **0.50**, better calibration.
- Random Forest: Accuracy **0.75**, Diabetic Recall **0.78**, stronger discrimination (AUC ~0.80).
- ROC curves show Random Forest separates classes better.
- Calibration curves show Logistic Regression provides more reliable probabilities.

---

## 🎯 Recruiter Narrative
This project demonstrates:
- Ability to balance **interpretability vs robustness**.
- Use of **threshold tuning** to prioritize healthcare-specific metrics.
- Advanced evaluation with **ROC and calibration curves**.
- Clear communication of trade-offs for recruiter and stakeholder audiences.

---

## 📂 Repository Structure
- `notebooks/diabetes_prediction.ipynb` → Full modeling workflow.
- `data/` → Dataset.
- `README.md` → Project summary (this file).

---

## 🚀 Next Steps (Not included in this project)
- Add ROC and PR curves for deeper evaluation.
- Explore calibration methods (Platt scaling, isotonic regression).
- Extend to other models (XGBoost, SVM) for comparison.

---

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

data-analytics-portfolio/Healthcare/diabetes-prediction/
│
├── README.md                  # Root-level project summary
├── requirements.txt            # Dependencies
├── .gitignore                  # Ignore checkpoints, envs, etc.
│
├── notebooks/
│   └── diabetes_prediction.ipynb   # Full modeling workflow
│
├── images/
│   ├── Alteryx_Workflow_Images/    # Organized Alteryx workflow screenshots
│   │   ├── workflow1.png
│   │   ├── workflow2.png
│   │   └── workflow3.png
│   │
│   └── Python_Images/              # Visuals from Python (plots, charts)
│       ├── roc_curve.png
│       ├── calibration_curve.png
│       └── comparison_chart.png
