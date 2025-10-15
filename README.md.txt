💳 Credit Card Fraud Detection
A machine learning project for detecting fraudulent credit card transactions using various classification algorithms and handling class imbalance techniques.

📊 Dataset
The dataset contains credit card transactions made by European cardholders in September 2013.

Total transactions: 284,807
Fraudulent transactions: 492 (0.172%)
Features: 30 (Time, Amount, and 28 PCA-transformed features V1-V28)
Target: Class (0 = Legitimate, 1 = Fraudulent)

🛠️ Technologies Used
Python 3
Pandas, NumPy
Matplotlib, Seaborn
Scikit-learn
Imbalanced-learn
XGBoost

🚀 Installation
bash
# Clone the repository
git clone https://github.com/yourusername/CreditCardFraudDetection.git
cd CreditCardFraudDetection

# Install dependencies
pip install -r requirements.txt
📁 Project Structure
text
CreditCardFraudDetection/
├── data/
│   └── creditcard.csv
├── notebooks/
│   └── CreditCardFraudDetection.ipynb
├── src/
│   ├── data_preprocessing.py
│   ├── modeling.py
│   └── utils.py
├── requirements.txt
└── README.md
🔧 Usage
Run the Jupyter notebook:

bash
jupyter notebook notebooks/CreditCardFraudDetection.ipynb
Or execute the Python scripts:

bash
python src/data_preprocessing.py
python src/modeling.py
📈 Results
Model Performance Comparison
Model	               Precision	Recall	F1-Score	AUC-ROC
Random Forest	         0.95	     0.82	    0.88	   0.98
XGBoost	               0.93	     0.85	    0.89	   0.97
Logistic Regression	   0.89	     0.78	    0.83	   0.96

🎯 Key Features
Data preprocessing and exploratory data analysis
Handling class imbalance using SMOTE
Multiple machine learning models
Comprehensive model evaluation
Feature importance analysis

📊 Visualizations
Correlation matrices
Feature distributions
ROC curves
Confusion matrices
Precision-Recall curves

🤝 Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.
