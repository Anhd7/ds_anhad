# ds_anhad
Trader Behavior vs Market Sentiment

This repository contains my submission for the Junior Data Scientist – Trader Behavior Insights assignment.

The project analyzes how trading outcomes and risk behavior change across different market sentiment conditions using historical trade data combined with the Bitcoin Fear & Greed Index.

Project Structure
ds_anhad/
├── 01_data_pipeline_and_analysis.ipynb
├── 02_visualization_and_plots.ipynb
├── csv_files/
│   ├── analysis_df.csv
│   └── summary.csv
├── outputs/
│   ├── efficiency_vs_sentiment.png
│   ├── trade_size_vs_sentiment.png
│   ├── profit_vs_efficiency.png
│   └── value_vs_trade_size.png
├── ds_report.pdf
└── README.md

Notebooks
analysis.ipynb

Primary notebook containing the full analytical workflow:

Data loading and cleaning

Sentiment encoding and date alignment

Definition of performance and risk metrics

Aggregation and summary generation

Running this notebook reproduces all analytical outputs.

visualization.ipynb

Visualization-only notebook:

Reads precomputed CSV outputs

Generates final charts used in the report

Saves figures to the outputs/ directory

No preprocessing or metric calculations are performed here.

Metrics Used

Profit Rate – share of trades with positive closed PnL

Average Trade Size – mean capital deployed per trade (USD)

Efficiency – closed PnL normalized by trade size

Median PnL – used alongside averages due to skewed distributions

Efficiency is emphasized to avoid conclusions driven purely by trade size.

Report

A concise summary of methodology, results, and interpretations is provided in:

ds_report.pdf


The report focuses on behavioral patterns rather than surface-level statistics.

Reproducibility

Analysis was performed in Google Colab

All intermediate data outputs are stored in csv_files/

Results can be reproduced by running the main analysis notebook end to end
