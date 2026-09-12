# 📊 CRT Trading Analyzer
## Candle Range Theory Pattern Recognition Tool

A professional-grade trading analysis platform for identifying and analyzing Candle Range Theory (CRT) patterns in real-time market data.

## 🎯 Features

### Core Functionality
✅ **Real-time Candlestick Charts** - Interactive charting with Chart.js  
✅ **CRT Pattern Recognition** - Automatically identifies HR, LR, Inside Bar, Outside Bar patterns  
✅ **Trading Signals** - Generated based on CRT analysis with entry/exit points  
✅ **Risk Management Tools** - Automatic calculation of stop loss and profit targets  
✅ **Multi-Timeframe Support** - Analyze any timeframe from 1-minute to daily  

### Educational Resources
📚 **CRT Concepts Guide** - Learn HR, LR, Inside/Outside bars  
📚 **Trading Setups** - Common CRT trading strategies  
📚 **Trading Tips** - Best practices and risk management  

### Analysis Tools
📈 **Candle Analysis** - Open, High, Low, Close, Range data  
📊 **Pattern Detection** - Type, strength, and signal identification  
📉 **Range Analysis** - Average range, range percentage, status  
🎯 **Setup Calculation** - Entry, stop loss, and profit target levels  

## 🚀 Quick Start

### Option 1: Online Demo
Visit: `https://MONI2303.github.io/trading-website/`

### Option 2: Run Locally

1. **Clone the repository:**
```bash
git clone https://github.com/MONI2303/trading-website.git
cd trading-website
```

2. **Start a local server:**

**Using Python 3:**
```bash
python -m http.server 8000
```

**Using Python 2:**
```bash
python -m SimpleHTTPServer 8000
```

**Using Node.js:**
```bash
npx http-server
```

**Using Live Server (VSCode):**
- Install Live Server extension
- Right-click `index.html` → "Open with Live Server"

3. **Open your browser:**
```
http://localhost:8000
```

## 📖 How to Use

### 1. **Analyzer Tab**
- Enter a trading symbol (AAPL, BTC, EURUSD, etc.)
- Select your preferred timeframe (1m, 5m, 15m, 1h, 4h, 1d)
- Click "Load Data" to fetch and analyze
- View candlestick chart and CRT analysis panels

### 2. **Learn CRT Tab**
- Understand key CRT concepts (HR, LR, Inside Bar, Outside Bar)
- Learn common trading setups
- Read best practices for CRT trading

### 3. **Signals Tab**
- View generated trading signals
- See entry, stop loss, and profit targets
- Understand signal strength and type

## 🔍 CRT Pattern Types

| Pattern | Description | Trading Signal |
|---------|-------------|-----------------|
| **🔥 High Range (HR)** | Large candle range compared to recent candles | Trending move, momentum trade |
| **❄️ Low Range (LR)** | Small candle range, consolidation pattern | Watch for breakout |
| **📊 Inside Bar** | Completely inside previous candle's range | Tight stop loss opportunity |
| **⬆️ Outside Bar** | Extends beyond previous candle in both directions | Volatility expansion signal |
| **💫 HR + HR** | Two consecutive high range candles | Strong trending market |
| **🔒 LR + LR** | Two consecutive low range candles | Consolidation/breakout setup |

## 📊 Analysis Panels

### Current Candle
Displays OHLC (Open, High, Low, Close) data and calculated range for the most recent candle.

### CRT Pattern
Identifies the current pattern type (HR, LR, Inside Bar, etc.), its strength, and trading signal.

### Range Analysis
Shows average range over last 5 candles, current range as percentage, and high/low range status.

### Trading Setup
Automatically calculates:
- **Entry Point** - Breakout level for trade entry
- **Stop Loss** - Risk management level
- **Profit Target** - Risk/reward based exit point

## 🛠️ Technologies

- **Frontend:** HTML5, CSS3, JavaScript (ES6+)
- **Charting:** Chart.js with Candlestick plugin
- **APIs:** (Ready for real market data integration)
  - Alpha Vantage
  - IEX Cloud
  - Alpaca
  - Finnhub

## 📝 File Structure

```
trading-website/
├── index.html          # Main HTML structure
├── style.css           # Styling and responsive design
├── script.js           # Pattern recognition & analysis logic
├── package.json        # Project metadata
└── README.md           # Documentation (this file)
```

## 🔧 API Integration Guide

The analyzer is ready to integrate with real market data APIs:

### Example: Alpha Vantage
```javascript
async function fetchRealData(symbol, timeframe) {
    const apiKey = 'YOUR_API_KEY';
    const url = `https://www.alphavantage.co/query?function=TIME_SERIES_INTRADAY&symbol=${symbol}&interval=${timeframe}&apikey=${apiKey}`;
    
    const response = await fetch(url);
    const data = await response.json();
    // Process and update chart
}
```

### Example: Alpaca Markets
```javascript
async function fetchAlpacaData(symbol, timeframe) {
    const headers = {
        'Authorization': `Bearer ${APCA_API_KEY}`
    };
    const url = `https://data.alpaca.markets/v1beta3/crypto/latest/bars?symbols=${symbol}&timeframe=${timeframe}`;
    
    const response = await fetch(url, { headers });
    const data = await response.json();
    // Process candle data
}
```

## 📈 Trading Strategies

### Strategy 1: Inside Bar Breakout
1. Identify Inside Bar pattern
2. Wait for breakout of high or low
3. Enter on close above/below previous high/low
4. Stop loss: 1ATR below entry level
5. Target: 2-3x risk/reward ratio

### Strategy 2: HR + HR Momentum
1. Identify two consecutive high range candles
2. Confirm trend direction
3. Enter on trend continuation
4. Trailing stop as market moves favorably

### Strategy 3: LR + LR Breakout
1. Identify consolidation (LR + LR)
2. Set buy/sell orders above high and below low
3. Take first signal that triggers
4. Exit on close of breakout candle

## ⚠️ Risk Disclaimer

**This tool is for educational purposes only. It should not be considered as financial advice.**

- Past performance is not indicative of future results
- Trading involves substantial risk of loss
- Always use proper risk management
- Start with small position sizes
- Never risk more than you can afford to lose
- Backtest strategies before live trading
- Consider using a stop loss on every trade

## 🤝 Contributing

Have ideas for improvements? Found a bug? Feel free to:
1. Open an issue on GitHub
2. Submit a pull request with enhancements
3. Suggest new features or patterns to analyze

## 📞 Support

For issues, questions, or suggestions:
- Open an issue: [GitHub Issues](https://github.com/MONI2303/trading-website/issues)
- Check documentation in the "Learn CRT" tab
- Review the code comments for implementation details

## 📚 References

- **CRT Resources:** Trading education platforms
- **Technical Analysis:** Investopedia, TradingView
- **Chart.js:** https://www.chartjs.org/
- **Market APIs:** Alpha Vantage, Finnhub, IEX Cloud

## 📄 License

MIT License - Feel free to use, modify, and distribute.

## 👨‍💻 Author

Created by **MONI2303**

---

**Ready to trade smarter with CRT? 📊 Start analyzing now!**
