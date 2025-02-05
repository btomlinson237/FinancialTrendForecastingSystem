# Financial Trend Forecasting System

## Overview
This project leverages publicly available financial data to develop a machine learning-based forecasting system for stock price movements. The model aims to predict upward or downward stock price trends using a combination of historical stock prices, public company news, analyst ratings, and SEC financial reports. The approach involves binary classification to determine daily price movements while considering complex, interconnected financial factors.

## Methodology
1. **Data Collection & Preprocessing**
   - Scrapes financial data and stores it in the `/data/` directory.
   - Requests stock price data from `yfinance` API.
   - Performs sentiment analysis on public news and financial reports.
   - Computes financial indicators and prepares datasets for training.
   
2. **Feature Engineering**
   - Sentiment scores are extracted from text-based sources.
   - Financial indicators are calculated and combined with textual insights.
   - Data is split into **training, validation, and test sets**.

3. **Model Training & Evaluation**
   - Implements **ARIMA**, **Transformers**, and **LSTM** models.
   - Separate models trained for Apple (AAPL) and Johnson & Johnson (JNJ).
   - Predictions are stored in `/data/final_output_data/` and labeled accordingly.
   - Evaluation includes performance metrics and visualizations.

## Technologies Used
- **Python**
- **Libraries**: `numpy`, `pandas`, `matplotlib`, `seaborn`, `scikit-learn`, `statsmodels`, `tensorflow`, `yfinance`
- **Machine Learning Models**: ARIMA, Transformer Networks, LSTM

## Installation
Clone the repository and install dependencies using Poetry:

```bash
git clone https://github.com/btomlinson237/financialTrendForecastingSystem.git
cd financialTrendForecastingSystem
poetry install
```

## Usage
- **Run Data Preprocessing**: Execute `featurization.ipynb` in `/notebooks/featurePrep/` to generate datasets.
- **Train Models**: Use notebooks in `/notebooks/models/` to train and evaluate different forecasting models.
- **Generate Predictions**: Predictions are stored in `/data/final_output_data/`.
- **Evaluate Performance**: Run validation notebooks in `/notebooks/validation/` to assess model accuracy.



