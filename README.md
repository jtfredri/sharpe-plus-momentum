# Sharpe Ratio and Momentum Strategy – Norwegian Stocks

## Data

The file `norwegian_stocks.csv` contains **adjusted closing prices** for selected Norwegian stocks.

- Period: **2025-01-08 to 2026-02-03**
- Frequency: Daily

---

## Returns

Daily returns are computed as:

$$
R_t = \frac{P_t}{P_{t-1}} - 1
$$

where $P_t$ is the adjusted closing price at time $t$.

---

## Sharpe Ratio

The Sharpe ratio measures return relative to risk.

$$
S = \frac{\bar{R} - r_f}{\sigma}
$$

where:

- $\bar{R}$ = average return  
- $r_f$ = risk-free rate
- $\sigma$ = standard deviation of returns  

Higher Sharpe ratio means better return per unit of risk.

---

## Momentum Strategy

Momentum assumes that stocks that have performed well recently continue to perform well.

Momentum over a lookback period $L$ is calculated as:

$$
M_t = \frac{P_t}{P_{t-L}} - 1
$$

Stocks are ranked by momentum, and the strongest performers are selected.

In this project:
- Stocks with high momentum are selected
- The Sharpe ratio can be used as an additional filter to avoid high-volatility stocks

---

## Correlation Matrix

The correlation matrix measures how stocks move relative to each other.

$$
\rho_{ij} = \frac{\text{Cov}(R_i, R_j)}{\sigma_i \sigma_j}
$$

- Values close to **1** → stocks move together  
- Values close to **0** → weak relationship  
- Values close to **-1** → move in opposite directions  

Example:
- **Equinor** and **Aker BP** show high correlation.
- This is expected because both operate in the oil and energy industry.

---

## Goal

The goal is to:
- Compare stock performance
- Identify high-momentum stocks
- Evaluate risk-adjusted returns using the Sharpe ratio
- Understand relationships between stocks through correlation
