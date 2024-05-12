# Customer_churn_prediction
Figuring out which customers may leave the product or service of the company.

Here's a breakdown of what we did:

1. **Data Loading and Exploration:**
    - Loads the churn dataset from a CSV file.
    - Provides summary statistics and unique values for each column.
    - Creates a copy of the dataset for exploration.
    - Visualizes the distribution of `SeniorCitizen` and analyzes churn rates across various features.

2. **Data Preparation:**
    - Drops unnecessary columns (`customerID`, `MonthlyCharges`, `TotalCharges`, `tenure`).
    - Creates a crosstabulation of churn rates for each feature.
    - Calculates the percentage of churn for each feature value. - help you understand how each feature is correlated with the output.
    - Creates a pie chart to visualize the churn breakdown - imbalance dataset.
    - Creates violin plots to compare monthly charges and tenure between churned and non-churned customers.
    - Plots a correlation matrix to analyze relationships between features.

3. **Data Cleaning:**
    - Drops rows with missing values in the `TotalCharges` column.

4. **Feature Engineering:**
    - Identifies categorical, numerical, binary, and multi-value columns.
    - Label encodes binary columns.
    - Creates dummy variables for multi-value categorical columns.
    - Scales numerical columns using the StandardScaler.
    - Drops the original numerical columns and merges the scaled columns back into the dataset.
    - Drops the `customerID` column.
    - Removes any remaining rows with missing values.

5. **Model Training and Evaluation:**
    - Splits the data into train and test sets (70:30 ratio), stratifying on the `Churn` target variable.
    - Performs random undersampling on the training data to address class imbalance.
    - Trains a logistic regression model on the training data.
    - Evaluates the model on the test data and prints the accuracy, confusion matrix, and classification report.
    - Trains a random forest model on the training data.
    - Evaluates the random forest model on the test data and prints the accuracy, confusion matrix, and classification report.

6. **Model Saving and Loading:**
    - Saves the trained random forest model to a file called `model.pkl` using pickle.
    - Loads the saved model from the file and makes predictions on the test data.

Overall, the code demonstrates a comprehensive approach to customer churn analysis using Python libraries such as pandas, matplotlib, seaborn, scikit-learn, and pickle. It illustrates data exploration, preparation, modeling, and evaluation steps while providing insights into churn behavior.