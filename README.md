# Task 4: Predicting Insurance Claim Amounts

## Overview

This project predicts medical insurance charges based on personal attributes such as age, BMI, smoking status, and region. The goal is to build a regression model that estimates how much an individual is likely to be charged and to understand which factors drive those costs.

The dataset used is the Medical Cost Personal Dataset by Miri Choi, available on Kaggle. It contains 1,338 records of insured individuals across the United States.

## Dataset

| Feature | Description |
|---------|-------------|
| age | Age of the insured individual |
| sex | Gender (male or female) |
| bmi | Body Mass Index |
| children | Number of dependents covered under the policy |
| smoker | Whether the individual smokes (yes or no) |
| region | Residential region in the US |
| charges | Medical insurance cost billed (target variable) |

Dataset source: [Kaggle, Medical Cost Personal Dataset by Miri Choi](https://www.kaggle.com/datasets/mirichoi0218/insurance)

## What Was Done

**Data Cleaning**
Checked for missing values and duplicates. Label encoded the categorical columns (sex, smoker, region) to prepare them for the model.

**Exploratory Data Analysis**
Visualized the relationship between charges and the three key variables: BMI, age, and smoking status. Used scatter plots, box plots, bar charts, and a correlation heatmap to understand the data before modeling.

**Model Training**
Trained a Linear Regression model using an 80/20 train-test split with a fixed random state for reproducibility.

**Evaluation**
Measured model performance on the test set using MAE, RMSE, and R².

## Results

| Metric | Value |
|--------|-------|
| MAE (Mean Absolute Error) | $4,186 |
| RMSE (Root Mean Squared Error) | $6,047 |
| R² (Coefficient of Determination) | 0.7515 |

The model explains 75% of the variance in insurance charges. Smoking status had the highest coefficient by a large margin, confirming it as the strongest predictor in this dataset.

## Key Findings

Smoking is the single biggest factor. Smokers pay roughly 3 to 4 times more than non-smokers regardless of other attributes. Age increases charges steadily but the effect is much more pronounced in smokers. BMI on its own does not dramatically raise costs unless the individual also smokes. Obese smokers consistently sit at the top of the charge range. The model under predicts in these extreme cases because linear regression cannot fully capture the interaction between BMI and smoking without an explicit interaction feature.

## Internship

Developers Hub Corporation, Data Science Internship, Task 4

## Author

Aiman Ishaq
