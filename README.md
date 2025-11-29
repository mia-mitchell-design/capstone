*An LSTM-based financial time-series forecasting system originally developed as my undergraduate capstone project.*

**Designed for a fictional fintech company called Nexfin,** this project demonstrates an end-to-end ML workflow for predicting next-day stock price movements using historical data and engineered features.

## 📌 Overview

This project implements a modular, reproducible pipeline for:

- Automated data collection and cleaning
- Feature engineering for both individual stocks and market-wide indicators
- LSTM-based neural architecture for sequence forecasting
- Evaluating model performance with clear metrics and visualizations

Originally built as my undergraduate capstone project, this version contains reorganized modules, improved preprocessing, and a cleaner development and front-end structure.

### ✨ Features

- Automated data ingestion and cleaning
- Separate feature engineering modules
- Reproducible pipeline architecture
- LSTM sequence model with configurable hyperparameters
- Evaluation utilities with plots & percentage-error metrics
- Clean directory structure for development & experimentation

### 🧠 Model Architecture

The model uses:

- Sliding window sequence inputs
- Stacked LSTM layers with dropout
- Dense prediction layer for next-day price forecasting
- MinMax scaling to normalize train/test splits

Training, evaluation, and model construction are separated for clarity.

### 📂 Project Structure

```css
project/
├── data/
│   ├── raw/
│   └── processed/
├── src/
│   ├── data_loader.py
│   ├── feature_engineering/
│   │   ├── stock_features.py
│   │   └── market_features.py
│   ├── model/
│   │   ├── lstm_model.py
│   │   ├── train.py
│   │   └── evaluate.py
│   └── utils/
├── notebooks/
├── results/
└── README.md
```

### 📈 Results

Across multiple tickers, the model achieved:

- Smoothly decreasing training loss
- ~1-3% average percentage error, depending on ticker
- Stable performance after refactor and feature separation

### 🛠️ Tech Stack

- python
- pandas, numpy
- tensorflow / keras
- matplotlib
- scikit-learn

### 📚 Future Improvements

- Compare LSTM to GRU and Transformer baselines
- Integrate news/sentiment features
- Improve validation stability through regularization tuning
- API or dashboard for predictions
- Containerized deployment workflow

### **📄 License**

MIT License
