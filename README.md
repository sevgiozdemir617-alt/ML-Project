# Forecasting Economic Growth in the European Union

Comparative machine-learning study using World Bank World Development Indicators.

## Project question

How accurately can next-year GDP growth across EU countries be predicted using historical economic indicators, and which models, hyperparameters and features contribute most to predictive performance?

## Scope

- Countries: current EU-27 member states
- Raw data period: 1995–2025
- Prediction structure: indicators from year `t` predict GDP growth in year `t+1`
- Final target year: 2025
- Flagship model: XGBoost Regressor
- Reference models: Linear Regression and Random Forest Regressor
- Primary metric: MAE
- Secondary metrics: RMSE and R²

## Predictors

- GDP growth, lagged
- GDP per capita, constant 2015 US$
- Inflation, consumer prices
- Gross fixed capital formation (% of GDP)
- Unemployment rate
- Trade openness, calculated as exports plus imports (% of GDP)
- FDI net inflows (% of GDP)
- General government final consumption expenditure (% of GDP)
- Population growth

## Methodology

1. Retrieve World Bank data through the API or DataBank.
2. Clean and reshape the country-year panel.
3. Create lagged features and the next-year GDP-growth target.
4. Use a chronological train/validation/test split.
5. Compare Linear Regression, Random Forest and XGBoost.
6. Tune XGBoost using Random Search, focused Grid Search and Manual Search.
7. Evaluate using MAE, RMSE and R².
8. Analyse XGBoost feature importance and performance by GDP-per-capita group.

## Validation periods

The current planned split is:

```text
Training target years:   1996–2018
Validation target years: 2019–2021
Testing target years:    2022–2025
```

The final test period must remain untouched until model and hyperparameter decisions are complete.

## Repository structure

```text
economic-growth-forecasting/
├── README.md
├── data/
├── notebooks/
├── src/
├── results/
│   └── figures/
├── requirements.txt
└── .gitignore
```

## Data source

World Bank World Development Indicators:

https://datatopics.worldbank.org/world-development-indicators/

The downloaded data is not committed to this repository until its final cleaned form and licensing/source documentation have been confirmed. See `data/README.md`.

## Presentation

Google Slides link: to be added.

## Status

Project setup in progress. Results and conclusions will be added after the data audit and model evaluation.
