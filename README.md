# Heart Disease Prediction using Machine Learning

An academic machine learning project that predicts the presence of heart disease using clinical attributes from the UCI Heart Disease dataset.

The project compares **Logistic Regression** and **Random Forest** models and focuses on preprocessing, exploratory data analysis, model evaluation, hyperparameter tuning, explainability, and probability-based risk categorization.

> **Disclaimer:** This project is for educational and academic purposes only. The predictions and risk categories are not clinically validated and must not be used for medical diagnosis or treatment decisions.

---

## Project Overview

Heart disease is one of the major health challenges worldwide. Machine learning can be used to identify patterns in clinical data and estimate the likelihood of heart disease.

This project transforms the original multi-class `num` target from the UCI dataset into a binary classification problem:

- `0` → No heart disease
- `1–4` → Presence of heart disease

Two machine learning approaches are implemented:

1. **Logistic Regression**
2. **Random Forest Classifier**

The models are evaluated using multiple classification metrics rather than accuracy alone.

---

## Objectives

The main objectives of this project are:

- Explore and understand the clinical dataset.
- Analyze missing values and feature distributions.
- Perform exploratory data analysis.
- Convert the original target into a binary classification problem.
- Handle numerical and categorical features appropriately.
- Build a Logistic Regression baseline.
- Build a Random Forest classifier.
- Compare model performance.
- Tune the Random Forest hyperparameters using cross-validation.
- Analyze classification errors.
- Provide probability-based risk categorization.
- Interpret model predictions using feature importance and model coefficients.

---

## Dataset

The project uses the **UCI Heart Disease dataset**.

Dataset source:

https://archive.ics.uci.edu/dataset/45/heart+disease

The version used in this project contains 920 observations and 16 columns.

### Features

| Feature | Description |
|---|---|
| `id` | Patient identifier |
| `age` | Age of the patient |
| `sex` | Biological sex |
| `dataset` | Dataset/source location |
| `cp` | Chest pain type |
| `trestbps` | Resting blood pressure |
| `chol` | Serum cholesterol |
| `fbs` | Fasting blood sugar |
| `restecg` | Resting electrocardiographic results |
| `thalch` | Maximum heart rate achieved |
| `exang` | Exercise-induced angina |
| `oldpeak` | ST depression induced by exercise |
| `slope` | Slope of the peak exercise ST segment |
| `ca` | Number of major vessels |
| `thal` | Thalassemia-related attribute |
| `num` | Original heart disease target |

The `id` column is excluded from model training because it is an identifier rather than a meaningful predictive feature.

The original `num` target is converted into a binary target:

```text
num = 0       → No disease
num > 0       → Disease
