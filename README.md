**Use of VIIRS Nighttime Light Data (NTL) for Prediction of GDP and Energy Consumption**


Abstract

This study focuses on the use of VIIRS Nighttime Light (NTL) data to predict GDP and energy consumption. It analyzes satellite light intensity values from 2013 to 2023, including median, masked median, minimum, and maximum. We apply machine learning models to identify the correlation between NTL features and economic indicators. Our results highlight the potential of NTL for estimating and forecasting GDP and energy consumption, especially in data-scarce environments.

Introduction

GDP and energy consumption are key indicators of a country’s economic development and quality of life. These metrics are essential for policymakers, researchers, and organizations in planning and executing sustainable development strategies. Traditionally, such indicators have been collected via surveys and governmental methods, which can be costly, delayed, or inaccurate.

With advancements in remote sensing, satellites have been collecting Nighttime Light (NTL) data since 2012. NTL has emerged as a valuable proxy for measuring human activity, economic development, and energy usage. Numerous studies have demonstrated a strong correlation between NTL and economic indicators, proving its utility in estimating trends in regions where traditional data is missing or unreliable.

This paper aims to leverage regression and time series models using VIIRS-derived NTL data to estimate GDP and energy consumption. The core objective is to demonstrate that satellite-derived light intensity correlates positively with economic metrics and can be effectively used for forecasting, especially in low-resource or developing regions.

Data and Preprocessing
Data Sources:
Nighttime Light Data: VIIRS-DNB (Day/Night Band) annual composite data from 2013 to 2023, accessed via Google Earth Engine.

GDP and Energy Consumption Data: Country-level statistics obtained from World Bank and national data repositories for the same time period.

Features Extracted from VIIRS NTL:
Median

Masked Median (excluding low-quality pixels)

Minimum

Maximum

Preprocessing Steps:
Data Integration:

Annual NTL values were extracted for each country.

Merged with corresponding GDP and energy consumption statistics.

Cleaning:

Removed null or incomplete entries.

Normalized GDP and energy values for consistency across countries.

Feature Engineering:

Year-over-year differences.

Log transformations to reduce skewness.

Lag features for time series modeling.

Train-Test Split:

80/20 split using temporal order (training on 2013–2020, testing on 2021–2023).

Results and Discussion
Modeling Approaches Used:
Linear Regression

Random Forest Regressor

XGBoost Regressor

LSTM (for time series prediction)

GDP Prediction:
Best Model: XGBoost Regressor

R² Score: 0.89 on test data

RMSE: Reduced significantly after using log-transformed GDP

Insights: Strongest predictors were masked median and maximum light intensity values. The model showed improved performance in regions with stable annual light patterns.

Energy Consumption Prediction:
Best Model: Random Forest Regressor

R² Score: 0.87 on test data

RMSE: Lower in industrialized nations compared to rural ones

Insights: Median and minimum NTL values correlated strongly with electricity usage. Incorporating lag features improved the temporal prediction accuracy.

Time Series Forecasting:
LSTM achieved R² = 0.84 for GDP and 0.82 for energy consumption using NTL features.

Demonstrated capability of NTL data in capturing temporal economic patterns.

