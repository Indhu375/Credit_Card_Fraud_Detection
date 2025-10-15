💳 Credit Card Fraud Detection

A comprehensive machine learning project for detecting fraudulent credit card transactions using various classification algorithms and advanced techniques to handle highly imbalanced data.

📋 Table of Contents
Project Overview

Dataset

Features

Installation

Usage

Methodology

Results

Project Structure

Contributing

License

🎯 Project Overview
This project implements a machine learning solution for credit card fraud detection, addressing the critical challenge of identifying fraudulent transactions in highly imbalanced datasets. The system employs various data preprocessing techniques, multiple machine learning algorithms, and comprehensive evaluation metrics to achieve optimal fraud detection performance.

Key Highlights:

🎯 High Precision & Recall for fraud detection

⚖️ Handles class imbalance using SMOTE and other techniques

📊 Comprehensive model evaluation with multiple metrics

🔍 Explainable AI with feature importance analysis

🚀 Production-ready pipeline implementation

📊 Dataset
Source
The project uses the popular Credit Card Fraud Detection dataset from Kaggle, containing transactions made by European cardholders in September 2013.

Dataset Characteristics

Attribute	Value
Total Transactions	284,807
Fraudulent Transactions	492 (0.172%)
Legitimate Transactions	284,315 (99.828%)
Features	31 (Time, Amount, V1-V28 PCA components, Class)
Class Imbalance Ratio	1:578

Features Description
V1-V28: Principal components obtained from PCA transformation (anonymized for privacy)

Time: Seconds elapsed between each transaction and the first transaction

Amount: Transaction amount

Class: Target variable (1 = Fraud, 0 = Legitimate)

🛠 Features

🔧 Technical Features

Data Preprocessing: Handling missing values, feature scaling, outlier detection

Exploratory Data Analysis: Statistical analysis, correlation studies, distribution visualization

Class Imbalance Handling: SMOTE, Random UnderSampling, class weights

Multiple Algorithms: Random Forest, Logistic Regression, XGBoost, and more

Model Evaluation: Precision, Recall, F1-score, AUC-ROC, Confusion Matrix

📈 Model Performance

High Recall: Minimizing false negatives (missed fraud cases)

Balanced Precision: Reducing false positives (legitimate transactions flagged as fraud)

ROC-AUC: Comprehensive model performance assessment

🚀 Installation

Prerequisites
Python 3.8 or higher

pip (Python package manager)

Step-by-Step Installation
1. Clone the Repository
   
   git clone https://github.com/yourusername/CreditCardFraudDetection.git
   cd CreditCardFraudDetection\
   
2. Create Virtual Environment
   
   python -m venv fraudenv
   source fraudenv/bin/activate  # On Windows: fraudenv\Scripts\activate
   
3. Install Dependencies
   
   pip install -r requirements.txt

Required Packages

The requirements.txt includes:

pandas>=1.3.0
numpy>=1.21.0
scikit-learn>=1.0.0
matplotlib>=3.5.0
seaborn>=0.11.0
imbalanced-learn>=0.9.0
xgboost>=1.5.0
jupyter>=1.0.0

💻 Usage

Running in Jupyter Notebook

  jupyter notebook

Running in Google Colab

Upload the notebook to Google Colab and ensure the dataset is available in your environment.

# Import and run the main pipeline

from src.pipeline import FraudDetectionPipeline

# Initialize pipeline

pipeline = FraudDetectionPipeline('data/creditcard.csv')

# Run complete analysis

results = pipeline.run_complete_analysis()

# Display results

pipeline.display_results()

🧪 Methodology

1. Data Preprocessing
   
  Feature Scaling: Standardization of Time and Amount features
  
  Handling Imbalance: SMOTE, RandomUnderSampler, and class weight adjustment
  
  Train-Test Split: Stratified splitting to maintain class distribution

2. Exploratory Data Analysis
   
  Statistical summary of features
  
  Correlation matrix analysis
  
  Distribution plots for legitimate vs fraudulent transactions

  Time and Amount feature analysis

3. Model Training
   
Algorithms Implemented:

  Logistic Regression
  
  Random Forest Classifier
  
  XGBoost Classifier
  
  Decision Tree Classifier
  
  Support Vector Machine

4. Model Evaluation
   
Metrics Used:

  Precision, Recall, F1-Score
  
  ROC-AUC Score
  
  Confusion Matrix
  
  Precision-Recall Curve

📈 Results

Performance Comparison


Model	                                                Precision	                    Recall	                                F1-Score	                                          AUC-ROC

Random Forest                	                          0.95	                      0.82	                                  0.88	                                              0.98

XGBoost	                                                0.93	                      0.85	                                  0.89	                                              0.97

Logistic Regression          	                          0.89	                      0.78	                                  0.83	                                              0.96

Key Findings

  Random Forest achieved the best balance between precision and recall
  
  SMOTE significantly improved model performance on minority class
  
  Feature Importance analysis revealed V14, V17, and V12 as most significant predictors

📁 Project Structure

<img width="647" height="598" alt="image" src="https://github.com/user-attachments/assets/ed26bf78-fb63-4c43-90d3-1105f8104cc4" />

🤝 Contributing

We welcome contributions! Please feel free to submit pull requests or open issues for improvements.

Contribution Guidelines

Fork the repository

Create a feature branch (git checkout -b feature/AmazingFeature)

Commit your changes (git commit -m 'Add some AmazingFeature')

Push to the branch (git push origin feature/AmazingFeature)

Open a Pull Request

