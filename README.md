# Lloyds Banking Group - Data Science & Analytics Internship Program

This repository contains the code and resources for the Data Science & Analytics Internship Program at Lloyds Banking Group through Forage. This program was divided into 3 tasks, each of which was designed to give me a taste of the work that data scientists and analysts do at Lloyds Banking Group. The tasks involved analyzing customer data, building predictive models, and presenting findings to stakeholders.The tasks were as follows:

1. Intro & Scenario
2. Task 1: Data gathering and exploratory analysis
3. Task 2: Building a machine learning model

## Table of Contents

- [Lloyds Banking Group - Data Science \& Analytics Internship Program](#lloyds-banking-group---data-science--analytics-internship-program)
  - [Table of Contents](#table-of-contents)
  - [Intro \& Scenario](#intro--scenario)
  - [Task 1: Data gathering and exploratory analysis](#task-1-data-gathering-and-exploratory-analysis)
  - [Task 2: Building a machine learning model](#task-2-building-a-machine-learning-model)

## Intro & Scenario

As a recent data science graduate, I'm eager to apply my skills to predict customer churn and contribute to a meaningful impact here at Lloyds Banking Group.

My initial goals for this phase are to:

- Collaborate closely with the team to understand the available data sources relevant to customer behaviour and churn.
- Begin the process of exploratory data analysis to identify initial patterns, trends, and potential relationships within the data.
- Familiarize myself with the data cleaning and preprocessing steps required to ensure data quality for model building.
- Start researching suitable predictive modelling techniques that can be applied to customer churn prediction.
- Consider potential evaluation metrics that can effectively measure the performance of the churn prediction model.

## Task 1: Data gathering and exploratory analysis

- Identified and gathered relevant data from `Customer_Demographics`, `Transaction_History`, `Customer_Service`, `Online_Activity`, and `Churn_Status` datasets to understand factors influencing customer churn.
- Documented the selection criteria, focusing on data providing insights into customer demographics, transaction patterns, service interactions, online engagement, and churn status.
- Performed Exploratory Data Analysis (EDA) using visualizations such as bar charts for churn distribution, histograms for age distribution by churn, box plots for transaction amounts, count plots for service interaction types, and scatter plots for login frequency versus service usage.
- Calculated descriptive statistics for key features like age and transaction amounts to understand data characteristics.
- Cleaned the data by noting missing values in `InteractionType` and `ResolutionStatus` for future handling.
- Standardized numerical features including `Age`, `AmountSpent`, and `LoginFrequency` using `StandardScaler` to ensure consistent scaling for model compatibility.
- Encoded categorical variables such as `Gender`, `MaritalStatus`, `ProductCategory`, `InteractionType`, and `ResolutionStatus` using one-hot encoding to convert them into a numerical format suitable for analysis.
- Merged relevant columns from all datasets into a final dataframe (`df_final`) using `CustomerID` as the key.
- Created a preliminary Customer Lifetime Value (CLV) dataset (`df_clv`) by summing the total amount spent by each customer, acknowledging the need for a more sophisticated calculation in the future.
- Prepared a comprehensive report detailing the data gathering process, EDA findings with key visualizations and statistical summaries, and the data cleaning and preprocessing steps undertaken, along with the cleaned and preprocessed dataset (`df_final`) ready for model building.

**Resources:**

- [Customer Churn Analysis Report](./Task1/Comprehensive%20Report_%20Data%20Gathering,%20EDA,%20and%20Data%20Cleaning.pdf)

## Task 2: Building a machine learning model

- Selected the Random Forest Classifier as the machine learning algorithm for predicting customer churn due to its ability to handle mixed data types, robustness to missing values, provision of feature importance, capability to capture non-linear relationships, inherent regularization, and scalability.
- Preprocessed the data by loading and merging relevant datasets, removing irrelevant columns, separating features and the target variable (`ChurnStatus`), identifying categorical and numerical features, creating separate preprocessing pipelines for each type (imputation and one-hot encoding for categorical; imputation and standardization for numerical), and splitting the data into training and testing sets with stratification.
- Trained a Random Forest Classifier model using the preprocessed training data within a pipeline that included the column transformer for feature preprocessing.
- Evaluated the model's performance on the test set using a classification report (precision, recall, F1-score), a confusion matrix (true positives, true negatives, false positives, false negatives), the ROC AUC score (0.99), and the ROC curve, demonstrating high accuracy (97%) and excellent discrimination between churned and non-churned customers.
- Suggested business recommendations based on the model's predictions, including targeted retention campaigns for high-risk customers, proactive churn prevention strategies by addressing underlying causes, customer segmentation and personalization based on churn risk, and resource optimization by focusing on valuable at-risk customers.
- Proposed potential areas for improvement, such as exploring additional feature engineering, considering simpler models for efficiency, implementing regular model updates with new data, establishing a feedback loop from retention efforts, and conducting a cost-benefit analysis of different retention strategies.
- Compiled a comprehensive report detailing the algorithm selection rationale, preprocessing steps, model training process, evaluation results with interpretations, business recommendations, and potential areas for improvement.

**Resources:**

- [Customer Churn Prediction Report](./Task2/Customer%20Churn%20Prediction%20Report.pdf)