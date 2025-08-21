# Project Title
**Stage:** Problem Framing & Scoping (Stage 01)
## Problem Statement
In high-frequency trading (HFT) and algorithmic trading, predicting short-term price movements is crucial for making profitable trades and managing risk. The Limit Order Book (LOB) contains detailed information about all outstanding buy and sell orders, providing insights into supply-demand dynamics for the partucular instrument. However, the order book evolves rapidly, and trades often cluster in time, making it difficult to extract actionable signals.

This project aims to combine Hawkes process modeling of trade arrivals with XGBoost machine learning model to predict short-term mid-price movements. By leveraging both statistical features of event clustering and traditional LOB features (spread, imbalance, depth), the project seeks to improve prediction accuracy and provide interpretable metrics for traders.
## Stakeholder & User
- **Decision Maker:** Quant researchers or algorithmic trading teams who design high-frequency strategies.  
- **End Users:** Trading algorithms or quantitative analysts using real-time or historical predictions to make market entry/exit decisions.  
- **Timing & Workflow Context:**  
  - Predictions operate on **sub-second to second intervals**, supporting short-term trade execution.  
  - Workflow integrates **LOB snapshot ingestion → feature extraction → predictive model output**.

---

## Useful Answer & Decision
- **Type:** Predictive  
- **Metric:** Next mid-price movement (Up/Down) in 1–5 seconds  
- **Artifacts Delivered:**  
  - LOB dataset will be cleaned and features will be derived  
  - Hawkes intensity and excitation features will be derived 
  - XGBoost predictive model to predict mid-price movemenr
  - Visualizations: mid-price, spread, imbalance, Hawkes intensity, feature importance  
  - Streamlit dashboard for interactive monitoring

---

## Assumptions & Constraints
- **Data Availability:** Free APIs from Binance will be used to provide sufficient LOB depth data and trade timestamps.  
- **Capacity:** Can process and store LOB snapshots locally; no GPU required.  
- **Latency:** Predictions are evaluated on historical data; real-time deployment is out of scope for this stage as it would require a low latency language like cpp and optimal use of multithreading and other things 
- **Compliance:** Public API usage; no sensitive trading data involved.  
- **Model Scope:** Short-term (seconds) price prediction; long-term price trends not addressed.

---

## Known Unknowns / Risks
- **Data Gaps:** Missing snapshots or WebSocket drops may affect feature quality → handled with forward-fill and masking.  
- **Market Regime Changes:** Volatility spikes or illiquidity periods may reduce prediction accuracy → visualize rolling accuracy.  
- **Hyperparameter Sensitivity:** XGBoost and Hawkes decay/alpha parameters need tuning → grid search or default heuristics.

---

## Lifecycle Mapping

| Goal | Stage | Deliverable |
|------|-------|------------|
| Understand order book microstructure & predict short-term price moves | Problem Framing & Scoping (Stage 01) | Project proposal & roadmap |
| Collect LOB and trade data | Data Acquisition & Cleaning (Stage 02) | Cleaned LOB dataset |
| Model order arrivals & excitation patterns | Feature Engineering (Stage 03) | Hawkes intensity/excitation features |
| Predict short-term mid-price movement | Modeling (Stage 04) | XGBoost predictive model |
| Evaluate model performance | Evaluation & Visualization (Stage 05) | Accuracy, confusion matrix, feature importance plots |
| Deliver insights for potential trading strategy | Deployment & Reporting (Stage 06) | Visual dashboards or report summarizing predictive insights |
## Repo Plan
/data/, /src/, /notebooks/, /docs/ ; cadence for updates
