# Loan Eligibility Prediction System

A machine learning project to predict whether a loan application should be approved or rejected based on applicant details.

## What this project does

Banks and NBFCs get thousands of loan applications every day. Manually reviewing each one takes time and is prone to errors. This project builds a classification model that looks at applicant details and predicts if they are eligible for a loan or not.

## Dataset

- 10,000+ loan applications
- 15+ features including income, credit score, employment type, loan amount, loan term, number of dependents, and loan history
- Binary target variable: Loan Approved (1) or Rejected (0)

## Steps followed

**1. Data Loading and Exploration**
- Loaded the dataset using Pandas
- Checked shape, data types, and basic statistics
- Looked at the distribution of approved vs rejected applications

**2. Data Cleaning**
- Handled missing values using median for numerical columns and mode for categorical columns
- Removed duplicate rows
- Fixed incorrect data types

**3. Exploratory Data Analysis**
- Checked correlation between features and loan status
- Plotted distribution of income, credit score, and loan amount
- Checked class imbalance - found more approved than rejected applications

**4. Feature Engineering**
- Encoded categorical variables using Label Encoding
- Applied SMOTE (Synthetic Minority Oversampling Technique) to handle class imbalance
- Scaled numerical features using StandardScaler

**5. Model Building**
- Tried three models: Logistic Regression, Decision Tree, Random Forest
- Split data into 80% training and 20% testing
- Random Forest gave the best accuracy at 85%

**6. Model Evaluation**
- Confusion Matrix
- Classification Report (Precision, Recall, F1-score)
- ROC Curve and AUC Score
- Feature Importance chart

## Results

| Model | Accuracy |
|-------|----------|
| Logistic Regression | 78% |
| Decision Tree | 81% |
| Random Forest | 85% |

Random Forest performed best with 85% accuracy.

Top 3 features affecting loan eligibility:
1. Credit Score
2. Applicant Income
3. Loan History

## Tech Stack

- Python 3
- Pandas, NumPy
- scikit-learn
- Matplotlib, Seaborn
- Jupyter Notebook

## How to run

```bash
# Clone the repo
git clone https://github.com/vasminesyed/Loan-Eligibility-Prediction-System.git

# Install required libraries
pip install pandas numpy scikit-learn matplotlib seaborn imbalanced-learn

# Open the notebook
jupyter notebook loan_eligibility_prediction.ipynb
```

## File structure

```
Loan-Eligibility-Prediction-System/
│
├── loan_eligibility_prediction.ipynb   # Main notebook with full analysis
├── README.md                           # Project documentation
```
