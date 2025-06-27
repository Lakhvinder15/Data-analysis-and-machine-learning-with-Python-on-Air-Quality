# Predictive Analysis and Machine Learning: Air Quality Data Analysis

## Project Overview
This project focuses on applying predictive analytics and machine learning techniques to analyze and predict carbon monoxide (CO) levels using the Air Quality UCI dataset. The goal is to explore the relationship between environmental variables (e.g., temperature, humidity) and CO levels, and to evaluate the performance of Linear Regression and Random Forest models in predicting CO concentrations.

## Dataset
The **Air Quality UCI dataset** contains measurements of air pollutants, including CO levels (CO(GT)), alongside environmental variables such as temperature (T), relative humidity (RH), and absolute humidity (AH). Key features of the dataset:
- **Columns**: CO(GT), PT08.S1(CO), NMHC(GT), NOx(GT), temperature (T), RH, AH, and others.
- **Data Type**: Numeric (float64) for most features, with datetime and object types for timestamps.
- **Data Size**: The Original dataset had missing values, which were cleaned and processed.

## Data Preparation
1. **Handling Missing Data**: Invalid values (e.g., -200) were replaced with `NaN`, and rows with missing data were dropped.
2. **Exploratory Data Analysis (EDA)**:
   A correlation heatmap revealed strong relationships between specific features.
   - Histograms and scatter plots showed the distribution of CO(GT) and its weak linear relationship with temperature.
3. **Feature Selection**: Focused on environmental variables (T, RH, AH) as predictors.

## Machine Learning Models
Two models were trained and evaluated:
1. **Linear Regression**:
   - Simple linear approach to predict CO(GT).
   - Performance: MAE ≈ 0.968, R² ≈ 0.18.
2. **Random Forest Regressor**:
   - Ensemble method to capture non-linear relationships.
   - Performance: MAE ≈ 0.948, R² ≈ 0.18.

## Results
- Both models showed **low predictive power** (R² ≈ 0.18), indicating limited ability to explain variance in CO(GT) levels.
- **Random Forest** marginally outperformed Linear Regression in MAE but struggled with higher CO(GT) values.
- Scatter plots of predicted vs. actual values revealed significant deviations, suggesting the models could not fully capture underlying patterns.

## Conclusion
- The project highlights the challenges of predicting air quality using limited environmental variables.
- **Recommendations for improvement**:
  - Incorporate additional features (e.g., temporal trends, traffic data).
  - Experiment with advanced techniques (e.g., hyperparameter tuning, deep learning).
  - Explore feature engineering to better represent non-linear relationships.

## Future Work
- Expand the dataset with more contextual variables.
- Test other algorithms (e.g., Gradient Boosting, Neural Networks).
- Optimize model parameters for better performance.
