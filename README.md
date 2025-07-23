#  Predictive Analysis of Customer Churn for SyriaTel Telecom

![](https://daxg39y63pxwu.cloudfront.net/images/blog/churn-models/Customer_Churn_Prediction_Models_in_Machine_Learning.png)

## 1. Overview
SyriaTel is a telecommunications company that, like many others in the industry, faces the challenge of customer churn (when customers discontinue their service or switch to competitors). Retaining existing customers is significantly more cost-effective than acquiring new ones, making churn reduction a key business priority.

This project aims to analyze customer behavior and build a predictive machine learning model that can identify customers at risk of churning. By understanding the factors that contribute to churn, the company can design targeted retention strategies, optimize customer service efforts, and ultimately improve profitability.

## 2. Business Understanding
Stakeholder: SyriaTel Telecom

### Business Problem
Customer churn significantly affects telecom revenue. The goal is to proactively detect customers at risk of leaving the service, allowing the business to take retention actions such as improved customer service or promotional offers.


## Data Understanding
The dataset being used for this project was obtained from kaggle.

The dataset has 3,333 customer records, including information on:
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
- **Decision Tree Classifier** - a supervised machine learning algorithm used for classification tasks.
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
![Confusion Matrix](images/Logistic%20Regression%20confusion%20matrix.png)

**Decision Tree Findings**
- The Decision Tree model achieved an AUC score of 0.84, indicating strong capability in distinguishing customers likely to churn from those who will stay.
![](images/Dec%20Tree%20confusion%20matrix.png)

**Random Forest Findings:**
- Improved recall and better F1-score on minority class
- More robust performance across metrics
![RF confusion matrix](images/Random%20Forest%20Confusion%20Matrix.png)

**Comparison of the three models**

## Model Performance comparison Table

| **Metric**            | **Logistic Regression** | **Random Forest** | **Decision Tree** |
| --------------------- | ----------------------- | ----------------- | ----------------- |
| **Accuracy**          | 91.3%                   | 94.1%             | 92.5%             |
| **Precision (Churn)** | \~0.67                  | \~0.84            | 0.75              |
| **Recall (Churn)**    | \~0.66                  | \~0.82            | 0.76              |
| **F1-Score (Churn)**  | \~0.66                  | \~0.83            | 0.75              |
| **ROC-AUC**           | \~0.89                  | \~0.96            | \~0.91            |

Bar Graph comparison of the models
![Performance Comparison](images/Model%20Performance%20Comparison.png)


## 5. Conclusion

Use Random Forest as your production model since it offers strong performance and a great balance of precision and recall. Logistic Regression can be kept for comparison, or to provide a baseline.

The model successfully identifies patterns associated with churn, particularly:
- High number of customer service calls
- High day-time call charges

**Next Steps:**
- Use SMOTE or class weighting to further address class imbalance
- Deploy the model for real-time scoring
- Collaborate with business teams for retention campaigns based on predictions

--- 
This project was developed by:
- *Pacificah Kwamboka Asamba* ([email](mailto:sikamboga1@gmail.com)) | [LinkedIn](https://www.linkedin.com/in/pacificah-omboga-42959b83/)
