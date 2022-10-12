# Breast cancer prediction: Project overview

**Tags: decision tree, AdaBoost, Random Forest, bagging, boosting, feature engineering, ensemble learning, confusion matrix, health**  

This notebook is part of the Breast Cancer Wisconsin (Diagnostic) Data Set Kaggle competition. The steps performed were:

- Dropped a useless column called "Unnamed: 32" in which all the values were Null.
- Label encoded the target variable from object to boolean. 
- Performed feature selection using correlation matrix but no column was discarded.
- Performed feature scaling to avoid model bias.
- Build a decision tree model as our baseline.
- Used ensemble models such as Random Forest and AdaBoost to improve classification outcomes.
- Draw recommendations on how to use model predictions to diagnose breast cancer.

## Code and resources

Platform: Google Colab

Python version: 3.7.6

Packages: itertools, os, matplotlib, pandas, numpy, seaborn and sklearn

## Data set

The data set contains information on cancerous cell nuclei in 3-dimensional space such as size, smoothness, radius, texture, perimeter, area, compactness, and concavity as well as their mean, standard error, and worst values. These characteristics are used to evaluate breast cancer. 

**Data set URL: https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data**

## Model building

- Created a simple decision tree model as our baseline and later compare it to the ensemble models. Then changed the min_samples_leaf parameter to 10 since max_depth was already low (6). Since the false negatives are more relevant and it was needed to decrease this number. 
- Built a Random Forest model using 100 estimators and an AdaBoost one.

## Model performance

- The decision tree had 6 false negatives and when we set min_samples_leaf to 10, the number increased to 7.
- The Random forest model had a good performance with 3 false positives and AdaBoost had an even better result, with only 2.
