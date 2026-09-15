# Supervised-Learning-Model-Implementation
Supervised learning project for fraud transaction detection using a Kaggle dataset. The project includes data preprocessing, EDA, feature engineering, class-imbalance handling, Logistic Regression, 3-fold cross-validation, and evaluation using Precision, Recall, F1-score, ROC-AUC, and PR-AUC.

# Fraud Transaction Detection Using Supervised Learning

## 📌 Project Overview

This project applies supervised machine learning to detect fraudulent financial transactions. The problem is formulated as a binary classification task, where transactions are classified as either legitimate or fraudulent.

## 📊 Dataset

The project uses a publicly available financial transaction dataset from Kaggle containing more than 6 million transaction records.

Target variable:

- 0 → Legitimate transaction
- 1 → Fraudulent transaction

The dataset is highly imbalanced, with approximately 99.87% legitimate and 0.13% fraudulent transactions.

## 🔧 Methodology

The project includes:

- Data cleaning and preprocessing
- Missing-value and duplicate checks
- Exploratory Data Analysis (EDA)
- Removal of high-cardinality identifier columns
- Categorical variable encoding
- Feature engineering using account balance changes
- Stratified train-test split
- Class imbalance handling using `class_weight='balanced'`
- Logistic Regression classification
- 3-fold stratified cross-validation

## 🤖 Model

**Logistic Regression** was selected as the primary classification model.

The model was evaluated using:

- Precision
- Recall
- F1-score
- ROC-AUC
- PR-AUC
- Confusion Matrix

## 📈 Results

Test-set performance:

| Metric | Score |
|---|---:|
| Precision | 0.0259 |
| Recall | 0.9799 |
| F1-Score | 0.0505 |
| ROC-AUC | 0.9946 |
| PR-AUC | 0.5993 |

The model achieved high recall, detecting approximately 98% of fraudulent transactions. However, the low precision indicates a relatively high number of false-positive fraud alerts.

## 🔍 Cross-Validation

Three-fold stratified cross-validation produced:

| Metric | Mean |
|---|---:|
| Precision | 0.0291 |
| Recall | 1.0000 |
| F1-Score | 0.0566 |
| ROC-AUC | 0.9974 |
| PR-AUC | 0.7318 |

## 🚀 Future Improvements

Possible improvements include:

- Classification threshold optimization
- Hyperparameter tuning
- Advanced models such as Random Forest, XGBoost, or LightGBM
- Additional fraud-related feature engineering
- Alternative class-imbalance techniques

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Google Colab
- Jupyter Notebook

## 📁 Project Structure

```text
Fraud-Transaction-Detection/
│
├── README.md
├── fraud_detection.ipynb
├── dataset/
└── report/
