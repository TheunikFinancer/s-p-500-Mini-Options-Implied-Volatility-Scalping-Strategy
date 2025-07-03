#  S&P 500 Mini Options — Implied Volatility Scalping Strategy

##  Strategy Overview

This project implements an **Implied Volatility (IV) Scalping Strategy** on **S&P 500 Mini Options**, targeting short-term fluctuations in implied volatility rather than directional price movement.

###  Core Strategy Logic

- **Sell Options** when **IV ≥ 35%**  
  → Assumes options are overpriced; short premium strategies are used

- **Buy Options** when **IV ≤ 25%**  
  → Assumes options are underpriced; long premium strategies are used

- **Stop-Loss: 35%**  
  → Exit the position if loss reaches 35% of the premium

The strategy aims to exploit **mean-reverting behavior** of implied volatility, using neutral positions like straddles and strangles.

---

##  Project Structure

```bash
.
├── data/                  # Historical IV and price data
├── notebooks/             # Jupyter notebooks for analysis & backtesting
├── strategy/              # Core logic and helper functions
├── results/               # Backtest performance and plots
├── README.md              # Project documentation
└── requirements.txt       # Python dependencies


## Backtesting Logic
Load historical implied volatility and options chain data. Trigger trades based on IV crossing thresholds (≥35% for sell, ≤25% for buy).Apply delta-neutral setups (e.g., ATM straddles or strangles).Enforce 35% stop-loss on premium paid or collected
### Track performance metrics:
Win rate
Average return per trade
Drawdown
Cumulative P&L

# Tools & Libraries
pandas / numpy — Data manipulation
matplotlib  — Visualization
