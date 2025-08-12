# 📈 Task 2: Stock Price Prediction

## 📌 Project Overview
This project aims to **predict future stock prices** using historical market data.  
The dataset includes key features such as:
- Opening price
- Highest price of the day
- Lowest price of the day
- Closing price
- Trading volume

Two different models were implemented for comparison:
1. **Linear Regression** – A simple and interpretable baseline model.
2. **LSTM (Long Short-Term Memory)** – A deep learning model designed for time-series forecasting.

---

## 🎯 Objectives
- **Load** historical stock data.
- **Explore** and visualize the data to understand trends and relationships.
- **Preprocess** the dataset for both traditional ML and deep learning models.
- **Train and evaluate** two different models.
- **Compare** model performance using appropriate metrics.
- **Visualize predictions** to assess how closely the models follow actual prices.

---

## 📂 Project Structure
The Jupyter Notebook is divided into clear sections:
1. **Install & Import Libraries** – Ensures all dependencies are available.
2. **Load Data** – Download historical stock prices from Yahoo Finance.
3. **Exploratory Data Analysis (EDA)** – Understand the dataset with summary statistics and visualizations.
4. **Part A: Linear Regression Model** –  
   - Feature selection (Open, High, Low, Volume → Close).
   - Train-test split.
   - Model training and evaluation.
   - Visual comparison between predicted and actual prices.
5. **Part B: LSTM Model** –  
   - Scaling and reshaping data for deep learning.
   - Creating sequences for time-series forecasting.
   - Building and training an LSTM model.
   - Evaluating and visualizing predictions.
6. **Conclusion** – Summary of results and potential improvements.

---

## 🛠 Methodology

### 1. Data Source
Historical stock data was fetched using the **Yahoo Finance API**.  
By default, the project uses **Apple Inc. (AAPL)** for the last 5 years, but the ticker symbol can be changed to analyze any other stock.

### 2. Exploratory Data Analysis
- Checked dataset structure, data types, and missing values.
- Plotted historical **closing prices** to visualize trends.

### 3. Linear Regression
- Used **Open, High, Low, Volume** as input features.
- Target variable: **Close**.
- Performed an 80/20 train-test split.
- Evaluated using:
  - **Mean Squared Error (MSE)**
  - **Root Mean Squared Error (RMSE)**
  - **R² Score**
- Visualized predicted vs actual prices.

### 4. LSTM Model
- Focused on **Close** prices for sequence prediction.
- Normalized data to the [0,1] range using MinMaxScaler.
- Created sequences of **60 days of past prices** to predict the next day.
- Built a Sequential LSTM model with:
  - Two LSTM layers
  - One Dense output layer
- Trained for **10 epochs** with a batch size of **32**.
- Evaluated using RMSE.
- Compared predictions against actual prices visually.

---

## 📊 Evaluation Metrics
Both models were assessed using:
- **MSE (Mean Squared Error)** – Measures average squared prediction errors.
- **RMSE (Root Mean Squared Error)** – More interpretable in original units.
- **R² Score** – Indicates how much variance in the target variable is explained by the model (only for Linear Regression).

---

## 📈 Results Summary
- **Linear Regression** is quick to train and provides a good baseline but lacks time-series awareness.
- **LSTM** captures sequential dependencies better and can potentially provide more accurate predictions for complex time-series patterns.

---
