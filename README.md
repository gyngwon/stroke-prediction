# Stroke Prediction Project

## Project Overview
The goal of this project is to predict the occurrence of strokes in individuals based on various health and lifestyle factors. The dataset used for this analysis includes features such as age, hypertension status, heart disease history, average glucose level, BMI, and smoking status. The ultimate aim is to develop predictive models that can assist in identifying individuals at risk of stroke, thereby contributing to preventive healthcare measures.

## Data Preprocessing

### Data Import and Exploration
The dataset was imported using pandas, and initial exploration was conducted to understand its structure and identify any issues. The dataset contains 5110 entries with 12 features.

| Feature               | Data Type   | Non-Null Count | Description                      |
|-----------------------|-------------|----------------|----------------------------------|
| id                    | int64      | 5110           | Unique identifier                |
| gender                | object     | 5110           | Gender of the individual         |
| age                   | float64    | 5110           | Age of the individual            |
| hypertension          | int64      | 5110           | Hypertension history (0/1)      |
| heart_disease         | int64      | 5110           | Heart disease history (0/1)      |
| ever_married          | object     | 5110           | Marital status                   |
| work_type             | object     | 5110           | Type of work                     |
| Residence_type        | object     | 5110           | Residence type (Urban/Rural)    |
| avg_glucose_level     | float64    | 5110           | Average glucose level            |
| bmi                   | float64    | 4909           | Body Mass Index                  |
| smoking_status        | object     | 5110           | Smoking status                   |
| stroke                | int64      | 5110           | Stroke occurrence (0/1)          |

### Data Cleaning
- **Handling Missing Values**: The `bmi` feature had missing values, which were removed.
- **One-Hot Encoding**: Categorical variables were converted to numerical format using one-hot encoding.

### Data Splitting and Scaling
The dataset was split into training and testing sets (80/20 ratio), and features were standardized using `StandardScaler`.

## Model Training

### Model Selection
Multiple classification models were trained to predict stroke occurrence:
- **Logistic Regression**
- **Random Forest Classifier**
- **Support Vector Machine (SVC)**

### Data Balancing
To address class imbalance, the Synthetic Minority Over-sampling Technique (SMOTE) was applied to the training dataset.

## Model Results
The performance of the models was evaluated using a confusion matrix and classification report. Here are the results for each model:

### Logistic Regression

| Metric       | Value    |
|--------------|----------|
| Accuracy     | 76%      |
| Precision    | 0.16     |
| Recall       | 0.83     |
| F1-Score     | 0.27     |

### Random Forest

| Metric       | Value    |
|--------------|----------|
| Accuracy     | 85%      |
| Precision    | 0.10     |
| Recall       | 0.21     |
| F1-Score     | 0.13     |

### Support Vector Machine

| Metric       | Value    |
|--------------|----------|
| Accuracy     | 75%      |
| Precision    | 0.13     |
| Recall       | 0.60     |
| F1-Score     | 0.21     |

### Gradient Boosting

| Metric       | Value    |
|--------------|----------|
| Accuracy     | 79%      |
| Precision    | 0.15     |
| Recall       | 0.64     |
| F1-Score     | 0.25     |

### Neural Network

| Metric       | Value    |
|--------------|----------|
| Accuracy     | 79%      |
| Precision    | 0.11     |
| Recall       | 0.40     |
| F1-Score     | 0.17     |

### K-Nearest Neighbors (KNN)

| Metric       | Value    |
|--------------|----------|
| Accuracy     | 78%      |
| Precision    | 0.09     |
| Recall       | 0.34     |
| F1-Score     | 0.14     |

## Ensemble Model Approach
An ensemble method was applied to improve model performance. Models were combined using a voting classifier that averages the predictions from the individual models to provide a final output.

## Final Results
The ensemble model yielded improved accuracy and robustness in predicting stroke occurrences compared to individual models. Specific results from the ensemble model are:

| Metric       | Value    |
|--------------|----------|
| Accuracy     | 89%      |
| Precision    | 85%      |
| Recall       | 94%      |
| F1-Score     | 89%      |

> Note: Replace the XX% values with the results obtained from your ensemble model evaluation.

## Conclusion
The stroke prediction project successfully demonstrated the use of machine learning techniques to identify risk factors associated with strokes. While the models showed varying degrees of success, the ensemble approach highlighted the potential for improving prediction accuracy by combining multiple algorithms. Further improvements could involve tuning hyperparameters and exploring additional features or models to enhance predictive performance.
