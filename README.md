# Nepal Flood & Weather Analysis

### Machine Learning Live Project Assessment

## Project Overview

This project analyzes weather and river discharge data from 10 monitoring stations in Nepal using Python and Machine Learning. It focuses on identifying rainfall and river discharge patterns, predicting next-day river discharge using regression models, and classifying high-flow observations.

## Project Objectives

- Analyze weather and river discharge patterns.
- Identify seasonal and station-wise variations.
- Perform data preprocessing and feature engineering.
- Predict next-day river discharge.
- Classify high-flow observations.
- Evaluate and compare machine learning models.

## Dataset Information

- **Total Records:** 13,390
- **Original Variables:** 19
- **Monitoring Stations:** 10
- **Data Period:** January 2023 – August 2026

## Tools and Technologies

Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn

## Data Preprocessing and Feature Engineering

- Checked missing values and duplicates.
- Handled missing numerical values using mean imputation.
- Created rainfall and river discharge lag features.
- Calculated rolling rainfall averages.
- Extracted date-based features.
- Applied one-hot encoding.
- Used a chronological 80:20 train-test split.

## Machine Learning Models and Results

### Regression – Next-Day River Discharge Prediction

| Model | MAE | RMSE | R² |
|---|---:|---:|---:|
| Linear Regression | 6.6558 | 18.2174 | 0.9038 |
| Random Forest Regressor | 2.8801 | 22.5870 | 0.8521 |
| Decision Tree Regressor | 3.4389 | 28.1439 | 0.7704 |

**Best Regression Model:** Linear Regression based on R² and RMSE.

### Classification – High-Flow Identification

| Model | Accuracy | Precision | Recall | F1-score |
|---|---:|---:|---:|---:|
| Logistic Regression | 84.40% | 29.15% | 100% | 45.14% |
| Decision Tree | 92.65% | 44.86% | 63.37% | 52.53% |
| Random Forest | 95.75% | 72.31% | 54.65% | 62.25% |

**Best Overall Classification Model:** Random Forest based on accuracy, precision, and F1-score.

## Key Findings

- River discharge was highest during July–September, peaking in August.
- Historical river discharge was the strongest predictor of next-day discharge.
- Feature engineering improved regression performance.
- Random Forest achieved the best overall high-flow classification performance.

## Limitations

- Extreme river discharge values remain challenging to predict.
- Linear Regression occasionally produced negative predictions.
- Mean imputation, including missing target values, may affect evaluation reliability and introduce information leakage.
- High-flow classification identifies same-day observations, not next-day flood events.
- Model performance on new monitoring stations has not been established.

## Conclusion

This project demonstrates the application of machine learning techniques to river discharge prediction and high-flow identification. Linear Regression achieved the best overall regression performance, while Random Forest performed best overall for classification.
