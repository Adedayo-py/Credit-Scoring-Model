# Credit Scoring Model

## Project Overview

This project uses machine learning to predict the likelihood of a borrower experiencing serious credit delinquency within the next two years.

The goal is to explore how financial and credit-related information can be used to identify borrowers who may be at risk of repayment difficulties.

The project was developed using Python and Scikit-learn, with an interactive demonstration built in Google Colab.

## Dataset

The project uses the **Give Me Some Credit** dataset from Kaggle.

[Dataset source – Kaggle](https://www.kaggle.com/c/GiveMeSomeCredit/data)

The dataset contains 150,000 borrower records and 10 input features.

## Features Used

The model uses the following features:

| Feature | Description |
|---|---|
| Age | Borrower's age |
| Monthly Income | Borrower's monthly income |
| Credit Utilization | Proportion of available credit currently being used |
| Debt Ratio | Monthly debt payments relative to monthly income |
| Open Credit Lines | Number of open credit accounts and loans |
| Dependents | Number of people financially dependent on the borrower |
| 30–59 Days Late | Number of times payments were 30–59 days overdue |
| 60–89 Days Late | Number of times payments were 60–89 days overdue |
| 90+ Days Late | Number of times payments were at least 90 days overdue |
| Real Estate Loans | Number of real estate loans or credit lines |

**Target variable:** `SeriousDlqin2yrs`

- `0`: No serious delinquency within two years.
- `1`: Serious delinquency within two years.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Joblib
- Google Colab
- IPywidgets

## Project Workflow

1. Data loading and exploration.
2. Data cleaning and preprocessing.
3. Exploratory Data Analysis (EDA).
4. Handling missing values using median imputation.
5. Splitting the dataset into training and testing sets.
6. Training and comparing machine learning models.
7. Handling class imbalance.
8. Hyperparameter tuning using RandomizedSearchCV.
9. Model evaluation and comparison.
10. Building an interactive credit scoring demonstration.

## Models Evaluated

- Logistic Regression
- Balanced Logistic Regression
- Random Forest Classifier
- Tuned Random Forest Classifier

## Best Model Performance

The Tuned Random Forest Classifier achieved the following results on the test dataset:

| Metric | Result |
|---|---:|
| Accuracy | 90.83% |
| Precision | 36.24% |
| Recall | 49.08% |
| F1-score | 41.69% |
| ROC-AUC | 0.8578 |
| Average Precision | 0.3812 |

The tuned Random Forest achieved the highest F1-score and ROC-AUC among the evaluated models.

## Interactive Demonstration

The project includes an interactive Google Colab interface where users can:

- Enter applicant financial information.
- Submit the information for assessment.
- Receive a lower-risk or higher-risk prediction.
- View the estimated probability of serious delinquency.

## Limitations

- The dataset is imbalanced, with significantly fewer serious delinquency cases than non-delinquency cases.
- The model's predictions are estimates and are not guarantees of future repayment behaviour.
- The dataset reflects a particular credit-scoring context and may not generalize to other countries or lending environments.
- The model is an educational project and should not be used as the sole basis for real lending decisions.

## Future Improvements

- Experiment with additional machine learning algorithms.
- Improve model calibration and probability estimates.
- Explore more advanced techniques for handling class imbalance.
- Deploy the model as a web application.
- Evaluate performance on more recent and diverse credit datasets.


