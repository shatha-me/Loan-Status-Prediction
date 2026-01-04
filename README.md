# Loan Status Prediction

## Project Overview
Financial institutions receive thousands of loan applications every year. 
Approving loans without proper risk assessment can lead to financial losses, 
while rejecting eligible applicants affects customer trust.

This project builds a machine learning model to predict whether a loan application 
will be approved or rejected based on applicant financial and demographic information.

## Dataset
- Source: Kaggle - [Loan Predication Dataset](https://www.kaggle.com/datasets/ninzaami/loan-predication)
- Features: 12+ features including Gender, Married, Education, ApplicantIncome, LoanAmount, Credit_History, Property_Area
- Target: `Loan_Status` (Y/N)

## Steps Performed

1. **Exploratory Data Analysis (EDA)**
   - Visualized distribution of numerical and categorical features
   - Analyzed feature relationship with target
   - Identified skewed features and outliers

2. **Data Cleaning & Preprocessing**
   - Imputed missing values using median/mode
   - Encoded categorical features (LabelEncoder + One-Hot Encoding)
   - Handled `Dependents` column properly

3. **Feature Engineering**
   - Created `Total_Income` = Applicant + Coapplicant Income
   - Created `Income_Loan_Ratio`
   - Applied log transformation for skewed features

4. **Modeling**
   - Logistic Regression (Baseline)
   - SVM
   - Random Forest
   - Cross-Validation applied for stable performance

5. **Evaluation**
   - Metrics: Accuracy, Precision, Recall, F1-score, ROC-AUC
   - Confusion Matrix and Feature Importance visualization

6. **Hyperparameter Tuning**
   - GridSearchCV applied to all models
   - Tuned Random Forest selected as final model

7. **Final Model & Inference**
   - Tuned Random Forest predicts loan approval
   - Feature importance reveals Credit_History & Total_Income as most important

## Results
- Tuned Random Forest:
    - Accuracy : 0.8226
    - Precision: 0.8200
    - Recall   : 0.9535
    - F1-score : 0.8817
    - ROC-AUC  : 0.7399
- Business insight: Applicants with strong credit history and high total income are more likely to get loans approved.

**Feature Importance**

<img width="830" height="528" alt="image" src="https://github.com/user-attachments/assets/a8cdb0ff-2ed2-4508-a1a3-1a0c01d4497e" />

**Confusion Matrix**

<img width="511" height="435" alt="image" src="https://github.com/user-attachments/assets/22b76c00-22c3-4fff-aee7-a2e038c1fddd" />


<img width="511" height="435" alt="image" src="https://github.com/user-attachments/assets/ca038085-e93b-4349-9b6f-aafa32a0bfb1" />

<img width="511" height="435" alt="image" src="https://github.com/user-attachments/assets/935ec1eb-e9c0-44e9-9d0d-98537902fbb9" />

