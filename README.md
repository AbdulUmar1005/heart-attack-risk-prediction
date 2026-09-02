# Heart Attack Risk Prediction

## Overview
A predictive modeling project analyzing clinical and lifestyle factors to identify individuals at risk of heart attack, with a focus on model fairness across gender.

## Problem
Heart attack risk depends on a mix of clinical markers (heart rate, cholesterol) and lifestyle factors (smoking, diet, stress, sleep). This project builds and evaluates multiple classification models to predict risk, and checks whether model performance holds up fairly across demographic subgroups.

## Approach
- Cleaned and merged clinical and lifestyle datasets, converted target variable to a factor, removed non-predictive columns
- Split data 70/30 into training and test sets
- Built and compared three models: Logistic Regression, Decision Tree (C5.0), and Random Forest
- Ran separate clinical-only vs. lifestyle-only logistic models to compare predictive strength of each variable group
- Evaluated model fairness by testing performance separately across male and female subgroups

## Key Findings
- Resting heart rate emerged as the strongest statistically significant clinical predictor of risk (p = 0.0011)
- Cholesterol and sleep duration showed borderline significance, worth further investigation
- Clinical-only and lifestyle-only models both plateaued around 63.6% accuracy, showing risk prediction benefits more from combining variable types than isolating them
- Gender fairness check: accuracy was comparable across males (62.8%) and females (64.6%), with no major disparity in balanced accuracy (~51% both groups)
- Across all models, sensitivity (catching true high-risk cases) remained low, highlighting a real limitation in the dataset for identifying high-risk individuals specifically, an honest finding that shaped the recommendation for future data collection

## Tools
R, dplyr, caret, C50, randomForest

## Files
- `Predictive_Final.Rmd` — full modeling pipeline and analysis

## Author
Abdul Rahman Umar, MS Business Analytics, University of Hartford
