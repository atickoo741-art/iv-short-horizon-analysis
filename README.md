# Overview

This project studies how implied volatility (IV) behaves around earnings announcements and whether it provides useful information about post-earnings price movement. Earnings are major market events with high uncertainty, which makes them a good setting to test how well the options market prices risk.

While implied volatility usually rises before earnings, this project looks deeper to see whether that increase actually signals meaningful information or is mostly a mechanical feature of how options are priced.

# Main Research Question

Does implied volatility before earnings help explain post-earnings price moves, or is the commonly observed volatility increase simply expected and already priced in?

More specifically, the project examines whether comparing current implied volatility to a stock’s own historical earnings behavior provides more insight than looking at absolute volatility levels alone.

# Methodology

To avoid using future information, the study uses walk-forward testing developed with python, meaning models and comparisons are built using only data available before each earnings event and evaluated only on data that comes afterward. This approach reflects how analysis would work in real time.

The analysis compares:

Pre-earnings implied volatility

Historical implied volatility around past earnings

Historical realized price moves after earnings

Instead of focusing on absolute volatility values, the project uses relative comparisons. Current implied volatility is evaluated against a stock’s own past earnings volatility to determine whether the market may be underpricing or overpricing the expected move.

Data is analyzed across multiple time periods to check that patterns are not driven by a single market environment.

# Key Findings

Implied volatility almost always increases before earnings.

Absolute implied volatility levels do not explain post-earnings returns very well.

Comparing implied volatility to historical implied and realized earnings moves is much more informative.

When implied volatility is low relative to a stock’s past earnings moves, post-earnings outcomes tend to be more uneven.

These patterns appear consistently across different market periods.

# What This Means

The pre-earnings volatility increase happens largely because of how volatility is calculated and how earnings risk is added into option prices, not because the market is consistently adjusting its expectations in a predictive way.

Any potential edge comes from identifying situations where the market is mispricing earnings risk relative to its own history, rather than from simply buying volatility because earnings are approaching.

This suggests that earnings volatility should be analyzed on a stock-by-stock basis using historical context, instead of relying on broad assumptions.

# Limitations

Results are based on historical data and may change as market structure evolves.

The project does not account for all real-world trading constraints.

Findings describe tendencies, not guaranteed outcomes.

This project does not predict earnings direction or fundamentals.

# Disclaimer

This project is for educational and research purposes only and does not provide investment advice.
Past performance does not guarantee future results.
