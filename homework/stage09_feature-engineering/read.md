# Rationale Behind Features

## 1. 7-Day Rolling Mean (`rolling_mean`)
- **Definition:** A moving average of the last 7 days’ closing prices.  
- **Purpose:**  
  - Smooths out daily noise and volatility.  
  - Helps identify **short-term trends** (whether the stock is gradually rising or falling).  
  - Traders often use moving averages for buy/sell signals (e.g., when the price crosses above/below the moving average).  

---

## 2. Weekly Percentage Change (`pct_change`)
- **Definition:** The percent change in price compared to 7 days earlier.  
- **Purpose:**  
  - Shows **momentum**: whether the stock is gaining or losing value week over week.  
  - Useful for spotting bullish or bearish patterns.  
  - Important for **risk management**, since large changes indicate higher volatility.  

---

## 3. Weekly Average Price (`weekly_avg`)
- **Definition:** The average closing price over the last 7 days.  
- **Purpose:**  
  - Provides a benchmark for the stock’s “typical” price in the short term.  
  - Smooths short-term swings and gives context for whether the current price is high or low.  
  - Often used in **portfolio strategies** to detect overvaluation or undervaluation.  

---

## 📌 Summary
- **Rolling mean** → short-term trend signal.  
- **Percentage change** → momentum indicator.  
- **Weekly average** → baseline price context.  