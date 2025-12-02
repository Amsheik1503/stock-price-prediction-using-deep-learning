# 📈 Stock Price Prediction using Deep Learning

This project focuses on forecasting stock prices and generating trading signals using deep learning models. Multiple architectures were trained and compared to identify the most accurate approach for financial prediction.

---

## 🔍 Objective

- **Predict next-day stock Closing Price**  
- **Compare performance** of different deep learning models  
- **Evaluate model accuracy** using real market data  
- **Generate Buy / Sell signals** to support trading decisions

---

## 📊 Dataset

- **Source:** Yahoo Finance API (`yfinance`)  
- **Stock Used:** Apple Inc. — **AAPL**  
- **Features:** Open, High, Low, Close, Adj Close, Volume + Technical Indicators  
- **Forecasting Type:** Univariate regression using sequences

---

## 🧠 Deep Learning Models Compared

| Model Name      | Description |
|-----------------|-------------|
| **LSTM + Attention** | Focuses on important time steps |
| **LSTM + GRU**       | Hybrid model combining memory + gating |
| **CNN + LSTM**       | Feature extraction + temporal learning |
| **BiLSTM + GRU**     | Bidirectional learning + gated sequence modeling |

---

## 📌 Evaluation Metrics

- **MAE** – Mean Absolute Error  
- **MSE** – Mean Squared Error  
- **R² Score** – Coefficient of Determination  
- **Adjusted R²** – Generalization Power

> All results are inverse-transformed to the original price scale.

---

## 🏆 Final Results (Notebook Run)

| Model            | MSE       | MAE     | R²     |
|------------------|----------:|--------:|-------:|
| lstm_attention   | 308.5495  | 13.6833 | 0.5388 |
| lstm_gru         | 145.7457  | 9.5270  | 0.7821 |
| lstm_cnn         | 235.8941  | 12.8773 | 0.6474 |
| **bilstm_gru**   | **81.1707** | **7.0387** | **0.8787** |

**Best Model:** **BiLSTM + GRU**

---

## 📈 Visual Outputs

- **Actual vs Predicted Price** plot  
- **Trading Signal Chart** (Buy / Sell markers)  

These visualizations demonstrate model usability in trading scenarios.

---

## 🚀 Features

- Full reproducible pipeline in **Google Colab**  
- Automatic feature engineering with technical indicators  
- Model training with callbacks (EarlyStopping, Checkpoint, ReduceLROnPlateau)  
- Export of prediction and trading signals to CSV

---

## 🛠 Technologies Used

- **Deep Learning:** TensorFlow, Keras  
- **Data Processing:** Pandas, NumPy  
- **Visualization:** Matplotlib, Seaborn  
- **Data Source:** Yahoo Finance (`yfinance`)  
- **Platform:** Google Colab  
- **Version Control:** GitHub

---

## 🔁 Reproducibility

To reproduce results reliably:

1. Fix random seeds (Python, NumPy, TensorFlow).  
2. Save and reuse fitted scalers (`joblib` / `pickle`).  
3. Use deterministic train/test split.  
4. Save model checkpoints and evaluate on the same test set.  
5. Freeze package versions: `pip freeze > requirements.txt`.

---


---

## 📌 Conclusion

BiLSTM-GRU achieved the best performance in the reported run, showing hybrid recurrent architectures are effective for short-term price forecasting. The pipeline provides a solid base for further experiments and deployment.

---

## 🔮 Future Enhancements

- Add Transformer / Attention-only models  
- Integrate sentiment analysis & alternative data  
- Implement walk-forward validation and backtesting  
- Deploy as a real-time trading system

---

## 👤 Author

**Amsheik . S**  
MSc. Statistics • Data Science Enthusiast


