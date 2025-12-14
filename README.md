
#PROJECT: An Empirical Study of Earnings Event Volatility Mispricing


DESCRIPTION
-----------
This project analyzes how implied volatility behaves prior to corporate
earnings announcements and tests whether the pre-earnings "IV ramp"
represents genuine repricing of risk or a mechanical effect of time decay.

Total implied volatility is decomposed into two components:
  (1) Ambient (background) volatility
  (2) Event-specific (earnings jump) volatility

The analysis shows that rising implied volatility alone does not imply
positive expected value. Any persistent edge must come from mispricing
of the earnings event volatility relative to historical outcomes.

This repository contains research code only. It is not a live trading
system and does not generate executable trade signals.

--------------------------------------------------------------------

DATASET
-------
Universe        : Liquid U.S. equities
Liquidity filter: >= 20,000 avg daily option contracts
Sample size     : 21,000+ pre-earnings observations
Time period     : 2009 - present

Instrument      : ATM straddles
Entry timing    : ~14 days before earnings
Exit timing     : Prior to earnings announcement
Earnings gap    : Explicitly excluded
Costs modeled   : Commissions, slippage, liquidity constraints

--------------------------------------------------------------------

METHODOLOGY
----------
1. Identify pre-earnings option expiries spanning the earnings date
2. Estimate ambient volatility using pre-event or forward volatility
3. Back out event (earnings) volatility via variance additivity
4. Convert event volatility into implied earnings move
5. Compare implied earnings moves to:
     - Prior implied earnings move
     - Historical average implied earnings move
     - Prior realized earnings move
     - Historical average realized earnings move
6. Evaluate relationships using decile analysis and monotonicity tests
7. Validate results using walk-forward, expanding-window OOS testing

--------------------------------------------------------------------

KEY FINDINGS
------------
- The pre-earnings IV ramp is largely mechanical
- Absolute implied volatility levels are weak predictors
- Relative implied vs historical implied/realized measures show
  stable, monotonic relationships with outcomes
- Predictive relationships persist across time and market regimes
- Mispricing exists at the event volatility level, not in IV broadly

--------------------------------------------------------------------

REPO STRUCTURE
--------------
/data        : raw, interim, and processed datasets (not tracked)
/src         : core research modules
/scripts     : pipeline execution scripts
/notebooks   : exploratory analysis
/outputs     : figures and summary tables

--------------------------------------------------------------------

TECH STACK
----------
Python
NumPy
Pandas
SciPy
statsmodels
Custom research & backtesting pipeline

--------------------------------------------------------------------

NOTES
-----
- All validation is strictly out-of-sample
- Walk-forward testing uses expanding windows
- No proprietary parameters or live trading logic included

--------------------------------------------------------------------

DISCLAIMER
----------
This project is for educational and research purposes only.
It does not constitute investment advice.

--------------------------------------------------------------------

AUTHOR
------
Vasu Tickoo
Empirical Volatility Research
====================================================================
