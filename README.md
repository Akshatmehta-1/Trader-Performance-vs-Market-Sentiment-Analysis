# Trader-Performance-vs-Market-Sentiment-Analysis

## Overview

This project analyzes how market sentiment (Fear/Greed) influences trader behavior and performance using historical trading data from Hyperliquid and Bitcoin market sentiment data.

The objective is to identify patterns in trader performance and behavior across different market conditions and derive actionable trading strategies.

---

## Dataset

1. **Bitcoin Market Sentiment Dataset**

   * Columns: date, classification (Fear, Greed, Extreme Fear, Extreme Greed, Neutral)

2. **Historical Trader Data**

   * Includes: account, execution price, size, side, timestamp, closed PnL, etc.

---

## Methodology

### Data Preparation

* Cleaned both datasets (removed duplicates, checked missing values)
* Converted timestamps to datetime format
* Aligned both datasets on daily date level
* Merged datasets using date as key

### Feature Engineering

* Win flag (profit > 0)
* Trade size (USD)
* Trade frequency
* Daily PnL per trader
* Long/Short ratio
* Trade count per day

Note: Leverage data was not available, so trade size (USD) was used as a proxy for risk exposure.

---

## Analysis

### Performance vs Sentiment

* Compared PnL and win rate across sentiment categories
* Added drawdown proxy using average losses

### Behavior vs Sentiment

* Trade frequency across sentiment
* Average trade size
* Long vs short distribution

### Trader Segmentation

* High vs Low trade size traders
* Frequent vs Infrequent traders
* Consistent winners vs inconsistent traders

---

## Key Insights

* Traders perform best during Extreme Greed and worst during Extreme Fear
* High trade size increases profitability but does not improve win rate
* Frequent traders underperform compared to selective traders

---

## Strategy Recommendations

* Reduce trade size during Fear phases to manage downside risk
* Avoid overtrading; focus on selective opportunities for better performance

---

## Bonus (Clustering)

* Traders were grouped into behavioral clusters using KMeans
* Identified high-risk high-reward traders and low-risk underperformers

---

## How to Run

1. Install dependencies:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

2. Run the notebook:

```bash
jupyter notebook
```

3. Open and execute the notebook step-by-step

---

## Output

* Charts comparing sentiment vs performance
* Segmentation tables
* Clustering results

---

## Conclusion

Market sentiment significantly influences trader behavior and performance. However, disciplined trading (controlled size and frequency) consistently outperforms aggressive behavior.

## Dataset Link
* 1) https://drive.google.com/file/d/1PgQC0tO8XN-wqkNyghWc_-mnrYv_nhSf/view?usp=sharing (Bitcoin market sentiment (Fear/Greed))
* 2) https://drive.google.com/file/d/1IAfLZwu6rJzyWKgBToqwSmmVYU6VbjVs/view?usp=sharing (Historical Trader Data (Hyperliquid))

