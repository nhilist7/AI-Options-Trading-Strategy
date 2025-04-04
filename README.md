# 🧠 ICICIdirect Breeze Live Options Trading Bot

This repository contains a **Python-based live options trading bot** that uses **ICICIdirect's BreezeConnect API** for real-time execution. The strategy is based on a combination of **RSI**, **Supertrend**, and **Volume Spike** to generate directional option buying signals on NIFTY.

---

## ⚙️ Strategy Logic

-  **Buy Call** when:
  - RSI crosses above threshold (default: 60)
  - Supertrend is positive (bullish)
  - Volume spike detected

-  **Buy Put** when:
  - RSI crosses below threshold (default: 40)
  - Supertrend is negative (bearish)
  - Volume spike detected

-  ATM Option is selected based on real-time spot price.
-  Live execution with BreezeConnect, trades are sent instantly to ICICIdirect account.

---

##  Features

-  Real-time signal generation using WebSocket tick data
-  Executes ATM CE/PE options based on strategy
-  Logs trade entries/exits with PnL to CSV
-  Risk control: one position at a time
-  Built-in indicators: RSI, Supertrend, Volume spike logic


---

