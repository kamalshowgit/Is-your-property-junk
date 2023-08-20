# Flagging Junk Property Listings Project

## Overview

This README.md file provides an overview of the "Flagging Junk Property Listings" project. The primary objective of this project is to develop a predictive model that can identify junk property listings in the real estate industry. By utilizing historical data, the project aims to create a model that helps determine whether a property is suitable for renovation and resale or should be flagged as unsuitable.

## Project Details

### 1. Background

In major cities, the real estate market offers opportunities for renovating old properties and reselling them for a profit. However, not all properties prove to be lucrative investments due to factors such as location, severe dilapidation, or a decline in the neighborhood's appeal. The key challenge is to identify these undesirable properties early in the process, which can save valuable time, resources, and money.

### 2. Data Source

The project utilizes data from previous operations involving properties purchased for renovation but later deemed unsuitable. The dataset includes detailed listing information and preliminary assessment features for each property. Two main data files are used:
- `Property_train.csv` for training the predictive model.
- `Property_test_share.csv` for testing the model's performance.

### 3. Problem Statement

The core task of this project is to build a predictive model using the provided training dataset. This model will assess whether a given property should be flagged as "junk" based on its listing details and preliminary assessment features. The target column for prediction is labeled as "Junk."

## Project Execution

The project execution involves several key steps, as reflected in the provided code. Below is a summary of the code's execution flow:

1. Import necessary libraries and suppress warnings.
2. Load training and testing data from CSV files (`Property_train.csv` and `Property_test_share.csv`).
3. Preprocess the data:
   - Convert certain categorical features to numeric.
   - Fill missing values with the median of corresponding columns from the training data.
   - Create indicator columns for selected categorical features with high frequency.
4. Prepare data for model training:
   - Separate the combined data into training (`x_train`, `y_train`) and testing (`x_test`) sets.
5. Build a predictive model:
   - Utilize logistic regression as the base model.
   - Define a parameter grid for hyperparameter tuning.
   - Perform randomized search cross-validation for optimal hyperparameters.
6. Generate predictions:
   - Use the trained model to predict the probability of properties being "junk" in the testing data.
7. Create a submission file:
   - Prepare a CSV file (`submission.csv`) containing the predicted probabilities.
## Getting Started

To get started with the project, follow these steps:

1. Review the provided data files: `Property_train.csv` and `Property_test_share.csv`.
2. Execute the code provided in your preferred Python environment.
3. Adjust parameters and perform further experimentation if desired.
4. Examine the generated `submission.csv` file for predicted probabilities.

Feel free to reach out if you have any questions or require further support. Good luck with your "Flagging Junk Property Listings" project!