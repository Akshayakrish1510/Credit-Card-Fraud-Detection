# Credit-Card-Fraud-Detection

Project Overview

This project aims to detect fraudulent credit card transactions using supervised machine learning. The dataset consists of transactions made by European cardholders, provided by researchers and hosted on Kaggle. Out of over 2,84,000 transactions, only 492 are frauds, presenting a highly imbalanced dataset.
The primary goal is to build a model that helps credit card companies identify fraudulent transactions in real time so that customers are not incorrectly charged.

Dataset Summary

Source: [Kaggle - Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
Records: 284,807 transactions
Fraud Cases: 492
Time, Amount, Class (0: non-fraud, 1: fraud)
28 anonymized PCA components (`V1` to `V28`)

The dataset is highly imbalanced, with frauds representing only 0.172% of all transactions.


Objectives

-Understand and explore the dataset
-Handle class imbalance using appropriate techniques (e.g., SMOTE, undersampling)
-Train and evaluate supervised ML models (e.g., Logistic Regression, Random Forest, XGBoost)
-Improve precision and recall for the minority (fraud) class
-Evaluate models using metrics suitable for imbalance (Precision, Recall, F1-Score, AUC-ROC)


Technologies Used

-Python (Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn)
-Jupyter Notebook
-Machine Learning Models: Logistic Regression, Random Forest, XGBoost
-Imbalanced-learn library for resampling techniques


Evaluation Metrics

Given the imbalance, traditional accuracy is misleading. We focus on:

-Precision: How many detected frauds were actually fraud?
-Recall (Sensitivity): How many actual frauds were detected?
-F1-Score: Balance between Precision and Recall
-AUC-ROC: Area under the ROC Curve for classification performance

 
Key Steps in the Project

1. Data Exploration & Preprocessing
   -Check for nulls, distribution, and correlations
   -Normalize `Amount` and drop `Time` if irrelevant
2. Class Imbalance Handling
   -Try SMOTE (oversampling)
   -Try undersampling majority class
3. Model Training
   -Train multiple models and tune hyperparameters
   -Use k-fold cross-validation
4. Model Evaluation
   -Evaluate on test data using suitable metrics
   -Confusion Matrix visualization
5. Conclusion
   -Choose the best-performing model
   -Discuss limitations and future improvements


Future Improvements

-Deploy the model via a web app (Flask/Streamlit)
-Real-time fraud prediction API integration
-Use Deep Learning (e.g., LSTM) for sequential transaction modeling
-Expand dataset with synthetic fraud scenarios

 
Results

The best-performing model achieved:

1. Precision:  [0] 1.00, [1] 0.84       
2. Recall: [0] 1.00, [1] 0.73 
3. F1-Score: [0] 1.00, [1] 0.78  
4. AUC-ROC: 0.9703013330095943
5. PR-AUC Score: 0.7496381817099266

EXECUTIVE SUMMARY

This project aims to detect fraudulent credit card transactions using machine learning. The data shows a heavy class imbalance, with fraud cases making up less than 0.2% of all transactions. After preprocessing, applying SMOTE to balance the data, and applying Optuna for Hyperparameter Tuning, the XGBoost model was trained and selected for its superior yet balanced performance. The final model showed strong Recall and Precision Scores, which are essential for minimizing False Negatives (missing actual fraud cases) whle also reducing false alarms (False Positives). The model was saved and successfully tested on simulated data, providing fraud probability scores for new randomly created transactions. This workflow demonstrates a scalable approach to building an effective fraud detection system.

