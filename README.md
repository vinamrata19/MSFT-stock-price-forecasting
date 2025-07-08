# MSFT-stock-price-forecasting
## 🧠 Model Summary: LSTM-based Stock Price Prediction

This project implements a **Long Short-Term Memory (LSTM)** neural network to forecast future stock prices based on historical data from **Microsoft (MSFT)**. The model captures temporal dependencies in stock price movements using a sequence-based approach.


## ⚙️ Training Details

- **Loss Function**: Mean Absolute Error (MAE)  
- **Optimizer**: Adam  
- **Evaluation Metric**: Root Mean Squared Error (RMSE)  
- **Epochs**: 20  
- **Batch Size**: 32  
- **Train/Test Split**: 95% training, 5% testing  

---

## 📈 Forecasting Strategy

The model is trained on historical closing prices using a **sliding window** of 60 days. For multi-step future forecasting:

- It uses the **last 60 known or predicted values** to forecast the next day.
- The new prediction is **fed back into the input window** to forecast the next step.
- This recursive process continues for a defined number of future days.


