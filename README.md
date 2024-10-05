# Financial Crime Detection And Analysis Of Black Money Using Machine Learning

## Project Overview

Financial crimes such as money laundering, fraud, and illegal money transfers have become increasingly sophisticated, making them harder to detect with traditional methods. This project aims to develop and compare machine learning models to detect potential financial crimes using a dataset with transaction details from various countries and industries. The project covers the full data science process, from data preprocessing to model evaluation and comparison, with a focus on predicting whether a transaction is suspicious based on several factors.

### Dataset

The dataset consists of 10,000 transactions with the following features:
- **Transaction ID**: Unique identifier for each transaction.
- **Country**: The country where the transaction took place.
- **Amount (USD)**: The amount of the transaction in USD.
- **Transaction Type**: Type of the transaction (e.g., deposit, withdrawal, transfer).
- **Date of Transaction**: The date the transaction occurred.
- **Person Involved**: The individual or entity associated with the transaction.
- **Industry**: The industry involved in the transaction.
- **Destination Country**: The destination country of the money involved.
- **Reported by Authority**: Whether the transaction was flagged by an authority.
- **Source of Money**: Where the funds originated.
- **Money Laundering Risk Score**: A score indicating the risk of money laundering associated with the transaction.
- **Shell Companies Involved**: Whether shell companies were involved in the transaction.
- **Financial Institution**: The institution where the transaction took place.
- **Tax Haven Country**: Whether the destination is a known tax haven.

The target variable in this project is detecting whether a transaction is suspicious, i.e., a financial crime.

## Data Preprocessing

The dataset underwent preprocessing to ensure data quality and consistency. Steps included:
- **Handling missing values**: Minimal adjustments were made to address any null or missing values.
- **Encoding categorical features**: Categorical columns such as "Country", "Transaction Type", "Industry", and "Destination Country" were one-hot encoded.
- **Normalization of numerical features**: Columns like "Amount (USD)" and "Money Laundering Risk Score" were normalized.
- **Train-test split**: The data was split into training (80%) and testing sets (20%).

## Modeling Approach

Three machine learning models were applied to the dataset:
1. **Logistic Regression**
2. **Random Forest**
3. **XGBoost**

### Model Performance Metrics
The models were evaluated using the following metrics:
- **Accuracy**: Percentage of correctly predicted instances.
- **Precision**: The proportion of true positives out of all predicted positives.
- **Recall**: The proportion of true positives out of all actual positives.
- **F1 Score**: The harmonic mean of precision and recall.
- **AUC (Area Under the ROC Curve)**: Measures the model’s ability to distinguish between classes.

## Model Comparison and Results

### Logistic Regression Performance
- **Accuracy**: 0.8010
- **Precision**: 0.0000
- **Recall**: 0.0000
- **F1 Score**: 0.0000
- **AUC**: 0.5064

**Analysis**:  
The model achieved an inflated accuracy due to failing to detect any crimes. The AUC score of 0.5064 indicates poor class differentiation.

### Random Forest Performance
- **Accuracy**: 0.8010
- **Precision**: 0.0000
- **Recall**: 0.0000
- **F1 Score**: 0.0000
- **AUC**: 0.5285

**Analysis**:  
Random Forest had similar issues, failing to detect crimes with an AUC of 0.5285, performing slightly better than Logistic Regression.

### XGBoost Performance
- **Accuracy**: 0.7890
- **Precision**: 0.2692
- **Recall**: 0.0352
- **F1 Score**: 0.0622
- **AUC**: 0.5237

**Analysis**:  
XGBoost had the best performance in identifying financial crimes with a higher precision and F1 score compared to the other models, though recall still needs improvement.

## Conclusion: Which Model is Best?

### Best Model: XGBoost

Despite lower accuracy, XGBoost is the best-performing model based on:
- **Precision**: It correctly identified 27% of predicted crimes, while the other models failed.
- **F1 Score**: The highest F1 score, balancing precision and recall.
- **AUC**: Slightly better than Random Forest, XGBoost is more capable of distinguishing between crime and non-crime transactions.


