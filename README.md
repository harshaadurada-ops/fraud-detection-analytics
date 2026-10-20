# fraud-detection-analytics
Credit card fraud detection using Python, machine learning, and Power BI.
# Fraud Detection Analytics Using Machine Learning

## Project Overview

Fraud Detection Analytics is a data science project that uses machine learning to identify potentially fraudulent credit card transactions. The project uses Python for data preprocessing, exploratory data analysis, model training, and evaluation. Microsoft Power BI is used to visualize transaction statistics and prediction results.

The main goal is to detect fraudulent transactions while reducing false alarms on legitimate transactions.

## Objectives

- Analyze credit card transaction data.
- Clean the dataset and remove duplicate records.
- Perform exploratory data analysis (EDA).
- Build a machine learning classification model.
- Evaluate the model using multiple performance metrics.
- Visualize fraud detection results using charts and a Power BI dashboard.
- Document the project and its findings.

## Tools and Technologies

- **Programming language:** Python
- **Environment:** Google Colab
- **Data analysis:** Pandas, NumPy
- **Data visualization:** Matplotlib, Seaborn
- **Machine learning:** Scikit-learn
- **Classification algorithm:** Logistic Regression
- **Business intelligence:** Microsoft Power BI
- **Version control:** GitHub

## Dataset

This project uses the Credit Card Fraud Detection dataset available on Kaggle.

**Dataset link:**  
https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud

The dataset contains anonymized transaction features, transaction amounts, time information, and a target column named `Class`.

- `Class = 0`: Legitimate transaction
- `Class = 1`: Fraudulent transaction

The dataset is highly imbalanced, with legitimate transactions significantly outnumbering fraudulent transactions.

Please download the dataset from Kaggle and upload it to your Google Colab environment before running the notebook.

## Project Workflow

1. Load the dataset into Python.
2. Inspect the dataset structure and data quality.
3. Identify and remove duplicate records.
4. Perform exploratory data analysis.
5. Separate input features and the target variable.
6. Split the data into training and testing sets using stratified sampling.
7. Standardize the features.
8. Train a Logistic Regression model with balanced class weights.
9. Generate predictions and fraud probability scores.
10. Evaluate the model using classification metrics.
11. Export prediction results to CSV.
12. Create a Power BI dashboard to visualize the results.

## Exploratory Data Analysis

The project explores transaction patterns through visualizations such as:

- Fraudulent versus legitimate transaction counts.
- Distribution of transaction amounts.
- Transaction amounts by fraud class.
- Distribution of fraudulent transactions over time.
- Average transaction amount by class.

These visualizations help examine class imbalance and possible differences between transaction categories.

## Machine Learning Model

Logistic Regression was selected as the initial classification algorithm.

The model uses `class_weight="balanced"` to account for the imbalance between legitimate and fraudulent transactions. A Scikit-learn pipeline combines feature standardization and classification.

The model predicts whether a transaction is legitimate or potentially fraudulent and generates a probability score for the fraud class.

## Model Performance

The following results were obtained on the test dataset:

| Metric | Result |
|---|---:|
| Accuracy | 97.53% |
| Precision | 5.64% |
| Recall | 87.37% |
| F1-score | 10.59% |
| Average Precision | 67.19% |
| Total Test Transactions | 56,746 |
| Actual Fraud Cases in Test Set | 95 |

### Interpretation

- **Accuracy:** 97.53% of test transactions were classified correctly.
- **Precision:** 5.64% of transactions predicted as fraud were actually fraudulent.
- **Recall:** 87.37% of actual fraud cases were detected.
- **F1-score:** 10.59%, reflecting the low precision despite relatively high recall.
- **Average precision:** 67.19%, summarizing precision-recall performance across different score thresholds.

The model detects a large proportion of fraud cases but generates many false positives. Therefore, accuracy alone does not establish that the model is suitable for real-world fraud detection.

## Power BI Dashboard

The planned dashboard includes:

- Total test transactions.
- Actual fraud cases.
- Predicted fraud cases.
- Average fraud score.
- Actual transaction distribution.
- Predicted transaction distribution.
- Average fraud score by actual transaction status.
- Interactive transaction-status slicer.

The dashboard is intended to make the model's results easier to understand through interactive visualizations.

**Dashboard screenshot:** Add a screenshot of the completed Power BI dashboard here after uploading it to the repository.

## Project Files

A suggested repository structure is:

```text
fraud-detection-analytics/
│
├── README.md
├── fraud_detection.ipynb
├── fraud_detection_results.csv
├── Fraud_Detection_Analytics.pbix
├── Fraud_Detection_Analytics_Report.pdf
└── screenshots/
    └── fraud_detection_dashboard.png
```

Only include files that you have actually created. Change the notebook filename to match your uploaded file.

## How to Run the Project

1. Download the dataset from Kaggle.
2. Open Google Colab: https://colab.research.google.com/
3. Upload or open the project notebook.
4. Upload the dataset to the Colab session.
5. Update the dataset path in the notebook if necessary.
6. Run the notebook cells in order.
7. Review the EDA charts and model evaluation results.
8. Export the prediction results CSV.
9. Open Power BI Desktop and import the CSV to build the dashboard.

## Limitations

- The dataset contains anonymized features.
- The class distribution is highly imbalanced.
- The model has low precision and produces many false positives.
- The current model has not been validated for deployment in a live payment system.

## Future Improvements

- Compare Logistic Regression with Random Forest and other classification models.
- Tune the probability threshold to balance recall and precision.
- Evaluate suitable class-imbalance handling techniques.
- Improve the Power BI dashboard with additional model-performance visualizations.
- Test the model on additional transaction datasets.
- Explore deployment after further validation.

## Conclusion

This project demonstrates an end-to-end introductory machine learning workflow for credit card fraud detection, from data preparation and exploratory analysis to model evaluation and dashboard visualization.

The model achieved 97.53% accuracy and 87.37% recall, but its 5.64% precision indicates that further improvements are necessary to reduce false positives.

The project provides practical experience in Python, data analysis, machine learning, model evaluation, Power BI, and GitHub documentation.

## References

- Kaggle dataset: https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud
- Scikit-learn: https://scikit-learn.org/
- Pandas: https://pandas.pydata.org/docs/
- Microsoft Power BI: https://learn.microsoft.com/power-bi/

---

**Author:** Harsha  
**Project:** Fraud Detection Analytics  
**Domain:** Data Science and Machine Learning
