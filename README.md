# Short-Horizon Analysis of Implied Volatility in 1-Day-to-Expiration Equity Options

This repository documents a personal research project examining the short-horizon behavior of implied volatility in one-day-to-expiration (1-DTE) equity options. The goal of the project is to study whether short-dated implied volatility exhibits structure beyond simple persistence assumptions over intraday time intervals.

The focus is on empirical statistical analysis and methodological clarity rather than trading outcomes or performance.


# Project Overview

Implied volatility for ultra-short-dated options is often treated as highly noisy and reactive. This project explores whether measurable short-term structure exists in 1-DTE option implied volatility when observed at regular intraday intervals.

Rather than attempting to optimize trading strategies, the project evaluates short-horizon behavior by comparing observed IV changes to a naïve persistence-based baseline.



# Data Scope

- Equity option chain snapshots collected at fixed intraday intervals  
- Focus on contracts with one day or less to expiration  
- Analysis centered on near-the-money contracts selected by strike proximity or delta range  

All data handling is structured to support repeatable statistical evaluation.

---

# Methodology (High-Level)

Option Chain Data
↓
Filter 1-DTE Contracts
↓
Select Near-ATM Strikes
↓
Compute Implied Volatility Metrics
↓
Baseline Model (IV Persistence)
↓
Short-Horizon IV Change Measurement
↓
Statistical Evaluation and Visualization


# Algorithm Outline (Pseudocode)

For each trading day:
Retrieve option chain snapshots at fixed intraday intervals

For each snapshot:
    Filter contracts with DTE ≤ 1
    Select near-the-money contracts
    Record implied volatility metrics

For each time step:
    Measure short-horizon IV changes
    Compare observed IV to persistence-based baseline
    Store error metrics for analysis

Aggregate results across trading days and evaluate statistical behavior.


---

## Evaluation Approach

Analysis focuses on:
- Short-horizon IV changes across intraday intervals  
- Comparison against a naïve persistence assumption  
- Error behavior and stability across different market conditions  

Results are evaluated using standard statistical error measures and visual analysis.

---

## Current Status

This repository contains documentation and methodological outlines only. Source code, datasets, and implementation details are intentionally excluded at this stage.

---

## Notes

- This project is exploratory and research-focused  
- No claims are made regarding profitability or trading performance  
- The repository is intended to document methodology and analytical approach  

---

## Disclaimer

This project is for informational and educational purposes only and does not constitute investment advice.


