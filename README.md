# 📈 Stock Forecasting using GRU-based Models

![Stock Forecasting](https://img.shields.io/badge/Deep%20Learning-Time%20Series-blue)  
> Predicting stock prices using deep learning models including GRU, CNN-GRU, Transformer, and more.

---

## 🧠 Project Overview

This project explores time series forecasting of stock prices using various deep learning models. It builds upon the base paper _["Stock Price Forecast Based on CNN-BiLSTM-ECA Model" by Yu Chen et al.]_ and compares its results against newer architectures such as:

- CNN-GRU
- GRU-only
- Transformer
- TCN
- Ensemble models

Our GRU-based model outperforms the others with the lowest MAE, demonstrating its effectiveness in capturing temporal dependencies in financial data.

---

## 📂 Files

- `Stock_Forecasting_With_GRU_Models.ipynb` — All model implementations, training, and evaluation
- `Stock_Forecasting_GRU_Report.pdf` — Project report summarizing methodology, experiments, and results

---

## 📊 Dataset

We used the [NIFTY50 stock market data](https://www.kaggle.com/datasets/rohanrao/nifty50-stock-market-data) from Kaggle, covering:

> 📆 **January 2001 to December 2021**  
> 🏢 **50 Companies from NIFTY50 Index**

---

## 🏗️ Model Architectures

### 1. 📚 Base Paper Model: CNN-BiLSTM-ECA

- 1D Convolutional Layer (CNN)
- Bidirectional LSTM Layer
- Efficient Channel Attention Module (ECA)
- Dense Output Layer

### 2. 🧮 Our CNN-GRU Model

- 1D CNN (3x3, ReLU)
- GRU Layer (64 units)
- GRU Layer (32 units)
- ECA Module
- Dense Output Layer

### 3. 🔁 GRU-Only Model

- GRU Layer (64 units)
- GRU Layer (32 units)
- Dropout Layer
- Dense Output Layer

### 4. 🧬 Ensemble Model

- Weighted combination of GRU and CNN-GRU outputs

---

## 🧪 Ablation Study

| Variation               | MAE   |
|------------------------|-------|
| GRU Baseline           | 0.0214 |
| No Hidden Dense Layer  | 0.047  |
| Optimizer: RMSProp     | 0.044  |
| No Second GRU Layer    | 0.043  |
| Replaced GRU with LSTM | 0.059  |
| Optimizer: SGD         | 0.055  |
| Activation: tanh       | 0.052  |
| Dropout Rate: 0.5      | 0.092  |

---

## 📈 Final Results

| Model              | MSE     | MAE    | RMSE   |
|-------------------|---------|--------|--------|
| **GRU**           | 0.0012  | 0.0214 | 0.0267 |
| Ensemble           | 0.0014  | 0.0240 | 0.0317 |
| CNN-GRU-ECA        | 0.0023  | 0.0317 | 0.0418 |
| CNN-BiLSTM-ECA     | 0.0480  | 0.0410 | 0.0521 |

---

## ✅ Conclusion

This project shows that GRU-based models can outperform state-of-the-art deep learning techniques for stock market forecasting. They offer an efficient and effective solution for capturing long-term dependencies in financial time series.
