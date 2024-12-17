# **Crude Oil Price Forecasting Using Transformer Models**

## **Project Overview**  
This project predicts **crude oil spot prices** using advanced time-series models, including **PatchTST** and **Temporal Fusion Transformer (TFT)**, alongside economic indicators and sentiment analysis. By integrating external data sources and optimizing hyperparameters, we address the limitations of traditional forecasting methods.

---

## **Problem Statement**  
Oil prices are highly volatile, influenced by macroeconomic shifts, market sentiment, and geopolitical events. Traditional models fail to capture these complexities, leading to inaccurate forecasts.  

---

## **Objectives**  
- Develop models to predict oil prices across short-term (16 steps), medium-term (48 steps), and long-term (96 steps) horizons.  
- Integrate historical prices, economic variables, and sentiment data to enhance predictions.

---

## **Methodology**  

### **1. Data Sources**  
- **Economic Indicators**: S&P 500, Interest Rates, VIX, OVX, USO, DXY.  
- **Historical Crude Oil Data**: WTI spot prices.  
- **Sentiment Data**: Extracted from oil-related headlines using BERT and Mistral models.

### **2. Models**  
- **PatchTST**: Autoregressive transformer model for univariate time-series forecasting.  
- **Temporal Fusion Transformer (TFT)**: Multivariate model incorporating exogenous variables.  
- **Benchmarks**: ARIMA and SARIMAX models.

### **3. Hyperparameter Tuning**  
- Tuning done using **Optuna**.  
- Forecast horizon fixed at **16, 48, 96 steps**.

| **Model**          | **Key Hyperparameters**        |  
|---------------------|--------------------------------|  
| PatchTST           | Forecast History: 16-128, Patch Length: 0-128, Dropout: 0.0-0.5, Heads: 1-4 |  
| TFT                | Hidden Size: 8-16, LSTM Layers: 1-4, Dropout: 0.1-0.5, Attention Heads: 1-4 |  

---

## **Results**  
| **Forecast Horizon** | **Best Performing Model** |  
|-----------------------|--------------------------|  
| **16 Steps**         | PatchTST                |  
| **48 Steps**         | PatchTST                |  
| **96 Steps**         | SARIMAX                 |  

---
