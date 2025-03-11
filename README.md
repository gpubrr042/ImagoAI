# ImagoAI
Machine Learning Assignment for ImagoAI

# EDA Notebook 
Exploratory Data Analysis (EDA) Summary:
1. Dataset Overview:
2. Entries: 500 samples
3. Features: 448 numeric hyperspectral features plus one target (vomitoxin_ppb)
4. Identifier Column: hsi_id (non-numeric)
   
# Key Observations:
1. No missing values detected in the dataset.
2. The target variable vomitoxin_ppb has a highly skewed distribution, ranging from 0 to 131,000, with significant right skewness.
3. The target variable vomitoxin_ppb has a skewness of 7.23 and a kurtosis of 55.54, confirming that it is significantly right-skewed and exhibits a long-tail distribution.

This indicates that there are several very high values, making transformations (such as a log-transform) advisable for regression or using threshold-based approaches for classification tasks.

# Regression Task Notebook
Dataset Description :
1. 500 corn samples
2. 448 Spectral brands
3. Vomitoxin_parts per billion

Regression Task : Predict vomitoxin concentraion based on spectral data.
Choice of the model - CNNs are a great fit for hyperspectral data because they can capture local spectral patterns (e.g., peaks/dips across adjacent bands) while being computationally efficient and widely successful in similar tasks.

We will treat 448 bands as 1D sequence, leveraging convolutional filters to extract feeatures.

# Classification Task Notebook
Converting the Regression Problem(predicitng vomitoxin_ppb) into a classification problem.

To distinguish into a binary classification we divide the vomitoxin level as per the median into binary classification problem as the distribution is rightly-skewed. 

It seems to be a practical choice for food safety applications where a threshold determines actionability

# Attention Mechnaism(Bonus)
Transformer with Attention

Transformerss excel at capturing long-range dependencies,which could be advantageous if spectral bands have complex, non-local interactions related to vomitoxin levels.

Unlike CNNs, which focus on local patterns, Transformers use attention to weigh all bands simultaneously, potentially capturing global spectral relationships relevant to vomitoxin.
