# Loan-Approval-Prediction

Overview
This project focuses on building a robust Machine Learning model to predict whether a loan application will be approved or rejected. In the fintech industry, such predictive systems are crucial for automating decision-making, assessing credit risk more accurately, and enhancing the efficiency of the loan disbursement process for banks and financial institutions.

Problem Statement
The core problem addressed is: To accurately predict loan approval status (approved or rejected) for applicants, enabling financial institutions to automate decision-making, mitigate lending risks, and optimize their loan processing efficiency.

Dataset
The project utilizes a dataset containing various applicant details and loan characteristics, including:

Demographic information (Gender, Marital Status, Dependents, Education, Self-Employment)

Financial details (Applicant Income, Co-applicant Income, Loan Amount, Loan Amount Term)

Credit history

Property area

Loan Status (the target variable: 'Y' for approved, 'N' for rejected)

Methodology & Workflow
The project follows a standard machine learning pipeline:
Data Loading: The raw loan application data was loaded into a Pandas DataFrame.

Data Preprocessing:

Irrelevant identifier columns (Loan_ID) were removed.

Missing values in categorical features (Gender, Married, Dependents, Self_Employed) were imputed using their modes.

Missing values in numerical features (LoanAmount, Loan_Amount_Term, Credit_History) were imputed using the median or mode, as appropriate.

Feature Engineering:

The 'Dependents' column was cleaned and converted to a numerical type.

A new feature, TotalIncome (sum of Applicant Income and Co-applicant Income), was created to provide a consolidated view of financial capacity.

Categorical Encoding: All remaining categorical features were converted into numerical representations using One-Hot Encoding. The target variable (Loan_Status) was mapped to numerical 1 (Approved) and 0 (Rejected).

Data Splitting: The dataset was divided into 80% training and 20% testing sets to train and evaluate models effectively.

Feature Scaling: Numerical features were scaled using StandardScaler to normalize their ranges, which helps various machine learning algorithms perform better.

Model Training & Evaluation: Two classification models were trained and rigorously evaluated.

Okay, here's a description tailored for your GitHub repository's README.md file for the Loan Approval Prediction project. It covers all the essential aspects and is designed to be easily understandable for visitors to your repository.

Loan Approval Prediction with Machine Learning
Overview
This project focuses on building a robust Machine Learning model to predict whether a loan application will be approved or rejected. In the fintech industry, such predictive systems are crucial for automating decision-making, assessing credit risk more accurately, and enhancing the efficiency of the loan disbursement process for banks and financial institutions.

Problem Statement
The core problem addressed is: To accurately predict loan approval status (approved or rejected) for applicants, enabling financial institutions to automate decision-making, mitigate lending risks, and optimize their loan processing efficiency.

Dataset
The project utilizes a dataset containing various applicant details and loan characteristics, including:

Demographic information (Gender, Marital Status, Dependents, Education, Self-Employment)

Financial details (Applicant Income, Co-applicant Income, Loan Amount, Loan Amount Term)

Credit history

Property area

Loan Status (the target variable: 'Y' for approved, 'N' for rejected)

Methodology & Workflow
The project follows a standard machine learning pipeline:

Data Loading: The raw loan application data was loaded into a Pandas DataFrame.

Data Preprocessing:

Irrelevant identifier columns (Loan_ID) were removed.

Missing values in categorical features (Gender, Married, Dependents, Self_Employed) were imputed using their modes.

Missing values in numerical features (LoanAmount, Loan_Amount_Term, Credit_History) were imputed using the median or mode, as appropriate.

Feature Engineering:

The 'Dependents' column was cleaned and converted to a numerical type.

A new feature, TotalIncome (sum of Applicant Income and Co-applicant Income), was created to provide a consolidated view of financial capacity.

Categorical Encoding: All remaining categorical features were converted into numerical representations using One-Hot Encoding. The target variable (Loan_Status) was mapped to numerical 1 (Approved) and 0 (Rejected).

Data Splitting: The dataset was divided into 80% training and 20% testing sets to train and evaluate models effectively.

Feature Scaling: Numerical features were scaled using StandardScaler to normalize their ranges, which helps various machine learning algorithms perform better.

Model Training & Evaluation: Two classification models were trained and rigorously evaluated.

Models Used
Random Forest Classifier: An ensemble learning method that builds multiple decision trees and merges their predictions to improve accuracy and control overfitting.

Logistic Regression: A fundamental linear model widely used for binary classification problems, providing interpretable coefficients.

Performance & Results
Both models demonstrated strong performance in predicting loan approval status on the test set:

Metric	    Random Forest Classifier     	Logistic Regression
Accuracy          	0.8780                    	0.8618
Precision         	0.8723                      0.8400
Recall	            0.9647	                    0.9882
F1-Score	          0.9162	                    0.9081
ROC AUC Score	      0.8334	                    0.8486


