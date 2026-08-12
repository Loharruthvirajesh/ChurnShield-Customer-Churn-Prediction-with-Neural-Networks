# ChurnShield — Customer Churn Prediction with Neural Networks

## Overview

ChurnShield is a machine learning project focused on predicting whether a customer is likely to leave a company. The project uses customer-level historical data and an Artificial Neural Network (ANN) to identify churn patterns and classify customers into churn and non-churn categories.

The goal is not just to build a prediction model, but to understand how customer characteristics can be transformed into useful information for customer-retention decisions.

## Business Problem

Customer churn can directly affect revenue and long-term business growth. If a company can identify customers who are more likely to leave, it can take preventive action through targeted offers, improved customer service or retention campaigns.

This project addresses the question:

> **Can we predict whether a customer is likely to churn based on their available customer information?**

## Project Objective

* Analyze customer data and understand churn patterns
* Prepare customer data for machine learning
* Transform categorical variables into numerical features
* Build an Artificial Neural Network for binary classification
* Predict the probability of customer churn
* Evaluate the model using multiple classification metrics
* Analyze model performance using visualizations
* Understand the challenges of predicting churn when the target classes are imbalanced

## Dataset

The project uses the **Churn Modelling** dataset containing **10,000 customer records and 16 variables**.

The target variable is:

* `Exited = 0` → Customer stayed
* `Exited = 1` → Customer churned

The dataset contains customer information such as:

* Credit Score
* Geography
* Gender
* Age
* Tenure
* Balance
* Number of Products
* Credit Card Status
* Active Member Status
* Estimated Salary

Identifiers such as `RowNumber`, `CustomerId` and `Surname` were excluded from model training.

## Approach

### 1. Data Preparation

The dataset was loaded using Pandas and inspected for its structure, variables and target distribution.

Categorical variables such as `Geography` and `Gender` were converted into numerical features using one-hot encoding.

### 2. Train-Test Split

The dataset was divided into training and testing sets using an 80:20 split.

Stratified sampling was used to maintain the proportion of churned and non-churned customers in both datasets.

### 3. Neural Network

An Artificial Neural Network was developed using TensorFlow/Keras.

The architecture consists of:

* Input layer
* Dense layer with 16 neurons and ReLU activation
* Dense layer with 8 neurons and ReLU activation
* Output layer with 1 neuron and Sigmoid activation

The model was trained using:

* **Optimizer:** Adam
* **Loss Function:** Binary Cross-Entropy
* **Epochs:** 50
* **Batch Size:** 32

### 4. Model Evaluation

The model generated churn probabilities which were converted into binary predictions using a 0.5 probability threshold.

Performance was evaluated using:

* Accuracy
* Precision
* Recall
* F1-Score
* ROC-AUC
* Confusion Matrix

Training and validation accuracy/loss curves were also examined to identify potential overfitting.

## Key Outcome

The model achieved approximately **80% test accuracy**, which is close to the overall proportion of customers who did not churn in the dataset.

This project therefore highlights an important machine-learning lesson: **accuracy alone is not enough for an imbalanced churn problem.**

Precision, recall, F1-score and ROC-AUC need to be considered together, particularly because correctly identifying customers who are likely to churn is more valuable from a retention perspective than simply achieving high overall accuracy.

## Business Application

A churn prediction system like this can help a business:

* Identify customers with a higher probability of leaving
* Prioritize customer-retention campaigns
* Understand customer characteristics associated with churn
* Support targeted offers and personalized communication
* Help customer-success teams focus their efforts on higher-risk customers

The model can serve as a starting point for a larger customer-retention analytics solution.

## Tools & Technologies

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* TensorFlow
* Keras
* Jupyter Notebook

## Project Structure

```text
ChurnShield/
│
├── ANN_Customer_Churn3.ipynb
├── Churn_Modelling3.csv
└── README.md
```

## Machine Learning Workflow

```text
Raw Customer Data
        ↓
Data Inspection
        ↓
Feature Selection
        ↓
Categorical Encoding
        ↓
Train-Test Split
        ↓
Artificial Neural Network
        ↓
Model Training
        ↓
Churn Probability
        ↓
Classification
        ↓
Model Evaluation
        ↓
Business Insights
```

## Conclusion

ChurnShield demonstrates an end-to-end approach to customer churn prediction using an Artificial Neural Network. The project combines data preparation, feature engineering, neural-network modelling and classification evaluation to turn customer data into a potential retention-support tool.

The project also demonstrates why a business problem should be evaluated from more than one metric rather than relying only on model accuracy.

## Author

**Ruthvi Rajesh Lohar**

Data Analyst | SQL | Python | Power BI | Machine Learning | Business Analytics
