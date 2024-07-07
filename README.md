# Stroke Prediction Using Machine Learning

This project aims to predict the likelihood of stroke in patients using various machine learning techniques. The dataset contains various features like gender, age, hypertension status, heart disease status, marital status, work type, residence type, average glucose level, BMI, and smoking status.

## Project Overview

In this project, four different machine learning models are used to predict stroke:

- Random Forest
- Support Vector Machines (SVM)
- K-Nearest Neighbors (KNN)
- Naive Bayes

## Dataset

The dataset used in this project contains the following features:

- **id**: Unique identifier
- **gender**: "Male", "Female" or "Other"
- **age**: Age of the patient
- **hypertension**: 0 if the patient doesn’t have hypertension, 1 if the patient has hypertension
- **heart_disease**: 0 if the patient doesn’t have any heart diseases, 1 if the patient has a heart disease
- **ever_married**: "No" or "Yes"
- **work_type**: "children", "Govt_job", "Never_worked", "Private", or "Self-employed"
- **Residence_type**: "Rural" or "Urban"
- **avg_glucose_level**: Average glucose level in blood
- **bmi**: Body mass index
- **smoking_status**: "formerly smoked", "never smoked", "smokes", or "Unknown"

## Handling Missing Values

The dataset contains 201 missing values in the BMI feature. To address this, the KNN imputer was used to estimate the missing values based on the closest neighbors in the dataset.

## Imbalanced Data

The dataset is imbalanced, with significantly more stroke-free patients than patients who have had a stroke. To address this, oversampling techniques were employed to balance the class distribution.

## Models and Results

### Random Forest

- **Average Accuracy**: 0.992
- **Average Precision**: 0.985
- **Average Recall**: 1.000
- **Average F1-Score**: 0.993
- **Average ROC AUC**: 0.992

### Support Vector Machines (SVM)

- **Average Accuracy**: 0.993
- **Average Precision**: 0.985
- **Average Recall**: 1.000
- **Average F1-Score**: 0.993
- **Average ROC AUC**: 0.993

### K-Nearest Neighbors (KNN)

- **Average Accuracy**: 0.993
- **Average Precision**: 0.986
- **Average Recall**: 1.000
- **Average F1-Score**: 0.993
- **Average ROC AUC**: 0.993

### Naive Bayes

- **Average Accuracy**: 0.995
- **Average Precision**: 0.990
- **Average Recall**: 1.000
- **Average F1-Score**: 0.995
- **Average ROC AUC**: 0.995

## Conclusion

The machine learning models used in this project have shown excellent performance in predicting strokes. The Random Forest and SVM models, in particular, demonstrated high accuracy, precision, recall, and F1-score. KNN and Naive Bayes also performed well, indicating the robustness of these techniques in medical prediction tasks.
