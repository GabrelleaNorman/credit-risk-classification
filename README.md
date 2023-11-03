# credit-risk-classification
# Credit Risk Analysis Challenge

This repository contains the code and report for the Credit Risk Analysis Challenge. The challenge involves building a logistic regression model to predict credit risk based on the provided dataset.

## Instructions

### Split the Data into Training and Testing Sets

1. Open the starter code notebook and follow these steps:
   - Read the `lending_data.csv` data from the Resources folder into a Pandas DataFrame.
   - Create the labels set (`y`) from the “loan_status” column, and then create the features (`X`) DataFrame from the remaining columns.
   - Note: A value of `0` in the “loan_status” column means that the loan is healthy. A value of `1` means that the loan has a high risk of defaulting.

2. Split the data into training and testing datasets by using `train_test_split`.

### Create a Logistic Regression Model with the Original Data

1. Use your knowledge of logistic regression to perform the following steps:
   - Fit a logistic regression model using the training data (`X_train` and `y_train`).
   - Save the predictions for the testing data labels by using the testing feature data (`X_test`) and the fitted model.

2. Evaluate the model’s performance by doing the following:
   - Generate a confusion matrix.
   - Print the classification report.
   - Answer the following question: How well does the logistic regression model predict both the `0` (healthy loan) and `1` (high-risk loan) labels?

### Write a Credit Risk Analysis Report

1. Create a `README.md` file and use the provided report template in the `Starter_Code.zip` file.

2. Structure your report with the following sections:
   - An overview of the analysis: Explain the purpose of this analysis.
   - The results: Using a bulleted list, describe the accuracy score, the precision score, and recall score of the machine learning model.
   - A summary: Summarize the results from the machine learning model. Include your justification for recommending the model for use by the company. If you don’t recommend the model, justify your reasoning.

## Report Template

Use the provided report template in the `Starter_Code.zip` file to structure and create your report.

---

Good luck with the challenge! If you have any questions or need further assistance, feel free to reach out. Happy coding!
