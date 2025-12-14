
# An Empirical Study of Earnings Event Volatility


OVERVIEW
--------
This project looks at how implied volatility changes before corporate
earnings announcements and whether the common “IV ramp” actually
creates an edge. Many traders believe that buying options before
earnings is profitable simply because implied volatility usually rises
as the announcement approaches. This study tests whether that belief
is supported by data.

By separating implied volatility into normal day-to-day movement and
earnings-specific movement, the project shows that rising implied
volatility alone does not mean expected returns are increasing.

------------------------------------------------------------

MAIN QUESTION
-------------
Is the increase in implied volatility before earnings caused by the
market updating its expectations, or is it mostly a mechanical result
of time passing?

If the IV ramp is mostly mechanical, then strategies that rely only on
“buying the ramp” should lose money over time.

------------------------------------------------------------

CORE IDEA
---------
Implied volatility before earnings can be broken into two parts:

1) Ambient volatility  
   The stock’s usual day-to-day movement when no major events occur.

2) Event (earnings) volatility  
   The one-day move the market expects from the earnings announcement.

As earnings get closer, normal trading days are removed from the time
window while the earnings day remains. Because the same earnings risk
is spread across fewer days, quoted implied volatility increases even
if expectations do not change.

This creates the IV ramp.

------------------------------------------------------------

DATA USED
---------
• Liquid U.S. stocks with active options markets  
• Over 21,000 pre-earnings observations  
• Data from 2009 to the present  

Each observation looks at at-the-money options entered roughly two
weeks before earnings and exited before the announcement. Earnings
day risk is intentionally avoided so the focus stays on volatility
behavior, not earnings surprises.

Transaction costs and liquidity constraints are included to keep the
results realistic.

------------------------------------------------------------

WHAT WAS ANALYZED
----------------
The study compares the market’s current implied earnings move to:

• The implied move from the previous earnings  
• The average implied move from past earnings  
• The actual move from the previous earnings  
• The average actual move from past earnings  

These comparisons help determine whether the market is pricing the
earnings event cheaply or expensively relative to history.

------------------------------------------------------------

HOW RESULTS WERE TESTED
----------------------
The data is grouped into buckets based on these comparisons, and
returns are analyzed across time to see whether patterns are
consistent.

To avoid using future information, the study uses walk-forward
testing, where models are evaluated only on data that comes after
they are built.

------------------------------------------------------------

KEY FINDINGS
------------
• Implied volatility usually rises before earnings, but this alone is
  not a reliable edge  
• Absolute implied volatility levels do not explain returns well  
• Relative comparisons to past implied and realized earnings moves are
  much more informative  
• These patterns hold up across different market periods  

------------------------------------------------------------

WHAT THIS MEANS
---------------
The IV ramp happens mostly because of how volatility is calculated,
not because the market is consistently changing its expectations.

Any potential edge comes from identifying when the market is
underpricing the earnings move compared to its own history, not from
buying volatility simply because earnings are approaching.

------------------------------------------------------------

LIMITATIONS
-----------
• Results are based on historical data  
• Market structure can change over time  
• Findings do not guarantee future performance  
• This project does not predict earnings direction  

------------------------------------------------------------

DISCLAIMER
----------
This project is for educational and research purposes only and does
not provide investment advice.

Code is kept private and not included in the repository.

------------------------------------------------------------

AUTHOR
------
Aditya Tickoo
Independent Research Project

============================================================

