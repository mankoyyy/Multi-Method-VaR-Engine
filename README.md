# Multi-Method-VaR-Engine
A Python engine comparing Historical, Parametric, and Monte Carlo VaR with Stress Testing.


# Multi-Method Value at Risk (VaR) Engine

## 📌 Overview
This project implements an end-to-end **Value at Risk (VaR) engine** to estimate the **maximum 1-day portfolio loss at 99% confidence**.  
It is designed from a **Model Risk Management (MRM)** perspective and compares multiple VaR methodologies with validation through **Backtesting** and **Stress Testing**.

## 💼 Portfolio
A $1,000,000 diversified portfolio:
- **SPY (30%)** – Equity market exposure  
- **TLT (40%)** – Long-term treasury hedge  
- **GLD (10%)** – Inflation & safe-haven asset  
- **NVDA (20%)** – High-beta technology exposure  

## ⚙️ VaR Methodologies
- **Historical VaR**  
  Non-parametric; uses empirical 1% return quantile. Captures fat tails but suffers from recency bias.
- **Parametric VaR**  
  Assumes multivariate normality; fastest but underestimates tail risk during crises.
- **Monte Carlo VaR**  
  Simulates 10,000 correlated scenarios using **Cholesky decomposition**; flexible and regulator-preferred.

## 🧪 Validation
- **Backtesting**: Counts VaR breaches vs expected frequency  
- **Stress Testing**: Custom “Tech Meltdown” scenario to test extreme regimes

## 🛠️ Tech Stack
Python, NumPy, Pandas, yfinance, Plotly

## 🚀 Run Instructions
```bash
git clone https://github.com/mankoyyy/MultiMethod-VaR-Engine.git
cd MultiMethod-VaR-Engine
pip install -r requirements.txt
python Multi_Method_VaR_Engine.ipynb
