The LSTM model tracks the observed series more closely and produces a more moderate long-range forecast with narrower uncertainty bounds.

### Comparative Interpretation
According to the report, the LSTM substantially outperforms ARIMA on this dataset because:

- oil prices exhibit **nonlinear dynamics**,
- the series includes **trend reversals**,
- volatility is not constant,
- ARIMA is limited by its linear structure,
- LSTM can better capture temporal dependencies and nonlinear patterns.


## Key Findings

- The oil price series is **non-stationary** in its original form.
- ARIMA provides a useful statistical benchmark but struggles with structural change.
- Residual diagnostics indicate that ARIMA does not fully capture the dependence structure.
- LSTM gives much better predictive accuracy on the reported test set.
- The 24-month forecasts from the two models differ substantially in shape and uncertainty.
- For this dataset, the report concludes that **LSTM is the more realistic forecasting model**.


## Repository Structure

A suggested project structure is:

```text
project/
│
├── README.md
├── report/
│   └── case study-Report(23076885).docx
├── data/
│   └── oil_price_dataset.csv
├── notebooks/
│   ├── 01_eda_stationarity.ipynb
│   ├── 02_arima_model.ipynb
│   └── 03_lstm_model.ipynb
├── figures/
│   ├── eda_overview.png
│   ├── differencing_acf_pacf.png
│   ├── residual_diagnostics.png
│   ├── lstm_predictions.png
│   ├── model_comparison.png
│   └── combined_forecast.png
└── requirements.txt
```

You can rename folders to match your actual GitHub repository.


## How to Run the Project

### 1. Install dependencies

```bash
pip install -r requirements.txt
```

### 2. Open the notebooks or scripts
Run the workflow in this order:

1. data loading and preprocessing
2. exploratory data analysis
3. stationarity testing and differencing
4. ARIMA model fitting and diagnostics
5. LSTM data preparation and training
6. evaluation and forecasting

### 3. Generate outputs
Expected outputs include:

- exploratory plots,
- stationarity test results,
- ARIMA diagnostics,
- LSTM training and prediction plots,
- forecast comparison charts,
- evaluation metrics table.


## Main Libraries Used

Typical Python libraries for this project include:

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn` or equivalent plotting tools
- `statsmodels`
- `scikit-learn`
- `tensorflow` / `keras`


## Limitations

The report also acknowledges several limitations:

- the analysis is based on a **univariate** series only,
- important exogenous drivers such as macroeconomic variables and geopolitical events are not included,
- ARIMA and LSTM use different data framing strategies, so comparisons should be interpreted carefully,
- uncertainty in long-horizon forecasting remains substantial,
- oil markets are influenced by real-world structural breaks that are difficult to capture fully.


## Future Work

Recommended extensions from the report include:

- **ARIMAX** with exogenous variables,
- **multivariate LSTM**,
- **hybrid ARIMA–LSTM models**,
- **GARCH-family volatility models**,
- **forecast combination methods**,
- **transformer-based forecasting models** such as Temporal Fusion Transformers.


## Citation

If you use this work, cite it as:

```text
Lekkalapudi, Sai Vara Prasad. (2026). Oil Price Time Series Analysis: ARIMA and LSTM Modelling & Forecasting.
Module: Advanced Research Topics in Data Science.
```


## References Used in the Report

Key references include:

- Akaike (1974)
- Baumeister & Kilian (2015)
- Box & Jenkins (1976)
- Fischer & Krauss (2018)
- Gal & Ghahramani (2016)
- Hamilton (1994, 2009)
- Hochreiter & Schmidhuber (1997)
- Lim et al. (2021)
- Zhang (2003)

Please refer to the full report for complete citation details.


## GitHub Link

Repository link from the report:

**Sai-Vara-Prasad-Lekkalapudi/time-series-case-study**
