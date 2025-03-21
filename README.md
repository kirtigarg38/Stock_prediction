# Stock Price Prediction with Stacked LSTM

## Project Overview
This project aims to predict stock prices for Apple Inc. (AAPL) using a **Stacked Long Short-Term Memory (LSTM)** neural network. Stock prediction generally follows two methodologies:  
1. **Fundamental Analysis**: Relies on company financials, news, and macroeconomic factors.  
2. **Technical Analysis**: Uses historical price/volume patterns to forecast trends.  

This implementation focuses on **technical analysis**, leveraging historical stock data to train a deep learning model capable of predicting future prices. The model is designed to forecast both short-term (test set) and long-term (30-day future) price movements.

---

## Methodology
### Technical Analysis Approach
Technical analysis assumes that historical price trends contain patterns that can be extrapolated to predict future behavior. This project uses daily stock prices (Open, High, Low, Close, Volume) to train the model. Key steps include:  
- **Data Normalization**: Scaling prices between 0 and 1 to improve model convergence.  
- **Sequence Generation**: Creating input sequences (e.g., 100 days of data) to predict the next day's closing price.  
- **Stacked LSTM Architecture**: A 3-layer LSTM network to capture complex temporal relationships in the data.  

### Why LSTM?
Long Short-Term Memory (LSTM) networks excel at modeling sequential data with long-term dependencies, making them ideal for time-series forecasting. The "stacked" design (multiple LSTM layers) allows the model to learn hierarchical patterns in stock data.

---

## Features
1. **Data Pipeline**  
   - **Automated Data Fetching**: Retrieves historical AAPL data using the Tiingo API.  
   - **Preprocessing**: Handles missing values, normalizes data, and splits it into training/testing sets.  

2. **Model Architecture**  
   - **3-Layer Stacked LSTM**: Enhances feature learning through deep sequential layers.  
   - **Dynamic Lookback Window**: Uses 100 days of historical data to predict the next day’s price.  

3. **Predictions**  
   - **Test Set Evaluation**: Validates model accuracy against unseen data.  
   - **30-Day Forecast**: Generates future price predictions for trend analysis.  

4. **Visualization**  
   - Interactive plots comparing predicted vs. actual prices.  
   - Future forecast trajectories to guide decision-making.  

