# Nasdaq Volatility Forecast with GARCH

This project uses a GARCH(1,1) model to forecast Nasdaq volatility and simulate future price paths. It also includes a simple rule-based trading strategy using statistical confidence intervals.

## 📂 Files
- `nasdaq_volatility_forecast.ipynb`: full notebook with modeling, simulation, and trade logic
- `volatility_model.py`: Python class wrapping the data, model, and forecast steps
- `charts/`: folder for saved visualizations

## 🔧 Tools Used
- Python, pandas, NumPy
- `yfinance` for data
- `arch` for GARCH modeling
- Matplotlib for plotting

## 🔍 Workflow
1. **Load Nasdaq data** (2018–2024)
2. **Fit GARCH(1,1)** to daily returns
3. **Forecast 30-day volatility**
4. **Simulate 500 future price paths**
5. **Derive confidence bands**
6. **Compare recent prices to cone**
7. **Generate buy/sell signals** based on 5th and 95th percentile breaches


## 💡 Insights
- Most actual prices fell within the 90% forecast cone
- Only a few trades were triggered — typical of conservative statistical strategies
- Symmetric cone reflects the assumption of normally distributed returns

## 🧪 Future Extensions
- Add expected return drift
- Integrate with option pricing or Greeks
- Try EGARCH or GARCH-M
- Evaluate strategy backtest performance

---

**Author**: Brian Njenga Mwaura  
**Portfolio**: [brianmwaura.com](https://www.brianmwaura.com)
