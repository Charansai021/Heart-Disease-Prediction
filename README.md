# ❤️ Heart Disease Prediction using Logistic Regression

A machine learning project that predicts the presence of heart disease using patient health data.  
This project focuses on **interpretability, proper preprocessing, threshold tuning, and medical relevance**, rather than black-box modeling.

---

## 📌 Project Overview

Heart disease is one of the leading causes of death worldwide.  
The goal of this project is to build an **interpretable classification model** that can predict whether a patient has heart disease based on clinical attributes.

Key highlights:
- Exploratory Data Analysis (EDA) to understand data patterns
- Proper preprocessing and feature encoding
- Logistic Regression with regularization
- Threshold tuning for healthcare-sensitive decisions
- Model evaluation using multiple metrics
- Clear feature importance interpretation

---

## 📂 Dataset Information

- **Dataset:** Heart Disease Dataset  
- **Records:** 1025 patients  
- **Target Variable:**  
  - `1` → Heart disease present  
  - `0` → No heart disease  

### Features:
- `age` – Age of the patient  
- `sex` – Gender (1 = Male, 0 = Female)  
- `cp` – Chest pain type  
- `trestbps` – Resting blood pressure  
- `chol` – Serum cholesterol  
- `fbs` – Fasting blood sugar  
- `restecg` – Resting ECG results  
- `thalach` – Maximum heart rate achieved  
- `exang` – Exercise-induced angina  
- `oldpeak` – ST depression induced by exercise  
- `slope` – Slope of peak exercise ST segment  
- `ca` – Number of major vessels  
- `thal` – Thalassemia  

---

## 🔍 Exploratory Data Analysis (EDA)

EDA was performed to understand:
- Feature distributions
- Differences between patients with and without heart disease
- Correlations between features and the target variable

### Key Insights:
- Chest pain type (`cp`) is the strongest predictor
- Maximum heart rate (`thalach`) is higher in patients with heart disease
- Exercise-related features (`oldpeak`, `slope`, `exang`) are highly influential
- Cholesterol alone is not a strong indicator

A correlation heatmap was used to identify the most impactful features.

---

## ⚙️ Data Preprocessing

Steps performed:
1. Checked for missing values (none found)
2. Converted categorical variables using **One-Hot Encoding**
3. Standardized numerical features
4. Train-test split (80/20)

Preprocessing ensures compatibility with Logistic Regression and prevents data leakage.

---

## 🤖 Model Building

- **Algorithm:** Logistic Regression  
- **Variants Tested:**
  - Baseline Logistic Regression
  - L2 Regularization (Ridge)
  - L1 Regularization (Lasso)

Regularization was used to improve stability and interpretability.

---

## 📊 Model Evaluation

### Performance Metrics:
- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- Confusion Matrix
- ROC Curve

### Best Results:
- **Accuracy:** ~87%
- **ROC-AUC:** ~0.94
- **High Recall:** Suitable for medical screening

---

## 🎯 Threshold Tuning

Instead of relying on the default threshold (0.5), multiple thresholds were evaluated.

| Threshold | Precision | Recall | F1-score |
|----------|----------|--------|----------|
| 0.3 | 0.785 | 0.971 | 0.868 |
| 0.4 | 0.832 | 0.943 | **0.884** |
| 0.5 | 0.856 | 0.905 | 0.880 |
| 0.6 | 0.885 | 0.876 | 0.880 |

**Optimal threshold:** `0.4`  
This provides the best balance between recall and precision, minimizing missed heart disease cases.

---

## 🔑 Feature Importance

Top contributing features:
- Chest pain type (`cp`)
- Number of major vessels (`ca`)
- Thalassemia (`thal`)
- ST segment slope (`slope`)
- Maximum heart rate (`thalach`)



## 📁 Project Structure

