# Portfolio Optimization using Clustering and Modern Portfolio Theory

This project explores the integration of unsupervised machine learning techniques with quantitative finance to construct, optimise, and evaluate diversified investment portfolios. By leveraging clustering algorithms to enhance asset selection and applying Modern Portfolio Theory (MPT) to derive optimal allocations, we assess how data-driven approaches can improve portfolio performance in terms of both return and risk.

---

## Overview

- **Objective**: To apply clustering techniques for portfolio diversification and use MPT for optimizing asset weights, with a focus on maximizing risk-adjusted returns.
- **Machine Learning Methods**: KMeans and hierarchical (correlation-based) clustering, used to segment assets based on return and volatility profiles or correlation structures.
- **Financial Optimization**: Implementation of MPT using PyPortfolioOpt to compute maximum Sharpe ratio and minimum volatility portfolios.
- **Evaluation Framework**:
  - Manual and automated backtesting using the `bt` library
  - Rolling Sharpe ratio analysis to monitor performance consistency
  - Benchmarking against the S&P 500 index
- **Comparative Analyses**:
  - KMeans vs correlation-based clustering
  - Equal-weighted vs MPT-optimized portfolios
  - Strategy performance vs market benchmark

---

## Methodology

### Clustering for Diversification
- **KMeans Clustering**: Performed on annualized return and volatility metrics to group stocks with similar risk-return profiles.
- **Hierarchical Clustering**: Based on correlation distances to identify underlying asset relationships and minimize intra-cluster correlation.

### Portfolio Optimization
- **Modern Portfolio Theory (MPT)**: Used to determine optimal portfolio weights by maximizing the Sharpe ratio or minimizing volatility under realistic constraints (e.g., long-only portfolios).
- **Expected Returns & Covariance**: Estimated using historical price data via the `mean_historical_return` and `sample_cov` functions from PyPortfolioOpt.

### Performance Analysis
- **Backtesting**: Both manually (via pandas) and programmatically using `bt` to simulate rebalancing strategies.
- **Rolling Sharpe Ratio**: Used to track the stability of risk-adjusted returns over time.
- **Benchmark Comparison**: Portfolios are evaluated relative to a passive investment in the S&P 500 index (ticker: `^GSPC`).

---

## Python Packages Used

- Python, pandas, NumPy, Matplotlib
- `yfinance` (data sourcing)
- `scikit-learn`, `scipy` (clustering algorithms)
- `PyPortfolioOpt` (portfolio optimization)
- `bt` (backtesting engine)

---

## Key Findings

- MPT-optimized portfolios consistently outperformed equal-weighted allocations in terms of Sharpe ratio.
- Correlation-based clustering often yielded more stable portfolios due to improved asset independence.
- Both clustering-based strategies demonstrated superior risk-adjusted returns compared to the S&P 500 benchmark over the testing period.

---

## Takeaways

This project demonstrates the practical value of combining unsupervised learning with classical portfolio theory. Through thoughtful feature engineering, robust optimization techniques, and structured backtesting, we show how systematic investment strategies can be enhanced through machine learning frameworks.

---

## Files

- `Clustering_Portfolio.ipynb`: Full implementation and analysis (Jupyter Notebook)
- `README.md`: Project overview and methodology
