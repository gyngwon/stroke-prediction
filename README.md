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
- **Gradient Boosting**
- **Neural Network**
- **K-Nearest Neighbors (KNN)**

### Data Balancing
To address class imbalance, the Synthetic Minority Over-sampling Technique (SMOTE) was applied to the training dataset.

## Model Results
The performance of the models was evaluated using a confusion matrix and classification report. 


| Model                              | Accuracy | Precision | Recall | F1-Score |
|------------------------------------|----------|-----------|--------|----------|
| Logistic Regression                | 76%      | 0.16      | 0.83   | 0.27     |
| Random Forest                      | 85%      | 0.10      | 0.21   | 0.13     |
| Support Vector Machine (SVC)      | 75%      | 0.13      | 0.60   | 0.21     |
| Gradient Boosting                  | 79%      | 0.15      | 0.64   | 0.25     |
| Neural Network                     | 79%      | 0.11      | 0.40   | 0.17     |
| K-Nearest Neighbors (KNN)         | 78%      | 0.09      | 0.34   | 0.14     |


## Ensemble of Gradient Boosting and Neural Network to Better Predict the Minority Class (Stroke Cases)
- **Stratified K-Fold Cross-Validation**: Use `StratifiedKFold` to ensure that the minority class is evenly distributed across each fold.
- **Defining Gradient Boosting and Neural Network Models**: Define `GradientBoostingClassifier` and `MLPClassifier`, and train each model to predict both the minority and majority classes effectively.
- **Ensemble Using VotingClassifier**: Use `VotingClassifier` to ensemble the two models. The `voting='soft'` option sums the predicted probabilities from each model to make the final prediction, potentially improving the prediction performance for the minority class.
- **Cross-Validation Evaluation**: For each fold, assess the precision, recall, and F1 score for the minority class (1) based on the prediction results, and finally summarize the average performance.

## Final Results
The ensemble model yielded improved accuracy and robustness in predicting stroke occurrences compared to individual models. Specific results from the ensemble model are:

| Metric       | Value    |
|--------------|----------|
| Accuracy     | 89%      |
| Precision    | 85%      |
| Recall       | 94%      |
| F1-Score     | 89%      |

## Conclusion
The stroke prediction project successfully demonstrated the use of machine learning techniques to identify risk factors associated with strokes. While the models showed varying degrees of success, the ensemble approach highlighted the potential for improving prediction accuracy by combining multiple algorithms. Further improvements could involve tuning hyperparameters and exploring additional features or models to enhance predictive performance.
