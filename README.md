An Empirical Study of Earnings Event Volatility Mispricing
Overview

This project investigates how implied volatility behaves leading up to corporate earnings announcements and examines whether the commonly observed pre-earnings “IV ramp” reflects genuine repricing of risk or is largely a mechanical effect of time passing.

By decomposing total implied volatility into ambient (background) volatility and event-specific (earnings jump) volatility, the analysis shows that rising implied volatility before earnings does not, by itself, imply positive expected value. Instead, any persistent edge must come from mispricing of the event volatility component relative to historical outcomes.

This repository presents the research framework, methodology, and empirical findings. It is intended as a study of volatility pricing dynamics rather than a trading recommendation.

Research Motivation

A common narrative among options traders is that buying straddles before earnings is profitable because implied volatility tends to rise as the announcement approaches. However, implied volatility is an annualized measure that aggregates variance over the remaining life of an option.

As time passes and lower-volatility ambient days roll off, the same fixed earnings event variance is averaged over fewer remaining days, mechanically increasing quoted implied volatility.

This raises the core research question:

Does the IV ramp represent new information being priced, or is it primarily a mathematical artifact?

Conceptual Framework

The analysis separates implied volatility into two components:

Ambient Volatility
The background day-to-day volatility of the stock outside of earnings events.

Event (Earnings) Volatility
A one-day jump component representing the market’s expected earnings move.

Using variance additivity, total variance over an option’s life is modeled as the sum of ambient variance across non-event days and a single event-day variance. This decomposition allows the implied earnings move to be estimated and compared against historical implied and realized outcomes.

Dataset

Universe: Liquid U.S. equities

Liquidity Filter: ≥ 20,000 average daily option contracts

Sample Size: 21,000+ pre-earnings observations

Time Period: 2009–present

Instrument: At-the-money straddles

Expiration: Nearest monthly expiration after earnings

Holding Period: ~14 days before earnings, exit prior to announcement

Transaction Costs: Commissions, slippage, and liquidity constraints included

The analysis explicitly avoids holding positions through the earnings announcement in order to isolate volatility repricing effects from earnings gap risk.

Methodology
Signal Construction

For each earnings event, the following relative measures are computed:

Current implied earnings move vs prior earnings implied move

Current implied earnings move vs historical average implied move

Current implied earnings move vs prior realized earnings move

Current implied earnings move vs historical average realized earnings move

Absolute implied volatility levels are evaluated but found to be weaker and less stable predictors.

Empirical Testing

Decile-based performance analysis

Correlation and multicollinearity checks (VIF)

Walk-forward out-of-sample testing using expanding windows

Stability checks across multiple market regimes

All model evaluation is performed strictly out of sample to avoid look-ahead bias.

Key Findings

The pre-earnings implied volatility ramp is largely mechanical and does not imply positive expected value by itself

Absolute implied volatility levels show weak and unstable relationships with outcomes

Relative implied versus historical implied and realized earnings measures exhibit stable, monotonic relationships

These relationships persist across time and market regimes under walk-forward validation

The results indicate that persistent mispricing exists at the event volatility level rather than in implied volatility more broadly.

Implementation Notes

While the research framework can be translated into systematic strategies, this repository focuses on empirical analysis, signal robustness, and proper research methodology.

No live trading signals or proprietary parameters are disclosed.

Tech Stack

Python

NumPy, Pandas, SciPy

statsmodels

Custom backtesting and data pipelines

Disclaimer

This project is for educational and research purposes only.
It does not constitute investment advice or a recommendation to trade securities.

Author

Vasu Tickoo
Quantitative Research Project
