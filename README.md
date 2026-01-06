# Earnings Volatility: Is the Pre-Earnings "Ramp" Actually Informative?

## Project Overview
Before a company reports earnings, there is almost always a noticeable spike in volatility. The common assumption is that this "ramp" indicates the market is bracing for a significant price move.

I built this project to test that assumption. I wanted to see if higher pre-earnings expectations actually correlate with larger realized moves, or if the volatility increase is largely mechanical and already priced in.

The Goal: To understand if earnings expectations are priced correctly relative to historical context, rather than trying to predict the direction of the stock price.

## Methodology
Because historical options data (implied volatility) is often difficult to source for free, I used a price-based proxy to model expectations:

Measuring Realized Moves: Calculated the absolute percentage change from the market close immediately before earnings to the first close after.

Building an Expectation Proxy: Used a "walk-forward" median of past earnings moves to simulate what a reasonable participant might expect based on the stock's own history.

Relative Context: I scaled these expectations to see if they were high or low relative to that specific stock's history. This allowed for a cleaner comparison across different tickers like NVDA and JPM.

## Key Findings

#### 1. Absolute Expectations are a Poor Predictor
The walk-forward testing showed that expected moves are much smoother than actual outcomes. In many cases, massive earnings moves occurred even when expectations were at "normal" levels. Knowing that expectations are high doesn't necessarily mean the stock is going to move more than usual.

#### 2. The Signal is in the "Relative" Mispricing
The most interesting results came from the bucket analysis. When looking at expectations relative to a stock's history:

Low Relative Expectations: These events actually saw the largest median realized moves.

High Relative Expectations: As the "hype" increased, the actual realized volatility tended to decrease.

This suggests that the market is often most surprised when it has become complacent—meaning the biggest moves happen when expectations are low compared to historical norms.

## Conclusion
The results suggest that the pre-earnings volatility ramp isn't an especially reliable predictor of the actual move size. Instead, the real "edge" appears to be in identifying relative mispricing—specifically when the market is under-pricing an event compared to how that stock has behaved in the past.

## Limitations
Universe: Analysis was limited to AAPL, NVDA, GOOGL, AMZN, and JPM (2022–2024).

Data: Used a price-based proxy instead of actual implied volatility from option chains.

Disclaimer: This is an educational project and does not constitute financial advice.
