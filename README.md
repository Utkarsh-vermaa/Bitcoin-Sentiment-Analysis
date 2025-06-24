# Bitcoin Market Sentiment vs Trading Performance Analysis

## 🚀 Project Overview

This project explores the intricate relationship between Bitcoin market sentiment and trader performance using real-world data from the Fear & Greed Index and Hyperliquid trading platform. By analyzing market psychology alongside actual trading outcomes, we uncover actionable insights for developing smarter trading strategies.

## 📊 Datasets

### 1. Bitcoin Market Sentiment Dataset (`fear_greed_index.csv`)
- **Source**: Fear & Greed Index
- **Columns**: 
  - `date`: Trading date
  - `classification`: Sentiment category (Fear/Extreme Fear/Neutral/Greed/Extreme Greed)
  - `value`: Numerical sentiment score (0-100)
  - `timestamp`: Unix timestamp

### 2. Historical Trader Data (`historicaldata.csv`)
- **Source**: Hyperliquid trading platform
- **Columns**: Account, Coin, Execution Price, Size Tokens, Size USD, Side, Timestamp IST, Start Position, Direction, Closed PnL, Transaction Hash, Order ID, Crossed, Fee, Trade ID, Timestamp

## 🔍 Key Findings

### Market Sentiment Performance Summary

| Sentiment | Periods | Avg Daily PnL | Total PnL | Win Rate | Avg Volume | Avg Traders | Volatility |
|-----------|---------|---------------|-----------|----------|------------|-------------|------------|
| **Extreme Fear** | 14 | $52,794 | $739,110 | 32.7% | $8.18M | 11.4 | $101,262 |
| **Fear** | 91 | $36,892 | $3.36M | 32.9% | $5.31M | 6.9 | $96,612 |
| **Neutral** | 67 | $19,297 | $1.29M | 33.2% | $2.69M | 5.6 | $37,995 |
| **Greed** | 193 | $11,141 | $2.15M | 33.6% | $1.50M | 3.4 | $62,428 |
| **Extreme Greed** | 114 | $23,817 | $2.72M | 46.7% | $1.09M | 4.6 | $72,827 |

### 🎯 Key Insights

1. **Contrarian Strategy Works**: Extreme fear periods show the highest daily PnL ($52,794), suggesting opportunities during market panic
2. **Fear Premium**: Fear and extreme fear periods generate significantly higher returns despite lower win rates
3. **Greed Paradox**: Extreme greed periods show the highest win rate (46.7%) but moderate daily returns
4. **Volume-Sentiment Correlation**: Fear periods attract higher trading volumes and more active traders
5. **Volatility Arbitrage**: Extreme sentiment periods (both fear and greed) exhibit higher volatility, creating profit opportunities

## 📈 Correlation Analysis

### Strong Correlations (>0.7):
- **Trade Count ↔ Active Traders**: 0.797 (High activity breeds more activity)
- **Trade Count ↔ Total Volume**: 0.720 (Volume drives trading frequency)
- **Sentiment ↔ Value**: 0.959 (Sentiment scores align with market value)

### Notable Insights:
- **Avg PnL per Trade ↔ Profit Factor**: 0.696 (Profitable trades compound)
- **Total PnL ↔ Active Traders**: 0.440 (More traders = more opportunities)
- **Win Rate ↔ Avg PnL per Trade**: 0.341 (Quality over quantity)

## 🛠️ Technical Implementation

### Data Processing Pipeline
1. **Data Ingestion**: CSV parsing with robust error handling
2. **Temporal Alignment**: Synchronizing sentiment data with trading timestamps
3. **Feature Engineering**: Creating derived metrics (win rates, volatility, trader activity)
4. **Statistical Analysis**: Correlation matrices and performance aggregations
5. **Insight Generation**: Pattern recognition and strategy formulation

### Technologies Used
- **Python**: Data processing and analysis
- **Pandas**: Data manipulation and aggregation
- **NumPy**: Numerical computations
- **Matplotlib/Seaborn**: Data visualization
- **Jupyter Notebooks**: Interactive analysis

## 🎯 Trading Strategy Implications

### 1. **Contrarian Fear Strategy**
- **Trigger**: Extreme Fear periods (sentiment < 25)
- **Action**: Increase position sizes during panic
- **Expected**: Higher daily returns (~$52K vs $11K in greed)

### 2. **Greed Momentum Strategy**
- **Trigger**: Extreme Greed periods (sentiment > 75)
- **Action**: Focus on high-probability setups
- **Expected**: Higher win rates (46.7% vs 32.7% in fear)

### 3. **Volume-Based Positioning**
- **Insight**: Fear periods attract 5-8x more volume
- **Strategy**: Scale position sizes with sentiment-driven volume

### 4. **Volatility Harvesting**
- **Opportunity**: Extreme sentiment = higher volatility
- **Approach**: Volatility-adjusted position sizing

