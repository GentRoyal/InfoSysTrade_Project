# Sales Forecast Project

## Overview
This project focuses on forecasting daily sales using time series models. Sales data has been aggregated at different time intervals (daily, weekly, and monthly) to provide flexibility in forecasting needs. The analysis includes data exploration, model selection, performance evaluation, and visualization.

## Data Exploration
- Log returns were calculated and visualized.
- Log returns appeared right-skewed, though no statistical tests were performed to confirm this.
- Selected models that handle skewed returns effectively: Prophet, SARIMAX, and XGBoost.

## Model Performance
| Model   | MAE (Mean Absolute Error) | RMSE (Root Mean Squared Error) |
|---------|--------------------------|------------------------------|
| SARIMAX | 467.93                   | 628.99                       |
| Prophet | 461.83                   | 619.99                       |
| XGBoost | 424.46                   | 472043.05                    |

## Model Selection & Insights
- **Prophet** was chosen due to its lowest RMSE, making it more sensitive to outliers.
- **SARIMAX** performed similarly to Prophet and remains a viable alternative.
- **XGBoost** had the lowest MAE but an excessively high RMSE, indicating poor generalization and high variance.

## Forecasting & Visualization
- Developed a forecasting function to output predicted sales with confidence intervals.
- Created a forecast visualization chart to illustrate predicted trends.

## Next Steps & Improvements
- Conduct further investigation into log return skewness to refine model assumptions.
- Perform hyperparameter tuning for SARIMAX and XGBoost to improve model performance.
- Explore alternative models such as LSTMs for better long-term forecasting.
- Integrate the model with an API for real-time analysis and forecasting.
- Deploy the model online for wider accessibility.

## Task 5: Data Storytelling & Dashboard Presentation
- Implemented a **Streamlit** dashboard to present sales forecast insights.
- The initial plan was to host the model online alongside the dashboard, but time constraints limited this.
- The dashboard is accessible here: [Sales Forecast Dashboard](https://alphaglobal-sales-forecast.streamlit.app/)

## Additional Features
- An additional Jupyter notebook (`Running Automation.ipynb`) automates the forecasting process.
- The notebook executes Python scripts stored in the `scripts` folder, streamlining workflow execution.
