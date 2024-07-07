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

| Random State | Test Size | Accuracy | Precision | Recall |
|--------------|-----------|----------|-----------|--------|
| 42           | 0.2       | 0.995    | 0.990     | 1.000  |
| 123          | 0.2       | 0.994    | 0.987     | 1.000  |
| 987          | 0.2       | 0.994    | 0.987     | 1.000  |
| 42           | 0.3       | 0.993    | 0.986     | 1.000  |
| 123          | 0.3       | 0.993    | 0.987     | 1.000  |
| 987          | 0.3       | 0.993    | 0.986     | 1.000  |
| 42           | 0.4       | 0.989    | 0.978     | 1.000  |
| 123          | 0.4       | 0.992    | 0.985     | 1.000  |
| 987          | 0.4       | 0.990    | 0.980     | 1.000  |

#### Average Results

| Metric          | Value |
|-----------------|-------|
| Average Accuracy| 0.992 |
| Average Precision| 0.985 |
| Average Recall  | 1.000 |
| Average F1-Score| 0.993 |
| Average ROC AUC | 0.992 |
| Average Null Accuracy| 0.50 |

### Support Vector Machines (SVM)

| Random State | Test Size | Accuracy | Precision | Recall |
|--------------|-----------|----------|-----------|--------|
| 42           | 0.2       | 0.994    | 0.987     | 1.000  |
| 123          | 0.2       | 0.994    | 0.987     | 1.000  |
| 987          | 0.2       | 0.995    | 0.990     | 1.000  |
| 42           | 0.3       | 0.993    | 0.986     | 1.000  |
| 123          | 0.3       | 0.993    | 0.987     | 1.000  |
| 987          | 0.3       | 0.993    | 0.986     | 1.000  |
| 42           | 0.4       | 0.989    | 0.979     | 1.000  |
| 123          | 0.4       | 0.991    | 0.983     | 1.000  |
| 987          | 0.4       | 0.992    | 0.983     | 1.000  |

#### Average Results

| Metric          | Value |
|-----------------|-------|
| Average Accuracy| 0.993 |
| Average Precision| 0.985 |
| Average Recall  | 1.000 |
| Average F1-Score| 0.993 |
| Average ROC AUC | 0.993 |
| Average Null Accuracy| 0.50 |

### K-Nearest Neighbors (KNN)

| Random State | Test Size | Accuracy | Precision | Recall | F1-Score |
|--------------|-----------|----------|-----------|--------|----------|
| 42           | 0.2       | 0.997    | 0.994     | 1.000  | 0.997    |
| 123          | 0.2       | 0.995    | 0.990     | 1.000  | 0.995    |
| 987          | 0.2       | 0.994    | 0.987     | 1.000  | 0.994    |
| 42           | 0.3       | 0.993    | 0.987     | 1.000  | 0.993    |
| 123          | 0.3       | 0.993    | 0.986     | 1.000  | 0.993    |
| 987          | 0.3       | 0.993    | 0.987     | 1.000  | 0.994    |
| 42           | 0.4       | 0.990    | 0.981     | 1.000  | 0.991    |
| 123          | 0.4       | 0.990    | 0.981     | 1.000  | 0.991    |
| 987          | 0.4       | 0.991    | 0.983     | 1.000  | 0.991    |

#### Average Results

| Metric          | Value |
|-----------------|-------|
| Average Accuracy| 0.993 |
| Average Precision| 0.986 |
| Average Recall  | 1.000 |
| Average F1-Score| 0.993 |
| Average ROC AUC | 0.993 |
| Average Null Accuracy| 0.50 |

### Naive Bayes

| Random State | Test Size | Accuracy | Precision | Recall | F1-Score |
|--------------|-----------|----------|-----------|--------|----------|
| 42           | 0.1       | 0.997    | 0.994     | 1.000  | 0.997    |
| 123          | 0.1       | 0.997    | 0.995     | 1.000  | 0.997    |
| 987          | 0.1       | 0.996    | 0.991     | 1.000  | 0.996    |
| 42           | 0.2       | 0.996    | 0.991     | 1.000  | 0.996    |
| 123          | 0.2       | 0.994    | 0.989     | 1.000  | 0.994    |
| 987          | 0.2       | 0.995    | 0.990     | 1.000  | 0.995    |
| 42           | 0.3       | 0.993    | 0.986     | 1.000  | 0.993    |
| 123          | 0.3       | 0.994    | 0.989     | 1.000  | 0.994    |
| 987          | 0.3       | 0.992    | 0.985     | 1.000  | 0.993    |

#### Average Results

| Metric          | Value |
|-----------------|-------|
| Average Accuracy| 0.995 |
| Average Precision| 0.990 |
| Average Recall  | 1.000 |
| Average F1-Score| 0.995 |
| Average ROC AUC | 0.995 |
| Average Null Accuracy| 0.51 |

## Conclusion

The machine learning models used in this project have shown excellent performance in predicting strokes. The Random Forest and SVM models, in particular, demonstrated high accuracy, precision, recall, and
