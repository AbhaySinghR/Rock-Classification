# Rock Classification Using Machine Learning

## Overview
This project focuses on applying and evaluating different classification methods to predict the **rock category** (Igneous, Metamorphic, Sedimentary) based on 11 distinct rock features. The dataset is derived from the **Rock Dataset** and consists of structured data split into training, validation, and test sets. The project also involves comparing the model's performance to human accuracy in classifying rocks.

## Source Description
https://osf.io/cvwu9/wiki/Data%20File%20Descriptions/



## Dataset Description
The dataset includes the following key components:

- **aggregateRockData.xlsx**:
  - Contains the rock category (label), which is in the 2nd column.
  - Rock categories: 
    - 1 = Igneous
    - 2 = Metamorphic
    - 3 = Sedimentary.

- **features_presence540.txt**:
  - Attributes (features): Columns 4 to 14.
  - Token number: Column 3 (used to separate training, validation, and testing data).

- **trialData.csv**:
  - Contains human classification data for comparison with model predictions.

### Data Constraints:
- Only the first 480 rows from the dataset are used.
- Token numbers are used for splitting the dataset:
  - Training: Token numbers 1-10.
  - Validation: Token numbers 11-13.
  - Testing: Token numbers 14-16.

### Features and Labels
- **Features (columns 4 to 14)**: Rock-specific attributes.
- **Labels (column 2)**: Rock category.

## Key Objectives
1. **Exploratory Data Analysis (EDA)**:
   - Display statistical values and histograms for each attribute.
   - Identify and address attributes requiring special treatment.

2. **Data Relationships**:
   - Compute Pearson Correlation Coefficient (PCC) and generate scatter plots.
   - Analyze relationships between attributes and labels.

3. **Data Splitting**:
   - Split data into training, validation, and testing subsets based on token numbers.

4. **Classifier Training and Evaluation**:
   - Train and tune hyperparameters for the following classifiers:
     - Multinomial Logistic Regression.
     - Support Vector Machine (SVM) with various kernels.
     - Random Forest Classifier with feature importance analysis.
   - Evaluate classifiers using accuracy, precision, recall, and F1 score.
   - Combine classifiers into an ensemble and evaluate performance.

5. **Human vs. Model Accuracy**:
   - Compare human classification accuracy to the best-performing model.
   - Analyze the correlation between human accuracy and model probabilities.

6. **Visualization and Statistical Analysis**:
   - Plot average human accuracy vs. model probabilities for 480 rocks.
   - Compute the correlation coefficient and p-value for accuracy comparison.
  

## Key Results

Exploratory Data Analysis (EDA): Visualized attribute distributions and identified correlations between attributes and labels.
Classifier Performance:
Compared Multinomial Logistic Regression, SVM, and Random Forest classifiers.
Fine-tuned hyperparameters (e.g., penalty term, kernel type, number of trees) to improve performance.
Combined classifiers into an ensemble for superior accuracy.
Human vs. Model Accuracy:
Analyzed model performance compared to human classification accuracy.
Investigated correlations between human accuracy and model probabilities.

##Insights and Future Work

Feature Engineering: Adding derived features or domain-specific transformations may enhance accuracy.
Advanced Models: Exploring neural networks or gradient-boosting techniques like XGBoost.
Human-in-the-Loop: Investigate hybrid models where human expertise augments machine learning.
