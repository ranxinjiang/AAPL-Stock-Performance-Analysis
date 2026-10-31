# AAPL Stock Performance Analysis

Statistical analysis of Apple Inc. (AAPL) stock performance over one year of daily trading data.

## Overview

This project uses descriptive statistics, time-series charts, and moving averages to analyze AAPL's price and volume behavior, investigates three events tied to the year's biggest price and volume moves, and develops a data-driven 30-day price range.

## Data

- **Source:** Yahoo Finance (finance.yahoo.com)
- **Period:** September 29, 2025 to September 25, 2026 (250 trading days)
- **Fields:** Date, Open, High, Low, Close, Adj Close, Volume
- The analysis uses the daily **Close** and **Volume** columns. Close was chosen over Adj Close to describe the price investors actually saw each day.

## Methods

- Descriptive statistics (mean, median, standard deviation, min/max) for closing price and volume
- Time-series charts of price and volume, plus monthly volatility (standard deviation of daily returns)
- 30-day and 60-day moving averages and their crossover points
- Event analysis comparing the 5 trading days before and after three key dates
- 30-day price range built by scaling full-year daily volatility to 21 trading days (square root of time), then tested against every 21-day stretch in the data

## Key Findings

- AAPL rose about **34%** over the period, from $254.43 to $341.07, and finished at its highest close of the year.
- The largest swings came around company news: Mac and iPad price hikes (−6.12% on June 25, 2026), a report on the new iPhone lineup (+4.84% on July 2), and fiscal Q3 earnings with a weak forecast (−7.35% on July 31). Only the earnings drop held for the following week.
- Not every volume spike was news-driven: the busiest day (June 26) lined up with the Russell index reconstitution, and December 19, 2025 was a "triple witching" day.
- Projected 30-day range: **about $317 to $365**. Across 229 past 21-day stretches, 64.2% would have landed inside it, close to the ~68% a one-standard-deviation range should capture.

## Files

| File | Contents |
|---|---|
| `aapl_stock_analysis.ipynb` | Full analysis notebook (Google Colab), with all code, charts, and written analysis |
| `aapl_stock_report.pdf` | Final written report |
| `AAPL.csv` | Raw daily price and volume data from Yahoo Finance |

## Tools

Python (pandas, matplotlib), Google Colab
