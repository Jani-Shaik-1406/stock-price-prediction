
# 📈 Apple Stock Price Prediction using Machine Learning

This project presents a comparative analysis of machine learning techniques to predict the closing stock price of Apple Inc. It utilizes historical stock data and focuses on building a reliable regression model to forecast stock movements.

---

## 🧠 Problem Statement

Apple Inc.’s stock price is influenced by multiple market factors, including trends, financial performance, macroeconomic indicators, and global events. The ability to predict future closing prices using past trends can help investors and analysts make better decisions.

---

## 📊 Dataset Description

- **File:** `AAPL.csv`
- **Date Range:** December 12, 1980 to 2021
- **Features:**
  - `Open`, `High`, `Low`, `Close`, `Adj Close`, `Volume`
- Additional engineered features like `DayOfWeek` and `Month` were considered but avoided to maintain model simplicity.
- The dataset contains **no missing values** and is comprised mainly of float data types.

---

## 🔍 Exploratory Data Analysis

- **Time-Series Trend:** Visualizations showed a strong upward trend over time (inflation-driven).
- **Correlation Analysis:** High correlation among price-related columns (Close, Open, High, Low), but `Volume` showed weak correlation and was dropped.
- **Scatter Plots:** Confirmed linear relationships and revealed missing price ranges due to rapid changes.

---

## 🤖 Model: Linear Regression with Look-Back Feature

- **Goal:** Predict `Close` price using historical data and a `look_back` value of 20 time steps.
- **Preprocessing:** Used MinMaxScaler to normalize features between 0 and 1.
- **Cross-validation:** 5-Fold Cross Validation used to train and evaluate the model.
- **Model Evaluation:**
  - Mean MSE: `0.5366`
  - Std MSE: `0.0755`
  - Mean R²: `0.9995`
  - Std R²: `0.0000634`
  - Test MSE: `2.1335`
  - Test R²: `0.99897`

📉 The model performs extremely well, closely tracking the actual closing prices in the test set.

---

## 📈 Visualization

The predicted closing prices closely follow the actual stock prices, indicating the effectiveness of the model in identifying underlying trends and patterns.

---

## ✅ Conclusion

This project demonstrated the power of linear regression with historical context (look-back) in stock price forecasting. The model achieved high accuracy and consistency across validation and test data. The methodology provides a strong baseline for financial time-series modeling, though more complex models could be explored in future iterations.

---

## 📂 Project Structure

```
├── AAPL.csv
├── model_training.ipynb
├── Report.pdf
└── README.md
```

---

## 📌 Future Enhancements

- Compare with more complex models (LSTM, Random Forest)
- Introduce external financial indicators or sentiment data
- Implement real-time prediction pipelines

---

## ⚠️ Disclaimer

This project is for academic and learning purposes only. Stock market investments carry risks, and this model is not intended for financial advice.

