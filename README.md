# Correlation-Dynamics-in-Technology-Stocks-A-Case-Study-of-Apple-and-Microsoft
aashusharma08/Correlation-Dynamics-in-Technology-Stocks-A-Case-Study-of-Apple-and-Microsoft

## 📌 Project Overview
This project fetches historical stock data using the `yfinance` library, processes it to compute moving averages, and visualizes stock trends using `plotly.express`. The goal is to analyze stock performance and trends using key technical indicators.

## 📂 Features
- Fetch historical stock data for any ticker symbol.
- Calculate **Simple Moving Averages (SMA)**.
- Plot interactive stock price charts with **candlestick patterns**.
- Compare stock closing prices with different SMA lines.
- Provide insights into stock trends and potential trading signals.

## 🛠️ Technologies Used
- **Python**: Core programming language.
- **yfinance**: Fetching historical stock data.
- **pandas**: Data manipulation and analysis.
- **plotly.express**: Interactive visualization.

## 📥 Installation
Ensure you have Python installed (preferably Python 3.12+). Then, install the required libraries:
```bash
pip install yfinance pandas plotly
```

## 📌 Usage
Run the script to analyze stock data:
```bash
python stock_analysis.py
```

### Example:
```python
import yfinance as yf
import pandas as pd
import plotly.express as px

# Fetch stock data
ticker = 'AAPL'  # Change this to any stock symbol
data = yf.download(ticker, period='6mo')

# Calculate moving averages
data['SMA_20'] = data['Close'].rolling(window=20).mean()
data['SMA_50'] = data['Close'].rolling(window=50).mean()

# Plot stock trends
fig = px.line(data, x=data.index, y=['Close', 'SMA_20', 'SMA_50'],
              labels={'value': 'Price', 'index': 'Date'},
              title=f'{ticker} Stock Price with Moving Averages')
fig.show()
```

## 📊 Visualization
The script generates an interactive line chart displaying:
- **Closing Prices** of the stock.
- **20-day SMA** (short-term trend indicator).
- **50-day SMA** (long-term trend indicator).

## 📌 Contribution
Feel free to improve this project! Fork, make changes, and submit a pull request.

## 📜 License
This project is open-source and available under the **MIT License**.

## 📧 Contact
For queries, reach out via GitHub or email me at **your.email@example.com**.

