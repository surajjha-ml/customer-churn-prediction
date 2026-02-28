# Customer Churn Prediction — End-to-End ML Project

## 📌 Project Overview

This project builds an end-to-end Machine Learning pipeline to predict customer churn in a telecom business.

The objective is to identify customers at high risk of leaving within the next 30 days so that the business can take proactive retention actions.

This project focuses not only on predictive performance but also on:
- Business alignment
- Data leakage prevention
- Model interpretability
- Deployment realism

---

## 🎯 Business Objective

Customer retention is typically more cost-effective than customer acquisition.  
By predicting churn probability, the business can:

- Prioritize high-risk customers
- Optimize retention budget allocation
- Improve Customer Lifetime Value (LTV)
- Increase overall revenue stability

Churn is defined as a customer leaving within a 30-day forward window.

---

## 📊 Dataset

- Telco customer churn dataset
- Contains customer demographics, contract details, billing information, and service usage features
- Target variable: `Churn` (Yes/No)

---

## 🧠 Project Structure

The project is divided into modular notebooks:

00_business_understanding  
01_data_understanding  
02_eda  
03_feature_engineering  
04_modeling  

This modular design improves:
- Reproducibility
- Clarity
- Production realism

---

## 🔍 Key Steps

### 1️⃣ Business Understanding
- Defined churn window (30-day forward-looking definition)
- Framed problem as cost-sensitive classification
- Identified operational constraints

### 2️⃣ Data Understanding & Leakage Prevention
- Identified potential leakage risks
- Ensured snapshot-based modeling setup
- Verified proper train-test separation

### 3️⃣ Exploratory Data Analysis
- Univariate and bivariate analysis
- Churn rate analysis across segments
- Identified strong predictors (tenure, contract type, monthly charges)

### 4️⃣ Feature Engineering
- Data type corrections
- Missing value handling
- One-hot encoding for categorical variables
- Stratified train-test split
- Deferred scaling to modeling stage to prevent leakage

### 5️⃣ Modeling
Models implemented:
- Logistic Regression (baseline, interpretable)
- Random Forest
- XGBoost (best performing)

Evaluation metric:
- ROC-AUC (primary)
- Precision, Recall, Confusion Matrix

Best Model:
- XGBoost
- ROC-AUC ≈ 0.84

---

## 🔎 Model Interpretability

SHAP (SHapley Additive exPlanations) was used to:

- Identify global feature importance
- Explain individual churn predictions
- Ensure transparency for business stakeholders

Top churn drivers:
- Tenure
- Contract type
- Monthly charges
- Payment method

Note: SHAP explains model behavior, not causal relationships.

---

## 📈 Business Application

The model can be deployed in batch mode (e.g., weekly):

1. Score active customers
2. Rank by churn probability
3. Target top-risk segment
4. Measure retention campaign impact

Future improvements:
- Uplift modeling
- ROI simulation
- Time-based validation
- Drift monitoring

---

## 🚀 Deployment Considerations

- Batch scoring preferred over real-time
- Monitor ROC-AUC and segment churn rates
- Track feature distribution drift
- Retrain periodically

---

## ⚠️ Limitations

- Snapshot-based validation (no time-based split)
- No causal uplift modeling
- No direct ROI simulation
- Public dataset (structured and relatively clean)

---

## 🛠 Tech Stack

- Python
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- SHAP
- Matplotlib / Seaborn
- Jupyter Notebook

---

## 📌 Key Takeaways

This project demonstrates:

- End-to-end ML workflow
- Business-aware modeling
- Leakage prevention awareness
- Model comparison strategy
- Interpretability with SHAP
- Deployment thinking
