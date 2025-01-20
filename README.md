# India Unemployment Rate Prediction

This project focuses on predicting the **Unemployment Rate** in India using various factors like **Region**, **Estimated Employed**, and **Labour Participation Rate**. The prediction is made using two models:

1. **ARIMA** for time-series forecasting
2. **Random Forest** for region-based predictions

## Overview

The goal of this project is to provide insights into the **unemployment rate** in India by predicting future rates based on historical data. The **ARIMA** model is used to forecast unemployment over time, while **Random Forest** is used to predict unemployment by region.

## Features

- **ARIMA Model**: Used to predict unemployment rates based on time-series data.
- **Random Forest**: Used to predict unemployment by analyzing different regions and their respective factors like **Labour Participation Rate** and **Estimated Employed**.

## Dataset

The dataset used in this project contains the following columns:

- **Region**: The region in India
- **Date**: The date of the record
- **Frequency**: The frequency of the data
- **Estimated Unemployment Rate (%)**: The unemployment rate
- **Estimated Employed**: The number of employed individuals
- **Estimated Labour Participation Rate (%)**: The percentage of the population participating in the labour force
- **Longitude**: Longitude of the region
- **Latitude**: Latitude of the region

### Sample Data:
| Region   | Date       | Frequency | Estimated Unemployment Rate (%) | Estimated Employed | Estimated Labour Participation Rate (%) | Longitude | Latitude |
|----------|------------|-----------|----------------------------------|--------------------|------------------------------------------|-----------|----------|
| Region 1 | 31-01-2020 | Monthly   | 7.8                              | 4500000            | 65.4                                     | 78.9600   | 22.5726  |
| Region 2 | 29-02-2020 | Monthly   | 6.5                              | 5500000            | 68.1                                     | 77.1025   | 28.7041  |

## Installation

1. Clone the repository
    ```bash
    git clone https://github.com/yourusername/unemployment-rate-prediction.git
    cd unemployment-rate-prediction
    ```

2. Install the required libraries
    ```bash
    pip install -r requirements.txt
    ```

## Usage

To run the project, follow these steps:

1. **Run the ARIMA Model** for time series forecasting:
    ```python
    python arima_model.py
    ```

2. **Run the Random Forest Model** for regional predictions:
    ```python
    python random_forest_model.py
    ```

3. **User Input Prediction**: After running the models, you can predict the unemployment rate for a specific region or future dates by providing the necessary input parameters (e.g., Region, Labour Participation Rate, Estimated Employed).

## Example:

To forecast the unemployment rate for the next few months using the ARIMA model:

```python
from arima_model import predict_unemployment_rate

# Example prediction
forecast = predict_unemployment_rate(start_date="2022-01-01", periods=12)
print(forecast)
