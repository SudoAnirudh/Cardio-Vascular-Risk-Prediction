# Cardiovascular Risk Prediction Analysis

## Project Overview

This notebook analyzes the "data_cardiovascular_risk.csv" dataset to predict the ten-year risk of coronary heart disease (`TenYearCHD`). The analysis involves data loading, exploration, handling missing values, addressing class imbalance, and building a predictive model.

## Data

The dataset contains information on various health factors and lifestyle choices for individuals, with the target variable being `TenYearCHD` (1 indicating the development of coronary heart disease within 10 years, and 0 indicating no development).

## Analysis Steps

1.  **Load the data**: The dataset was loaded into a pandas DataFrame.
2.  **Explore the data**: Initial exploration included displaying the head of the DataFrame, checking data types, and identifying missing values.
3.  **Analyze the data**: Basic analysis involved calculating descriptive statistics for numerical columns and value counts for categorical and target columns.
4.  **Visualize the data**: Visualizations were created to understand the distribution of key variables and the relationships between them.
5.  **Handle missing values**: Missing values in numerical columns were imputed using the mean.
6.  **Handle categorical features**: Categorical variables ('sex' and 'is_smoking') were one-hot encoded.
7.  **Address class imbalance**: The SMOTE technique was applied to oversample the minority class (`TenYearCHD=1`) and balance the dataset.
8.  **Split the data**: The resampled data was split into training and testing sets (80/20 split).
9.  **Build a predictive model**: A Random Forest Classifier model was trained on the training data.
10. **Evaluate the model**: The model's performance was evaluated on the test set using metrics like Accuracy, Precision, Recall, F1 Score, and AUC.
11. **Interpret the model**: Feature importances were analyzed to understand which features contribute most to the prediction.

## Key Findings

*   Several columns had missing values, which were handled through mean imputation.
*   The target variable `TenYearCHD` had a significant class imbalance, which was addressed using SMOTE oversampling.
*   The trained Random Forest model achieved good performance metrics on the test set, with an AUC score of approximately 0.94.
*   The most important features for predicting `TenYearCHD` were identified, including age, systolic blood pressure, and education.

## Next Steps

*   Further explore the relationships between the top influential features and the risk of CHD.
*   Experiment with other predictive models and compare their performance.
*   Perform hyperparameter tuning on the chosen model to potentially improve performance.
*   Investigate potential feature engineering techniques to create more informative features.
*   Consider the ethical implications of using this model for predictions and ensure fairness and transparency.
