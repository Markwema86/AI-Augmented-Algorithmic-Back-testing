# AI-Augmented-Algorithmic-Back-testing
The Objective: Build a systematic trading strategy that combines traditional technical indicators with AI-driven sentiment analysis, and back-test its profitability.

# The Theory: 
Institutional funds do not deploy capital based on gut feelings. Every strategy must be rigorously tested against historical data to calculate maximum drawdown, Sharpe ratio, and alpha generation.

# Execution Steps:

1. # The Baseline Strategy:
Use pandas to calculate a fast (50-day) and slow (200-day) Simple Moving Average (SMA) for an index ETF like the SPY. Generate buy signals when the 50-day crosses above the 200-day (a "Golden Cross").

2. # The Vectorized Back-test:
Instead of looping through rows (which is slow), use vectorized operations in NumPy to calculate the cumulative returns of this strategy versus a simple "buy and hold" approach.

3. # The AI Sentiment Overlay:
This is where you become an AI Engineer in finance. Mock up a dataset of daily financial news headlines. Use a pre-trained NLP model via the HuggingFace pipeline to score the daily sentiment from -1 (bearish) to 1 (bullish).

4. # The Fusion:
Modify your trading algorithm to only execute the SMA "buy" signal if the 7-day rolling average of the AI sentiment score is positive.
