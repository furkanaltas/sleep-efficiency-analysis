# Sleep Efficiency Analysis

## Problem Statement
Sleep efficiency is a measure of how well a person sleeps relative to the total time spent in bed. Poor sleep efficiency can negatively impact health and daily performance. This project aims to predict sleep efficiency based on personal attributes, lifestyle habits, and sleep patterns.

## Dataset
**Source**: Kaggle – Sleep Quality Dataset  / https://www.kaggle.com/datasets/equilibriumm/sleep-efficiency/data
**Columns**:
  - `Age`, `Gender`, `Sleep duration`, `Awakenings`, `Caffeine consumption`, `Alcohol consumption`, `Smoking status`, `Exercise frequency`, `REM sleep time`, `Deep sleep time`, `Light sleep time`, `Sleep efficiency` (target)

## Business Goal
The goal is to model sleep efficiency using available features. Understanding which factors most influence sleep quality can help individuals improve their sleep habits and assist healthcare professionals in making recommendations.

## Modeling Approach
**Baseline model**: Linear Regression  
**Tuned model**: ElasticNet with GridSearchCV  
**Best parameters**: `alpha=0.01`, `l1_ratio=0.01`  

### Metrics
| Model                   | R²   | MAE  | RMSE |
|-------------------------|------|------|------|
| Linear Regression       | 0.81 | 0.05 | 0.06 |
| ElasticNet (GridSearch) | 0.81 | 0.05 | 0.06 |

## Key Findings
**Positive impact on sleep efficiency**: REM sleep, Deep sleep, Exercise frequency  
**Negative impact**: Light sleep, Smoking status, Awakenings, Alcohol consumption  

## Future Work
* Try advanced models such as Random Forest or XGBoost for potentially better predictions.  
* Explore clustering methods to categorize sleep patterns for personalized recommendations.
