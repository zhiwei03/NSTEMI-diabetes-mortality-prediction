# Mortality Prediction in Diabetes Patient with NSTEMI

## Table of Contents
* [General Info](#general-info)
* [Libraries](#libraries)
* [Workflow](#workflow)
* [Data Preprocessing](#data-preprocessing)
* [Feature Selection](#feature-selection)
* [Models Development](#models-development)
* [Calibration](#calibration)
* [SHAP](#SHAP)
* [Conclusion](#Conclusion)

## General Info
Machine learning model to predict mortality (0 = alive, 1 = death) in diabetes patients with NSTEMI (Non-ST Elevation Myocardial Infarction). 
The model is trained and evaluated using **real** clinical datasets.

## Libraries
- pandas, numpy: data manipulation
- scikit-learn: machine learning models development and evaluation
- matplotlib, seaborn: data visualization

## Workflow
a) Data preprocessing
b) Feature selection
c) Models development
d) Calibration
e) Model Explainability

## Data Preprocessing
- Imputation method
  - Binary & categorical columns ---> SimpleImputer (mode)
  - Continuous columns ---> IterativeImputer

- Normalization method
  - StandardScaler for continuous features

## Feature Selection
- Backward elimination using: XGBClassifier, LogisticRegression, RandomForestClassifier, LinearSVC

## Models Development
- Models used: XGBClassifier, LogisticRegression, RandomForestClassifier, LinearSVC, GradientBoostingClassifier

## Calibration
- Methods: isotonic and sigmoid calibration applied to all models

## Model Explainability
- Using SHAP to interpret model predictions
- Visualizations: beeswarm and waterfall plots for feature importance
  
## Conclusion
- Backward elimination with XGBClassifier achieved highest AUC (0.8081) with 16 selected features
- Sigmoid calibration better than isotonic calibration
- XGBClassifier has the highest performance
  
