# Indonesia Non-Oil Export Forecasting Using ARIMA

## Overview
This project analyzes and forecasts Indonesia's monthly non-oil
export value using the ARIMA time series model.
The analysis was conducted using Minitab as part of a time series
analysis project.

## Objective
The objective of this analysis is to model the monthly pattern of
Indonesia's non-oil exports and forecast the export value for
April 2024.

## Data
- Data source: Statistics Indonesia (BPS)
https://www.bps.go.id/id/statistics-table/2/MTc1MyMy/nilai-ekspor-migasnonmigas.html
- Indicator: Indonesia's non-oil export value
- Frequency: Monthly
- Period: January 2021 – March 2024
- Unit: Million USD (FOB)
<img width="564" height="372" alt="image" src="https://github.com/user-attachments/assets/cc32c036-64cf-4a59-a628-d20db1816281" />

## Methodology
The analysis follows the Box-Jenkins ARIMA framework:
1. Time series visualization
2. Stationarity assessment
3. Box-Cox transformation assessment
4. ACF and PACF analysis
5. Differencing
6. ARIMA model identification
7. Model estimation and evaluation
8. Residual diagnostics
9. Forecasting

## Results
### Candidate Models
Three ARIMA models were evaluated based on Mean Squared Error (MSE).
| Model | MSE with Constant | MSE without Constant |
|---|---:|---:|
| ARIMA(1,1,0) | 4,497,421 | 4,422,546 |
| ARIMA(1,1,2) | 4,288,129 | 4,240,064 |
| **ARIMA(0,1,2)** | **4,187,520** | **4,144,165** |

**Selected Model:** ARIMA(0,1,2)
ARIMA(0,1,2) was selected because it produced the lowest MSE among
the candidate models, both with and without a constant term.

### Forecast

The selected ARIMA(0,1,2) model was used to forecast Indonesia's
non-oil export value.

| Period | Forecast (million USD) | Lower 95% Limit | Upper 95% Limit |
|---:|---:|---:|---:|
| 40 | 20,297.0 | 16,306.2 | 24,287.9 |
| 41 | 20,176.1 | 15,618.7 | 24,733.5 |
| 42 | 20,176.1 | 15,201.6 | 25,150.7 |
| 43 | 20,176.1 | 14,816.8 | 25,535.4 |
| 44 | 20,176.1 | 14,457.9 | 25,894.4 |
| 45 | 20,176.1 | 14,120.2 | 26,232.0 |
| 46 | 20,176.1 | 13,800.4 | 26,551.9 |
| 47 | 20,176.1 | 13,495.8 | 26,856.4 |
| 48 | 20,176.1 | 13,204.6 | 27,147.7 |

<img width="590" height="227" alt="image" src="https://github.com/user-attachments/assets/7e1acc3a-d488-4bce-befa-0c3a0f400968" />
<img width="1535" height="1024" alt="image" src="https://github.com/user-attachments/assets/1721ca30-b1c5-4acc-afb5-aae839c333fe" />

## Key Findings
- **Forecast for April 2024:** 20,297.0 million USD.
- The ARIMA(0,1,2) forecast is consistent with the manual calculation.
- April 2024 represents the **highest forecasted value** among the forecast periods, before the forecast stabilizes at approximately 20,176.1 million USD.
- The April 2024 forecast is lower than the actual March 2024 export value of **21,253.6 million USD**..

## Tools
- Minitab
- Time Series Analysis
- ARIMA
- Forecasting
