# Heart Disease Prediction Analysis

This project analyzes the Heart Disease UCI dataset to predict the presence of heart disease using different machine learning models. The goal is to clean the data, train models, evaluate them, and compare their performance.

---

## Dataset

- Dataset Used: Heart Disease UCI
- Loaded from: `/content/ucg kaggle.zip`
- Contains patient medical information such as:
  - Age, Sex, Chest Pain Type
  - Resting Blood Pressure, Cholesterol
  - ECG Results, Maximum Heart Rate, Exercise Induced Angina, etc.

Target Variable:  
`num` – indicates heart disease severity (0 to 4)

---

## Steps in the Analysis

### 1. Data Loading and Exploration
- Imported the dataset into a pandas DataFrame
- Explored data structure, checked missing values, and reviewed summary statistics

### 2. Handling Missing Values
- Numerical columns (`trestbps`, `chol`, `thalch`, `oldpeak`, `ca`) were filled with the mean
- Categorical columns (`fbs`, `restecg`, `exang`, `slope`, `thal`) were filled with the mode

### 3. Encoding Categorical Features
- One-Hot Encoding was applied to convert categorical features into numerical format

### 4. Feature Scaling
- StandardScaler was used to normalize numerical features

### 5. Splitting the Data
- Dataset was split into:
  - 80% for training
  - 20% for testing

### 6. Model Training
The following machine learning models were trained:

- Logistic Regression
- Random Forest Classifier
- XGBoost Classifier

### 7. Model Evaluation
Models were evaluated using the following metrics:

- Accuracy
- Precision
- Recall
- F1-Score
- ROC AUC

---

## Results

| Model | Accuracy | Precision | Recall | F1-Score | ROC AUC |
|--------|----------|------------|--------|-----------|----------|
| Random Forest | 0.6576 | 0.6222 | 0.6576 | 0.6318 | 0.8722 |
| XGBoost | Slightly lower than Random Forest | - | - | - | - |
| Logistic Regression | Performed lowest across all metrics | - | - | - | - |

Key Observations:
- Random Forest gave the best overall performance.
- XGBoost performed close to Random Forest.
- Logistic Regression performed the poorest.

---

## Conclusion

Based on the evaluation, the Random Forest model is the most suitable for predicting heart disease for this dataset.

---

## Future Improvements

- Perform hyperparameter tuning for Random Forest and XGBoost
- Explore additional models such as SVM, CatBoost, or Neural Networks
- Apply feature engineering and feature selection techniques
- Use cross-validation for more accurate performance evaluation
