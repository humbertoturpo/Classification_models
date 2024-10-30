# Classification_models
Capstone Project 17.1: Problem Statement (Section B)


# Marketing Campaign Acceptance Prediction

This project analyzes data from a Portuguese banking institution’s marketing campaigns to predict client acceptance of campaign offers. Following the **CRISP-DM** methodology, we identified key predictors of campaign success and evaluated multiple machine learning models to determine the best approach for predicting client responses.

## CRISP-DM Process

### 1. Business Understanding

The objective of this project was to improve the bank's campaign effectiveness by predicting which clients would accept a campaign offer. Success was defined by the accuracy and reliability of the models in identifying high-potential clients for targeted outreach.

### 2. Data Understanding

The dataset includes detailed information from previous marketing campaigns, with key features such as call duration, outcome of previous campaigns, contact method, and financial indicators like balance. Initial exploration showed that these features are potentially influential in predicting whether a client will accept a campaign offer.

### 3. Data Preparation

We prepared the data by encoding categorical variables and standardizing continuous variables where necessary. This structured approach ensured compatibility with machine learning algorithms and enabled accurate model comparisons.

### 4. Modeling

We evaluated four machine learning models: **Support Vector Machine (SVM)**, **Logistic Regression**, **Decision Tree**, and **k-Nearest Neighbors (kNN)**. Each model was assessed based on accuracy, ROC-AUC, and training time.

### Model Performance Summary

- **SVM**: Achieved the highest accuracy (90.5%) and ROC-AUC (0.906), making it a reliable predictor, though its long training time (277 seconds) makes it more suitable for batch predictions.
- **Logistic Regression**: Nearly matched SVM's performance (89.9% accuracy, 0.904 ROC-AUC) with a much shorter training time (12 seconds), making it ideal for real-time predictions.
- **Decision Tree** and **kNN**: These models demonstrated lower accuracy and ROC-AUC, making them less effective for high-stakes predictions compared to SVM and Logistic Regression.

### Key Factors Influencing Acceptance

1. **Duration of Call**: The most influential variable across models; longer call durations correlate strongly with acceptance.
2. **Past Campaign Success** (`poutcome_success`): Clients with positive responses to previous campaigns are more likely to accept current offers.
3. **Contact Method**: Calls made to mobile phones show higher acceptance rates compared to landlines.
4. **Balance** and **Age**: Higher account balances and specific age groups are associated with greater likelihood of acceptance.

### 5. Evaluation

The evaluation results show that SVM and Logistic Regression are the top models for predicting client acceptance. SVM offers the highest accuracy but is slower to train, making it best suited for batch processing. Logistic Regression, with comparable accuracy and faster training time, is ideal for real-time applications. The feature importance analysis highlighted the critical role of call duration, past campaign success, contact type, and financial indicators in influencing campaign responses.

### 6. Deployment

Recommendations for deploying the models include:

- **Use Logistic Regression for Real-Time Predictions**: With high accuracy and efficient training time, this model is suited for quickly identifying high-potential clients.
- **Employ SVM for Batch Predictions**: SVM can be used for periodic, high-accuracy predictions when training time is less critical.
- **Focus on Key Features in Campaign Strategy**: Prioritize calls to clients with longer engagement times, successful past interactions, mobile contacts, and those with higher balances or within certain age ranges.

## Summary of Findings

- **Top Models**: SVM and Logistic Regression showed the best performance for predicting campaign acceptance.
- **Influential Factors**: Call duration, past campaign outcomes, contact method, and financial indicators like balance and age emerged as key predictors.
- **Deployment Strategy**: Logistic Regression for real-time predictions and SVM for high-accuracy batch processing.

By following these recommendations based on the CRISP-DM process, the bank can enhance its outreach strategy to improve campaign effectiveness.

