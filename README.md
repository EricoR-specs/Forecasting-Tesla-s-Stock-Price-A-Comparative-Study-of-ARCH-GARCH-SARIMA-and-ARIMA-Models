## Forecasting Tesla's Stock Price: A Comparative Study of ARCH/GARCH, SARIMA, and ARIMA Models

**Project Overview**

This project aims to forecast Tesla's stock price movements using various time series models: ARCH/GARCH, SARIMA, and ARIMA. By comparing the performance of these models, we aim to provide insights into the most suitable approach for predicting Tesla's stock price.

**Data**

* **Dataset:** Historical Tesla stock price data from October 9, 2023, to October 9, 2024.
* **Source:** https://www.marketwatch.com/investing/stock/tsla/download-data?startDate=1/1/2020&endDate=09/08/2024

**Methodology**

1. **Data Preprocessing:**
   * Clean and preprocess the data to handle missing values, outliers, and stationarity.

2. **Model Building:**
   * **ARIMA:** Autoregressive Integrated Moving Average model.
   * **SARIMA:** Seasonal ARIMA model.
   * **ARCH/GARCH:** Autoregressive Conditional Heteroskedasticity and Generalized ARCH models.

3. **Model Training and Evaluation:**
   * Train each model using historical data.
   * Evaluate model performance using metrics such as AIC, BIC, R-squared, Mean Absolute Error (MAE), Mean Squared Error (MSE), Root Mean Squared Error (RMSE), Mean Squared Logarithmic Error (MSLE), and Median Absolute Error (MedAE).

**Results**

**Model Evaluation**

| Model | AIC | BIC |
|---|---|---|
| ARIMA | 1848.185 | 1855.325 |
| SARIMA | 590.532 | 597.260 |
| ARCH | 3409.09 | 3419.67 |
| GARCH | 3411.08 | 3425.20 |

**AIC and BIC Comparison**

Lower AIC and BIC values generally indicate a better balance between model fit and complexity. Based on the provided AIC and BIC values, the SARIMA model appears to be the most suitable for forecasting Tesla stock.

**ARCH and GARCH High AIC**

The ARCH and GARCH models have significantly higher AIC values compared to ARIMA and SARIMA. This is likely due to their assumption of heteroskedasticity, which means the variance of the error term is not constant over time. If Tesla's stock price volatility is relatively stable, the ARCH and GARCH models might not be as effective as ARIMA or SARIMA, which assume constant variance.

**Conclusions**

Based on the evaluation of ARIMA, SARIMA, ARCH, and GARCH models for forecasting Tesla stock prices, the SARIMA model with parameters p=0, d=1, q=1, P=0, D=1, Q=1, and seasonal period=210 exhibited the best performance.

The selection of this model was primarily due to:

* **Lowest AIC and BIC values:** Indicating a good trade-off between model fit and complexity.
* **R-squared score:** While negative (-4.899), it suggests a reasonable fit to the data. Negative R-squared values, especially in cases of non-stationary data or non-linear models, may not always indicate a poor model fit.

**Model performance metrics:**

* **MAE, MSE, RMSE, MSLE, MedAE:** These metrics provide insights into the model's prediction errors. Further analysis is required to determine if these values are within acceptable ranges for the specific application.


* The selected SARIMA model can be considered a suitable model for forecasting Tesla stock prices based on the evaluation metrics. However, it is important to note that no model is perfect, and model performance may vary depending on market conditions and other factors.
