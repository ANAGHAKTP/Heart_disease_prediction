#Heart Disease Prediction Analysis
This notebook analyzes the "Heart Disease UCI" dataset to predict heart disease using various machine learning models.

Dataset
The dataset is loaded from the /content/ucg kaggle.zip file and contains information about patients, including age, sex, chest pain type, and other medical indicators. The target variable is num, which indicates the severity of heart disease (0-4).

Analysis Steps
Data Loading and Initial Exploration: The dataset is loaded into a pandas DataFrame, and initial exploration is performed to understand the data structure, check for missing values, and get descriptive statistics.

Handle Missing Values: Missing values in numerical columns (trestbps, chol, thalch, oldpeak, ca) are imputed with the mean, and missing values in categorical columns (fbs, restecg, exang, slope, thal) are imputed with the mode.

Encode Categorical Features: Categorical features are one-hot encoded to convert them into a numerical format suitable for machine learning models.

Scale Numerical Features: Numerical features are scaled using StandardScaler to ensure they have a similar range.

Split the Data: The dataset is split into training (80%) and testing (20%) sets.

Train Models: Logistic Regression, Random Forest, and XGBoost models are trained on the training data.

Evaluate Models: The trained models are evaluated on the testing data using metrics such as Accuracy, Precision, Recall, F1-score, and ROC AUC.

Compare Models: The performance of the models is compared to identify the best performing one.

Findings
Based on the evaluation metrics on the test set:

Random Forest achieved the highest Accuracy (0.6576), Precision (0.6222), Recall (0.6576), F1-score (0.6318), and ROC AUC (0.8722).
XGBoost showed comparable performance to Random Forest, with slightly lower metrics.
Logistic Regression performed significantly lower across all metrics compared to Random Forest and XGBoost.
Conclusion
The Random Forest model appears to be the most suitable model among the evaluated options for this heart disease prediction task based on the test set performance.

Next Steps
Further hyperparameter tuning for Random Forest and XGBoost models could potentially improve their performance.
Explore other machine learning algorithms and techniques.
Perform more in-depth feature engineering.
