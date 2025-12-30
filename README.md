# ds_anhad
project:
  title: Trader Behavior vs Market Sentiment
  description: >
    This repository contains the completed assignment for the
    Junior Data Scientist – Trader Behavior Insights role.
    The analysis studies how trader behavior (profitability,
    trade sizing, and efficiency) changes across different
    market sentiment regimes using historical trade data
    aligned with the Bitcoin Fear & Greed Index.

repository_structure:
  root: ds_anhad/
  contents:
    - file: 01_data_pipeline_and_analysis.ipynb
      description: Main analysis notebook (single source of truth)
    - file: 02_visualization_and_plots.ipynb
      description: Visualization-only notebook
    - directory: csv_files/
      files:
        - analysis_df.csv
        - summary.csv
    - directory: outputs/
      files:
        - efficiency_vs_sentiment.png
        - trade_size_vs_sentiment.png
        - profit_vs_efficiency.png
        - value_vs_trade_size.png
    - file: ds_report.pdf
      description: Final summarized analysis and insights
    - file: README.yaml
      description: Project overview and usage notes

notebooks:
  - name: 01_data_pipeline_and_analysis.ipynb
    role: Core analysis
    details:
      - Data loading
      - Data cleaning and type handling
      - Sentiment encoding (categorical, ordinal, continuous)
      - Trade and sentiment alignment
      - Metric definitions
      - Aggregation and summary table
    notes: >
      This notebook runs end-to-end and reproduces all
      analytical outputs. It is the primary notebook
      reviewers should refer to.

  - name: 02_visualization_and_plots.ipynb
    role: Visualization
    details:
      - Loads precomputed CSV outputs
      - Generates final plots used in the report
      - Saves plots to outputs directory
    restrictions:
      - No data cleaning
      - No feature engineering
      - No metric recomputation

metrics:
  profit_rate:
    description: Percentage of trades with positive closed PnL
  average_trade_size:
    description: Mean trade size in USD
  efficiency:
    description: Closed PnL divided by trade size (risk-adjusted return)
  median_pnl:
    description: >
      Used alongside averages due to the heavy-tailed
      nature of trading PnL distributions

analysis_notes:
  - Efficiency is treated as the primary performance metric
  - Binary sentiment encoding was avoided to preserve signal
  - Only overlapping date ranges between datasets were used

report:
  file: ds_report.pdf
  includes:
    - Objective and methodology
    - Summary statistics
    - Visual analysis
    - Behavioral insights
    - Practical trading implications
    - Limitations and future scope

environment:
  platform: Google Colab
  reproducibility: >
    All results are reproducible by running the main
    analysis notebook from top to bottom.

submission_compliance:
  - Repository structure follows provided assignment guidelines
  - All CSV outputs are stored under csv_files/
  - All visual outputs are stored under outputs/

contact:
  name: Anhad
  email: your_email_here
  github: your_github_link_here
  linkedin_or_portfolio: optional
