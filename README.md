# Loan Credit Approval Project

## Project Overview


This project aims to predict the eligibility of individuals for home loans based on key financial and personal factors such as income, credit history, loan amount, and other variables. The data belongs to Dream Housing Finance, a company that provides home loans across urban, semi-urban, and rural areas. The dataset contains demographic information like gender and education, alongside financial data such as income and credit history. Our goal is to build a machine learning model to predict whether a client is eligible to receive a loan.

## Dataset
The dataset consists of various features related to clients' demographic and financial profiles:

- Gender: Male/Female
- Education: Graduate/Not Graduate
- Married: Yes/No
- Dependents: Number of dependents
- ApplicantIncome: Income of the applicant
- CoapplicantIncome: Income of the co-applicant (if applicable)
- LoanAmount: The loan amount requested by the client
- Loan_Amount_Term: Duration of loan repayment (in months)
- Credit_History: Client's credit history (1: Good, 0: Bad)
- Property_Area: Urban/Semi-Urban/Rural
- Loan_Status: Target variable indicating loan eligibility (Y/N)

## Imbalanced Data & Evaluation Metric
The dataset is imbalanced, with the "Y" class (eligible clients) being approximately twice as frequent as the "N" class (ineligible clients). As a result, accuracy is not an ideal metric because a model could achieve high accuracy by predominantly predicting the majority class. Therefore, the F1 score is chosen as the evaluation metric, as it balances precision and recall:

- Precision: Focuses on correctly identifying ineligible individuals.
- Recall: Ensures that most ineligible individuals are detected.
- F1 Score: The harmonic mean of precision and recall, making it an appropriate choice when both precision and recall are equally important.

Given that in our scenario, predicting both eligible and ineligible clients correctly is crucial, the F1 score is a more reliable metric than accuracy.

Project Structure
LoanEligibility-EDA-ModelBuilding.ipynb: The main notebook where we perform the following steps:
Exploratory Data Analysis (EDA): Visualizations are used to extract insights, understand feature distributions, and identify correlations.
Model Building: Various machine learning models are trained to predict loan eligibility. This includes data preprocessing, model training, and evaluation based on the F1 score.
