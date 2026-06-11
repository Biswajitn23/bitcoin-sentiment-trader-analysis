# Bitcoin Market Sentiment vs Trader Performance Analysis

## Overview

This project explores the relationship between Bitcoin market sentiment and trader performance using historical trading data from Hyperliquid and the Bitcoin Fear & Greed Index.

The objective is to understand how trader behavior, profitability, and risk-taking patterns change under different market sentiment conditions such as Fear, Greed, Extreme Fear, and Extreme Greed.

---

## Datasets

### 1. Bitcoin Fear & Greed Index

Columns:

* timestamp
* value
* classification
* date

### 2. Hyperliquid Historical Trading Data

Columns:

* Account
* Coin
* Execution Price
* Size Tokens
* Size USD
* Side
* Timestamp IST
* Start Position
* Direction
* Closed PnL
* Transaction Hash
* Order ID
* Crossed
* Fee
* Trade ID
* Timestamp

---

## Objective

The analysis focuses on the following questions:

* Does trader profitability vary across market sentiment conditions?
* Which sentiment produces the highest win rate?
* How does trading activity change during Fear and Greed periods?
* Do traders take larger positions under specific market conditions?
* What actionable insights can be extracted to support trading decisions?

---

## Methodology

1. Loaded and inspected both datasets.
2. Performed data quality checks.
3. Converted timestamp fields into a common date format.
4. Merged trading records with daily sentiment classifications.
5. Analyzed:

   * Trading activity
   * Profitability
   * Win rate
   * Position sizing
   * Top-performing traders
6. Derived insights and trading recommendations based on observed patterns.

---

## Key Findings

### Trading Activity

* Fear recorded the highest trading activity with 61,837 trades.
* Extreme Fear recorded the lowest trading activity with 21,400 trades.

### Profitability

| Sentiment     | Average PnL |
| ------------- | ----------: |
| Extreme Greed |       67.89 |
| Fear          |       54.29 |
| Greed         |       42.74 |
| Extreme Fear  |       34.54 |
| Neutral       |       34.31 |

* Fear generated the highest cumulative profit.
* Extreme Greed produced the highest average profit per trade.

### Win Rate

| Sentiment     | Win Rate |
| ------------- | -------: |
| Extreme Greed |   46.49% |
| Fear          |   42.08% |
| Neutral       |   39.70% |
| Greed         |   38.48% |
| Extreme Fear  |   37.06% |

* Extreme Greed achieved the highest win rate.
* Extreme Fear produced the lowest win rate.

### Position Size

| Sentiment     | Avg Position Size (USD) |
| ------------- | ----------------------: |
| Fear          |                   7,816 |
| Greed         |                   5,737 |
| Extreme Fear  |                   5,350 |
| Neutral       |                   4,783 |
| Extreme Greed |                   3,112 |

* Traders allocated the largest position sizes during Fear periods.
* Extreme Greed had the smallest average position size.

### Top Trader Analysis

* The most profitable trader generated more than 2.14 million in realized profit.
* Profitability was concentrated among a relatively small number of accounts.

---

## Hidden Patterns

* Traders appeared more aggressive during Fear periods by allocating larger position sizes.
* Extreme Greed delivered both the highest average profit per trade and the highest win rate.
* Higher trading activity did not necessarily result in higher profitability per trade.
* Market sentiment influenced both trading behavior and trade outcomes.

---

## Trading Recommendations

1. Consider monitoring market sentiment as an additional decision-making factor.
2. Apply stricter risk controls during Extreme Fear conditions.
3. Avoid assuming larger position sizes automatically lead to better performance.
4. Use sentiment indicators alongside technical and risk management strategies.
5. Study the behavior of consistently profitable traders to identify effective trading patterns.

---

## Repository Structure

```text
bitcoin-sentiment-trader-analysis
│
├── images
│   ├── trade_count_by_sentiment.png
│   ├── win_rate_by_sentiment.png
│   ├── position_size_by_sentiment.png
│   └── top_traders.png
│
├── notebooks
│   └── analysis.ipynb
│
├── README.md
├── requirements.txt
└── .gitignore
```

---

## Tools Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Jupyter Notebook

---

## Author

Biswajit
