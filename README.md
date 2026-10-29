# TapLend – Loan Risk Prediction & Credit Risk Analysis

## Project Overview

TapLend is a machine learning project focused on analyzing loan application data and predicting potential loan default risk. The objective is to help lenders identify potentially risky applications and make more informed lending decisions using customer and financial information.

## Objectives

- Analyze historical loan application and repayment outcome data.
- Clean, preprocess, and integrate customer and loan records.
- Identify useful features associated with loan risk.
- Train and compare classification models.
- Evaluate model performance and explore different risk classification thresholds.
- Discuss data limitations and potential improvements.

## Dataset Overview

The dataset was provided directly by TapLend as part of the data science assessment. It was used to analyze historical loan application data, study loan repayment outcomes, and develop machine learning models for loan risk prediction.

- **656 loan records**
- **640 unique customers**
- **354 Bad loan records**
- **302 Good loan records**

The target variable was encoded as:
- `1` – Bad loan
- `0` – Good loan

*Note: The dataset's original source and collection details should be documented if available.*

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook

## Methodology

1. **Data Cleaning:** Standardized customer identifiers, handled missing values, and prepared the data for analysis.
2. **Exploratory Data Analysis:** Examined loan outcomes, customer characteristics, and financial features.
3. **Feature Engineering:** Explored additional financial ratios and selected relevant features for model development.
4. **Preprocessing:** Used imputation, one-hot encoding, and numerical scaling where appropriate.
5. **Model Development:** Trained Logistic Regression and Random Forest classifiers.
6. **Evaluation:** Used a customer-wise train-test split to reduce the risk of the same customer's records appearing in both sets.
7. **Threshold Analysis:** Compared different classification thresholds to understand the trade-off between detecting bad loans and incorrectly flagging good loans.

## Model Results

The Random Forest model achieved the following results on the customer-wise test set at the default threshold of 0.50:

| Metric | Result |
|---|---:|
| Accuracy | 64.6% |
| Precision for Bad Loans | 72.0% |
| Recall for Bad Loans | 72.0% |
| F1-score for Bad Loans | 72.0% |
| ROC-AUC | 0.710 |
| PR-AUC | 0.798 |

At an exploratory threshold of 0.40, recall for Bad loans increased to approximately **93.9%**, with precision of approximately **70.0%** on the same test set.

This threshold also caused more Good loans to be incorrectly classified as High Risk. Therefore, the 0.40 threshold should be validated on separate validation data before being considered for practical use.

## Key Learnings

- Understood how to prepare real-world loan data for machine learning.
- Applied classification models to a credit risk problem.
- Learned why recall and precision are important when identifying potentially risky loans.
- Explored how decision thresholds affect classification outcomes.
- Recognized the importance of customer-wise evaluation and responsible use of predictive models.

## Limitations and Future Improvements

- Evaluate the model on a larger and more recent dataset.
- Validate the decision threshold using separate validation data.
- Perform further hyperparameter tuning and cross-validation.
- Investigate class-specific errors and model calibration.
- Assess fairness, explainability, and the impact of incorrect lending decisions.
- Incorporate additional verified financial and repayment-history features when available.

## Project Deliverables

- Jupyter Notebook containing the analysis and model development.
- Model evaluation and risk summary files.
- Project report documenting the methodology, findings, and limitations.

## Disclaimer

This project is for educational and analytical purposes. Model predictions are estimates and should not be used as the sole basis for real-world lending decisions.
