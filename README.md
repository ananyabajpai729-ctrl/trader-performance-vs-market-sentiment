# trader-performance-vs-market-sentiment
Analyzing how market sentiment (Fear/Greed) influences trader behavior and profitability using historical trading data.
# Trader Performance vs Market Sentiment Analysis

## Overview
This project explores how market sentiment (Fear, Greed, Neutral) impacts trader behavior and performance using historical trading data.

The goal is to identify patterns in profitability, trading behavior, and risk-taking across different market conditions, and use those insights to suggest simple strategy improvements.

---

## Dataset
The analysis uses two datasets:

### 1. Market Sentiment Data
- Contains daily sentiment labels (Fear, Greed, Neutral)
- Includes a sentiment score and classification for each date

### 2. Trader Data (Hyperliquid)
- Trade-level data including:
  - Account
  - Trade size (USD)
  - Execution price
  - Buy/Sell side
  - Closed PnL (profit/loss)
  - Timestamp

---

## Methodology

### Data Preparation
- Converted timestamps to a common date format
- Merged trader data with sentiment data using date
- Cleaned sentiment labels (merged extreme categories)
- Removed rows with missing values

### Feature Engineering
- Created a **Win column**:
  - 1 if PnL > 0  
  - 0 otherwise  
- Filtered out trades with zero PnL for better accuracy

### Analysis
- Compared performance across sentiment:
  - Average PnL  
  - Win rate  
  - Average trade size  

- Performed segmentation:
  - Divided traders into **High** and **Low** groups based on trade size
  - Analyzed performance across both sentiment and segments

---

## Key Insights

- Traders achieve **higher profits during Greed periods**, though win rates are slightly higher during Fear.
- **Trade sizes are largest during Fear**, indicating higher risk-taking behavior.
- **Neutral markets show the lowest profitability**, suggesting weaker trading opportunities.
- **High-size traders dominate overall profits**, while low-size traders generate relatively small returns.

---

## Strategy Recommendations

- During **Greed periods**, traders may benefit from slightly increasing exposure to capture stronger market moves.
- During **Fear periods**, reducing position size can help manage risk, as larger trades do not necessarily lead to better outcomes.

---

## Setup Instructions

### Requirements
Make sure you have Python installed (3.8+ recommended).

Install required libraries:

```bash
pip install pandas numpy matplotlib seaborn
