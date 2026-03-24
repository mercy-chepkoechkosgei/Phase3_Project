## **Modeling Customer Churn in Telecommunications using Machine Learning**
 ### Project Overview

This project aims to predict customer churn for SyriaTel, a telecommunications company, using logistic regression. Churn prediction is critical for the company to proactively identify customers at risk of leaving, allowing targeted retention strategies and minimizing revenue loss. The analysis includes data preprocessing, exploratory analysis, model building, class balancing with SMOTE, and model evaluation using metrics such as accuracy, recall, precision, confusion matrix, and ROC-AUC.

### Business and Data Understanding

The goal of this project is to support SyriaTel’s customer retention efforts by modeling customer churn.

**Bussiness Stakeholder**: SyriaTel’s management and marketing teams who are responsible for retention campaigns and service improvement.

**Dataset Choice**: The dataset contains 3333 customer records with 21 features including demographic information, service plans, usage metrics (day, evening, night, international calls), and customer service calls.

**Key Observations**:
Most customers (~85%) did not churn, making the dataset imbalanced.
Features like customer service calls and total day minutes have high correlation with churn, indicating potential drivers of customer churn.

###  Logistic regression models:

**Baseline Model**:
Logistic regression without class balancing
Standard training and evaluation
Handled categorical features by one-hot encoding

**Improved Model**:
Applied SMOTE to balance the training dataset
Logistic regression using the liblinear solver and tuned iterations
Scaled numerical features.
Objective: improve detection of churners (increase recall)
### Evaluation

**Baseline Model Metrics**:

Accuracy: ~84%

Recall: ~12% (poor detection of actual churners)

Precision: ~48%

ROC-AUC: 0.74

**Improved Model Metrics**:

Accuracy: 77.7%

Recall: ~77%, effectively identifies most churners

Precision: ~38%

ROC-AUC: 0.83, significantly better separating between churners and non-churners


### Key Findings:
Customer service calls and total day minutes are strong predictors of churn.
Balancing the dataset improved recall, helping the model capture most at-risk customers.
### Conclusion
The improved logistic regression model demonstrates strong performance in identifying customers likely to churn, providing actionable insights for SyriaTel’s retention strategies. High recall ensures that most at-risk customers are flagged, while the model’s insights into key features can guide interventions such as improving customer service and offering incentives. This approach allows SyriaTel to proactively manage churn, improve customer satisfaction and minimize revenue loss.