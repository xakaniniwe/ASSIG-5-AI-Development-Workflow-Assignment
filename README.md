# ASSIG-5-AI-Development-Workflow-Assignment
# Predictive Modelling Projects
### Authors: Veronica Moshesha, Moleboheng Madela, Niniwe Xaka

---

## 📌 Project 1: Teenage Pregnancy Risk Prediction

### 🧠 Overview

This project focuses on building a **predictive machine learning model** to assess the risk of teenage pregnancy using socio-economic, educational, and behavioural data. The ultimate goal is to enable **targeted interventions**, support **policy decisions**, and reduce teenage pregnancy rates.

### 🎯 Objectives

- Identify adolescents at high risk for pregnancy early on.
- Support public health planning through data-driven risk assessments.
- Optimize intervention and resource allocation.

### 👥 Stakeholders

- Government Health Departments
- Educational Institutions and Policy Makers

### 🧮 Key Performance Indicator

- **Predictive Accuracy** of identifying high-risk and low-risk individuals.

---

### 📊 Data Collection & Preprocessing

- **Sources**:
  - National Health and Demographic Surveys
  - School Administrative Records
- **Challenges**: 
  - Underreporting due to stigma
- **Steps**:
  - Missing data imputation
  - Encoding categorical variables
  - Normalization of numerical features

---

### 🏗️ Model Development

- **Model Used**: Random Forest Classifier
- **Rationale**: Handles mixed data, robust to overfitting, interpretable via feature importance
- **Data Split**:
  - Training: 70%
  - Validation: 15%
  - Test: 15%
- **Hyperparameters Tuned**:
  - Number of Trees
  - Maximum Tree Depth

---

### 📈 Evaluation & Deployment

- **Metrics**:
  - Accuracy
  - F1-Score (emphasis on recall)
- **Concept Drift**:
  - Regular re-evaluation and retraining
- **Deployment Challenges**:
  - Scalability
  - Data privacy
  - System integration

---

## 📌 Project 2: Patient Readmission Risk Prediction

### 🧠 Overview

A machine learning model to predict **30-day hospital readmissions**, aimed at improving patient outcomes and reducing healthcare costs.

### 🎯 Objectives

- Early risk identification at discharge
- Tailored interventions (e.g., telehealth, follow-ups)
- Quality improvement & cost reduction

### 👥 Stakeholders

- Healthcare Providers
- Hospital Administrators

---

### 📊 Data Strategy

- **Dataset**: diabetic_data.csv (EHR-based)
- **Key Features**:
  - Diagnoses, emergency visits, medications, demographics
- **Ethical Concerns**:
  - Data privacy (HIPAA, POPIA)
  - Bias in historical data

---

### 🔄 Preprocessing Pipeline

1. Clean and impute missing data
2. Binary target engineering (`readmitted_30d`)
3. Drop IDs to prevent leakage
4. Encode categorical variables
5. Scale features
6. Train/test split with stratification

---

### 🏗️ Model Development

- **Model Used**: Gradient Boosting Classifier
- **Performance**:
  - Excellent at predicting non-readmissions
  - Very low recall for actual readmissions (highlighting class imbalance)

---

### 🚀 Deployment Plan

- REST API (Flask/FastAPI)
- Integration with EHR systems
- Clinician training & workflow embedding
- HIPAA-compliant data handling

---

### 🧪 Optimization

- Use of GridSearchCV for hyperparameter tuning
- Focus on maximizing **recall**
- Address class imbalance via SMOTE or sample weighting

---

## 🔍 Critical Thinking

### ⚖️ Ethics & Bias

- **Risks**: Bias can reinforce healthcare disparities
- **Mitigation**: Sample weighting, fairness audits, stakeholder involvement

### 🧭 Interpretability vs Accuracy

- Trade-off between explainability and performance
- Healthcare models should prioritize **interpretability**

### ⚙️ Resource Constraints

- Consider simpler models like **Logistic Regression** for low-resource settings

---

## 🧠 Reflection

- **Biggest Challenge**: Severe class imbalance
- **Improvements**:
  - Advanced resampling
  - Hyperparameter tuning
  - Domain expert collaboration

---

## 🔄 AI Development Workflow

```text
1. Problem Definition
2. Data Collection
3. Preprocessing
4. Model Development
5. Evaluation
6. Deployment
7. Monitoring & Updates

## 📚 License
This project is for educational and research purposes only.
