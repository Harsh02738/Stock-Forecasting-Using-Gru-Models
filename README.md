📈 Stock Forecasting using GRU-based Models

Predicting stock prices using deep learning models including GRU, CNN-GRU, Transformer, and more.

🧠 Project Overview
This project explores time series forecasting of stock prices using various deep learning models. It builds upon the base paper ["Stock Price Forecast Based on CNN-BiLSTM-ECA Model" by Yu Chen et al.] and compares its results against newer architectures such as:

CNN-GRU

GRU-only

Transformer

TCN

Ensemble models

Our GRU-based model outperforms the others with the lowest MAE, demonstrating its effectiveness in capturing temporal dependencies in financial data.

📂 Files
Stock_Forecasting_With_GRU_Models.ipynb: Jupyter notebook containing all model implementations, training, and evaluation.

Stock_Forecasting_GRU_Report.pdf: Final report summarizing the methodology, experiments, and results.

📊 Dataset
We used the NIFTY50 stock market data from Kaggle, spanning January 2001 to December 2021, for all 50 companies.

🏗️ Model Architectures
1. 📚 Base Paper (CNN-BiLSTM-ECA)
1D CNN → BiLSTM → ECA Module → Dense Layer

2. 🧮 CNN-GRU
1D CNN (3x3, ReLU) → GRU (64) → GRU (32) → ECA → Dense Layer

3. 🔁 GRU-only
GRU (64) → GRU (32) → Dropout → Dense Layer

4. 🔧 Ensemble
GRU + CNN-GRU predictions combined

🧪 Ablation Studies
We tested:

Model with no second GRU layer

Using LSTM instead of GRU

Removing dense layers

Varying dropout (0.5)

Optimizers: RMSProp, SGD

Activations: tanh vs ReLU

Variation	MAE
GRU Baseline	0.0214
No Dense	0.047
RMSProp	0.044
No 2nd GRU	0.043
LSTM	0.059
SGD	0.055
tanh	0.052
Dropout 0.5	0.092

📈 Final Results
Model	MSE	MAE	RMSE
GRU	0.0012	0.0214	0.0267
Ensemble	0.0014	0.0240	0.0317
CNN-GRU-ECA	0.0023	0.0317	0.0418
CNN-BiLSTM-ECA	0.0480	0.0410	0.0521

✅ Conclusion
Our experiments suggest that GRU-based models significantly outperform other state-of-the-art deep learning approaches for stock price forecasting. This aligns with the need for lightweight, efficient models that capture temporal dynamics well.
