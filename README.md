# ImagoAI
Machine Learning Assignment for ImagoAI

# EDA Notebook 
Exploratory Data Analysis (EDA) Summary:
1. Dataset Overview:
2. Entries: 500 samples
3. Features: 449 numeric hyperspectral features plus one target (vomitoxin_ppb)
4. Identifier Column: hsi_id (non-numeric)
   
# Key Observations:
1. No missing values detected in the dataset.
2. The target variable vomitoxin_ppb has a highly skewed distribution, ranging from 0 to 131,000, with significant right skewness.
3. The target variable vomitoxin_ppb has a skewness of 7.23 and a kurtosis of 55.54, confirming that it is significantly right-skewed and exhibits a long-tail distribution.

This indicates that there are several very high values, making transformations (such as a log-transform) advisable for regression or using threshold-based approaches for classification tasks.
