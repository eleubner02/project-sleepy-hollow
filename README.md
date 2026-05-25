# Project Sleepy Hollow
## 1. Concept
An end-to-end automated statistical pipeline predicting the daily Day-Ahead to Real-Time (DA/RT) spread for the Hudson Valley NYISO node (EASTVIEW_138_KV_38W32_REV_LBMP_I)
The engine utilizes a dual-model approach: a Logistic Regression model to predict spread direction, and an ARIMA time-series model to forecast spread magnitude.
## 2. Deliverables
* The Engine: A Python script hosted and executed automatically via GitHub Actions every morning at 7:00 AM EST.
* The Tear-sheet: A daily automated email reporting:
  * Today's Direction Prediction (Logistic) & Magnitude Prediction (ARIMA).
  * Yesterday's PnL & Grade (Model vs. Actual).
  * Rolling 30-day directional accuracy.
* The Post-Mortem: A 2-page highly technical write-up detailing model architecture, out-of-sample performance, and physical grid deductions.
## 3. Tech Stack
* Language & IDE: Python, VS Code.
* Data Ingestion: gridstatus open-source API package.
* Modeling: scikit-learn (Logistic Regression), statsmodels (ARIMA), pandas.
* Automation: GitHub Actions (cron scheduling/execution), smtplib (email routing).
* Version Control: Git / GitHub.
## 4. Risks / Challenges
Scope creep. The urge to add more nodes, more complex neural networks, or heavily engineered news scrapers will threaten the 10-week timeline. Success relies on ruthless prioritization of the MVP (Minimum Viable Product).
## 5. Timeline: 
* Ten Weeks (2026.05.25 - 2026.07.31)
## 6. Phase 2 Features
Lightweight NLP macro-news sentiment score (HuggingFace).
Custom NYISO API scraper to replace gridstatus.
