# ds_anhad

# Trader Behavior vs Market Sentiment

This repository contains my submission for the **Junior Data Scientist – Trader Behavior Insights** assignment.

The project analyzes how trading performance and risk behavior change across different market sentiment regimes using historical trade data aligned with the Bitcoin Fear & Greed Index.

---

## Project Structure

ds_anhad/
├── analysis.ipynb
├── visualization.ipynb
├── csv_files/
│ ├── analysis_df.csv
│ ├── fear_greed_index.csv
│ ├── historical_data.csv
│ └── sentiment_summary.csv
├── outputs/
│ ├── efficiency_vs_sentiment.png
│ ├── trade_size_vs_sentiment.png
│ ├── profit_vs_efficiency.png
│ └── value_vs_trade_size.png
├── ds_report.pdf
└── README.md

---

## Notebooks

### analysis.ipynb
Main analysis notebook containing:
- Data loading and cleaning  
- Sentiment encoding and date alignment  
- Definition of performance metrics  
- Aggregation and summary generation  

Running this notebook reproduces all analytical results.

---

### visualization.ipynb
Visualization-only notebook that:
- Loads precomputed CSV outputs  
- Generates final charts used in the report  
- Saves figures to the `outputs/` directory  

No preprocessing or metric recomputation is performed here.

---

## Metrics Used

- **Profit Rate** – share of trades with positive closed PnL  
- **Average Trade Size** – mean capital deployed per trade (USD)  
- **Efficiency** – closed PnL normalized by trade size  
- **Median PnL** – used alongside averages due to skewed distributions  

Efficiency is emphasized to avoid conclusions driven purely by trade size.

---

## Report

A concise summary of methodology, results, and interpretations is provided in:

**ds_report.pdf**

---

## Reproducibility

- Analysis was performed in Google Colab  
- Intermediate outputs are stored in `csv_files/`  
- Results can be reproduced by running the main analysis notebook end to end  
