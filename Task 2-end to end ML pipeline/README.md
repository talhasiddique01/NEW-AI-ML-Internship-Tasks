# Task 2 ## Customer Churn Prediction – End-to-End Machine Learning Pipeline

## Objective of the Task
The objective of this task is to design and implement a reusable, scalable, and production-ready
machine learning pipeline to predict customer churn using the Telco Customer Churn dataset.
The goal is to identify customers who are likely to discontinue services, enabling businesses
to take proactive retention measures.

This task focuses on building an end-to-end ML workflow using Scikit-learn’s Pipeline API,
ensuring clean preprocessing, effective model training, and seamless deployment readiness.

---

## Dataset Description
The Telco Customer Churn dataset contains information about customers, including:
- Demographic details (gender, senior citizen status)
- Account information (tenure, contract type, payment method)
- Service usage (internet service, phone service, streaming)
- Target variable: **Churn** (Yes / No)

---

## Methodology / Approach

### 1. Data Loading and Exploration
- Loaded the dataset using Pandas
- Analyzed feature distributions and target class imbalance
- Identified categorical and numerical features

### 2. Data Preprocessing
To ensure clean and consistent data handling:
- Missing values were handled appropriately
- Numerical features were scaled using **StandardScaler**
- Categorical features were encoded using **OneHotEncoder**
- A **ColumnTransformer** was used to apply transformations efficiently

### 3. Pipeline Construction
A complete end-to-end pipeline was constructed using Scikit-learn:
- Integrated preprocessing steps and model training into a single pipeline
- This approach ensures reusability, maintainability, and prevention of data leakage

### 4. Model Development
Two machine learning models were implemented and compared:
- **Logistic Regression** (baseline interpretable model)
- **Random Forest Classifier** (non-linear ensemble model)

### 5. Hyperparameter Tuning
- Used **GridSearchCV** to optimize model hyperparameters
- Performed cross-validation to ensure robust model performance
- Selected the best model based on F1-score and ROC-AUC metrics

### 6. Model Evaluation
Models were evaluated using:
- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix
- ROC-AUC Score

### 7. Model Export
- The final trained pipeline was exported using **joblib**
- This allows the pipeline to be directly reused for inference or deployment without retraining

---

## Key Results / Observations

### Model Performance Summary
- Logistic Regression provided a strong baseline with good interpretability
- Random Forest outperformed Logistic Regression in most evaluation metrics

### Detailed Observations
- **Random Forest achieved higher recall**, making it more effective at identifying churned customers
- Feature preprocessing within the pipeline significantly improved consistency and reliability
- Customers with **short tenure**, **month-to-month contracts**, and **higher monthly charges**
  showed a higher likelihood of churn
- The pipeline-based approach reduced code complexity and improved reproducibility

### Final Model Selection
- **Random Forest Classifier** was selected as the final model due to better overall performance
- The exported pipeline can be directly used in production environments for real-time predictions

---

## Skills Gained
- End-to-end ML pipeline construction using Scikit-learn
- Feature preprocessing with ColumnTransformer
- Hyperparameter tuning using GridSearchCV
- Model evaluation using multiple performance metrics
- Model persistence and reusability using joblib
- Writing clean, production-ready ML code

---

## Tools & Technologies
- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib / Seaborn
- Joblib

---

