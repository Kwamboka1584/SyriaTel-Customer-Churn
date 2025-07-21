#  Predictive Analysis of Customer Churn for SyriaTel Telecom
## 1. Overview
SyriaTel is a telecommunications company that, like many others in the industry, faces the challenge of customer churn (when customers discontinue their service or switch to competitors). Retaining existing customers is significantly more cost-effective than acquiring new ones, making churn reduction a key business priority.

This project aims to analyze customer behavior and build a predictive machine learning model that can identify customers at risk of churning. By understanding the factors that contribute to churn, the company can design targeted retention strategies, optimize customer service efforts, and ultimately improve profitability.

## 2. Business Understanding
Stakeholder
SyriaTel Telecom

### Business Problem
Customer churn significantly affects telecom revenue. The goal is to proactively detect customers at risk of leaving the service, allowing the business to take retention actions such as improved customer service or promotional offers.


## Data Understanding
The dataset being used for this project was obtained from kaggle.

The dataset includes information on:
- Account length
- Customer service calls
- Minutes and charges during different times of the day
- International and voice mail plans
- Churn label (target variable)

Key questions addressed:
- What features are associated with churn?
- How can we build a reliable model to predict it?


## 3. Modeling

### Data Preparation
- Null checks and cleaning
- Encoding of categorical features
- Feature scaling using StandardScaler
- Splitting into training and testing sets

### Models Used
- **Logistic Regression**: As a baseline linear model
- **Random Forest Classifier**: To capture nonlinear patterns and feature importance
- (Other models can be added iteratively in case of need)

A machine learning pipeline was used to ensure efficient and repeatable preprocessing and model training.

## 4. Evaluation

Each model was evaluated on:
- **Accuracy**
- **Precision**
- **Recall**
- **F1-Score**
- **Confusion Matrix**
- **ROC-AUC**

**Logistic Regression Findings:**
- High accuracy but low recall for churn class (imbalance issue)

**Random Forest Findings:**
- Improved recall and better F1-score on minority class
- More robust performance across metrics


