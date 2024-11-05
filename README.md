# Brent Oil Price Analysis and Forecasting

This project provides a comprehensive time series analysis and forecasting of Brent crude oil prices using statistical, econometric, and machine learning models. The project is divided into two main tasks:

1. **Task 1**: Baseline analysis and forecasting of Brent oil prices.
2. **Task 2**: Advanced analysis incorporating additional economic indicators, exploring relationships, and applying multivariate time series models.

## Project Structure

- **Data**: Contains the datasets used for analysis, including Brent oil prices, GDP, and unemployment rate.
- **Notebooks**: Jupyter notebooks detailing the analysis, modeling, and results for each task.
- **Results**: Generated outputs such as forecasts and residuals.
- **Scripts**: Python scripts for preprocessing, model building, and evaluation.
- **README.md**: Overview of the project.

---

## Task Overview

### Task 1: Baseline Analysis and Forecasting of Brent Oil Prices

The objective of Task 1 is to establish a baseline analysis of Brent oil prices using time series techniques.

#### Steps

1. **Data Loading and Preprocessing**
   - Load Brent oil price data and preprocess it for time series analysis.
   - Ensure the time series is stationary by differencing if necessary.

2. **Exploratory Data Analysis (EDA)**
   - Visualize the time series to examine trends and patterns.
   - Perform seasonal decomposition to observe trend, seasonality, and residual components.

3. **Stationarity Test**
   - Apply the Augmented Dickey-Fuller (ADF) test to assess stationarity of the series.

4. **Autocorrelation Analysis**
   - Plot Autocorrelation Function (ACF) and Partial Autocorrelation Function (PACF) to determine the order of the ARIMA model.

5. **ARIMA Model Fitting**
   - Fit an ARIMA model to the series based on ACF and PACF analysis.
   - Use the model to forecast future values of Brent oil prices.
   - Evaluate the model by examining residuals to ensure they resemble white noise.

6. **Results and Visualization**
   - Generate a forecast with confidence intervals and visualize it.
   - Save forecasted and residual data to CSV files (`forecast.csv` and `residual.csv`).

#### Output
- `forecast.csv`: Contains forecasted oil prices.
- `residual.csv`: Contains residuals from the ARIMA model, indicating the model's fit.

### Task 2: Advanced Analysis and Multivariate Modeling

Building on Task 1, Task 2 expands the analysis by including economic indicators and employing advanced models to understand and predict oil price fluctuations better.

#### Steps

1. **Data Collection**
   - Load additional data on economic indicators, including GDP and unemployment rates.
   - Merge this data with the Brent oil price data to create a multivariate dataset.

2. **Multivariate Time Series Modeling**
   - Implement a Vector Autoregression (VAR) model to analyze the relationship between Brent oil prices, GDP, and unemployment rate.
   - Fit the model to understand the interactions among these variables and forecast future prices.

3. **Model Selection and Evaluation**
   - Use the AIC criterion to select the optimal lag order for the VAR model.
   - Forecast oil prices and related indicators for the next 10 months.

4. **Result Analysis**
   - Evaluate the VAR model’s forecasts, interpreting the influence of each variable on oil prices.
   - Compare forecast accuracy with baseline results from Task 1.

5. **Interpretation of Results**
   - Analyze the VAR model output to assess how GDP and unemployment rates affect Brent oil prices.
   - Generate actionable insights based on the multivariate model to understand economic and social impacts on oil markets.

#### Output
- `forecast_multivariate.csv`: Forecast results from the VAR model for Brent oil prices, GDP, and unemployment rate.

---

## Requirements

To replicate the analysis, install the required packages:

```bash
pip install -r requirements.txt
```

## Usage

1. **Data Preparation**:
   - Ensure all data files are placed in the `data/` directory.
   - `BrentOilPrices.csv`: Historical Brent oil prices.
   - `GDP.csv`: GDP data.
   - `UNRATE.csv`: Unemployment rate data.

2. **Running Task 1**:
   - Execute `task1_analysis.ipynb` in the `Notebooks` folder to generate baseline forecasts and residuals.

3. **Running Task 2**:
   - Execute `task2_advanced_analysis.ipynb` to run the multivariate analysis and generate the VAR model forecast.

## Results and Analysis

- Task 1 output: Baseline forecast of Brent oil prices using ARIMA.
- Task 2 output: Forecast of Brent oil prices, GDP, and unemployment rate using the VAR model.
- Visualizations are saved within the notebooks, providing insights into the oil market trends, dependencies, and forecasting accuracy.

## Conclusion

This project showcases a comprehensive approach to analyzing and forecasting Brent oil prices by combining traditional time series analysis with advanced econometric modeling. The results provide valuable insights into how macroeconomic factors influence oil prices, potentially guiding policy-making and investment decisions.
