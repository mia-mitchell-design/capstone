*A neural time-series forecasting tool built with LSTMs, designed to predict next-day stock price movements using historical features and market indicators.*

## 📌 Overview

This project is an end-to-end machine learning pipeline for financial time-series price prediction.  It includes:

- Automated data collection and cleaning
- Feature engineering for both individual stocks and market-wide indicators
- LSTM-based neural architecture for sequence forecasting
- Full training/validation workflow
- Visualization of performance metrics
- Modularized codebase refactored for reproducibility and clarity

Originally built as my undergraduate capstone project, this version contains reorganized modules, improved preprocessing, and a cleaner development and front-end structure.

### ✨ Features

- Automated data ingestion and cleaning
- Modular pipeline: no global variables, explicit state management
- Customizable feature sets
- LSTM sequence model with tunable hyperparameters
- Training curves + validation performance visualizations
- Evaluation metrics with percentage-error summary
- Clear directory structure for dataset, model, and results

### 🧠 Model Architecture

A stacked LSTM with:

- Sliding window sequence inputs
- Dropout regularization
- Dense prediction head
- Train/test split handled inside preprocessing
- Scaler retained and applied consistently

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

The final model achieved:

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
- Improve validation stability through regularization tuning
- Expand features with sentiment or macroeconomic indicators

### **📄 License**

MIT License
