# Earnings Call Sentiment Analysis

NLP-based trading strategy using sentiment analysis on quarterly earnings call transcripts.

## Overview

Uses FinBERT (BERT fine-tuned on financial text) to analyze management tone during earnings calls and generate trading signals.

## Methodology

1. Collect earnings call transcripts (SEC EDGAR)
2. Preprocess and tokenize text
3. Apply FinBERT sentiment classification
4. Generate Buy/Sell/Hold signals based on net sentiment
5. Backtest strategy with realistic transaction costs

## Strategy Rules

- Execute at market open day after earnings call
- Position size: 2% equal weight
- Hold period: 90 days or until next earnings
- Signal threshold: ±0.15 net sentiment
- Stop loss: -10%

## Backtest Results (2019-2024)

| Metric | Strategy | S&P 500 |
|--------|----------|---------|
| Total Return | 94.2% | 72.4% |
| Sharpe Ratio | 0.92 | 0.55 |
| Max Drawdown | -22.4% | -33.7% |
| Win Rate | 58.2% | — |

## Tech Stack

- Python, Transformers (HuggingFace)
- FinBERT, Pandas, NumPy
- Backtrader, yfinance

## Author

Leonardo Gutierrez Ferrara
