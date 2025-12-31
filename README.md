# data-science
test 
ds_ankul_singh/
│
├── notebook_1.ipynb
├── notebook_2.ipynb   (optional)
│
├── csv_files/
│   ├── cleaned_trader_data.csv
│   ├── sentiment_merged_data.csv
│
├── outputs/
│   ├── pnl_vs_sentiment.png
│   ├── volume_vs_sentiment.png
│   ├── leverage_distribution.png
│
├── ds_report.pdf
└── README.md


import pandas as pd

sentiment = pd.read_csv("Fear_Greed_Index.csv")
trades = pd.read_csv("Hyperliquid_Trader_Data.csv")


merged = trades.merge(sentiment, left_on='date', right_on='Date', how='inner')


# Data Science Assignment – Web3 Trading Team

## Candidate Name
Ankul Singh

## Objective
Analyze how trader behavior aligns or diverges from Bitcoin market sentiment
(Fear vs Greed) to uncover hidden trading patterns.

## Datasets
- Bitcoin Fear & Greed Index
- Hyperliquid Historical Trader Data

## Structure
- notebook_1.ipynb → Main analysis (Google Colab)
- csv_files/ → Processed datasets
- outputs/ → Visualizations
- ds_report.pdf → Final summarized insights

## How to Run
1. Open notebook_1.ipynb in Google Colab
2. Upload datasets
3. Run all cells sequentially

## Key Insights
- Traders increase leverage during Greed phases
- Fear phases show reduced volume but higher volatility
- Consistent traders outperform emotional traders
