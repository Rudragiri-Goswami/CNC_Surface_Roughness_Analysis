# CNC Surface Roughness Prediction

### Multiple Linear Regression on CNC Turning Data

## Motivation

Surface roughness is an important indicator of machining quality and can be affected by different cutting conditions.

This project was carried out to investigate how cutting speed, feed rate, and depth of cut are related to surface roughness and to build an interpretable model for predicting the resulting surface finish.

## Methods

- Exploratory Data Analysis
- Correlation Analysis
- Multiple Linear Regression
- Train-Test Evaluation
- 5-Fold Cross-Validation
- Residual Analysis

## Results

| Metric | 5-Fold CV |
|---|---:|
| R² | 0.579 |
| MAE | 0.160 |
| RMSE | 0.214 |

The regression model provides an interpretable baseline for relating machining parameters to surface roughness.

## Tools

Python · Pandas · NumPy · Matplotlib · Seaborn · Scikit-learn · Jupyter
