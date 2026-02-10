# Monte-Carlo-Simulation-GBM-VaR-CVar

## Overview
This project implements a Monte Carlo Simulation Framework to model the future price behaviour of an equity index (VOO) using Geomwtric Brownian Motion (GBM).

According to John C.Hull (*Options, Futures, and Other Derivatives*), financial assest prices are often modeled as stochatic processes in order to capture uncertainty.
Geometric Brownian Motion is one of the most commonly used models for equity prices
because it ensures positive prices and normally distributed returns.

Monte Carlo simulation is a numerical technique that generates many possible future
outcomes by repeatedly simulating random price movements. It is widely used in
financial engineering for risk analysis and scenario-based evaluation.

---

## Model Assumptions

The equity price \( S_t \) is assumed to follow Geometric Brownian Motion:

\[
dS_t = \mu S_t dt + \sigma S_t dW_t
\]

where:
- \( \mu \) is the expected (real-world) return  
- \( \sigma \) is the volatility  
- \( dW_t \) is a Brownian motion  

---

## Monte Carlo Simulation Methodology

1. The GBM process is discretized over daily time steps.
2. Random shocks are drawn from a standard normal distribution.
3. Thousands of price paths are simulated over the investment horizon.
4. The distribution of terminal prices is analyzed.

---

## Simulated Price Paths

![Monte Carlo Price Paths](figures/price_paths.png)

The figure above shows a subset of simulated equity index price paths generated
using the GBM model.

---

## Terminal Price Distribution

![Terminal Price Distribution](figures/final_price_hist.png)

This histogram shows the distribution of terminal prices obtained from the Monte
Carlo simulation.

---

## Profit and Loss (P&L)

Profit and loss is defined as:

\[
\text{P\&L} = S_T - S_0
\]

Positive values indicate gains, while negative values represent losses.

---

## Value at Risk (VaR)

Value at Risk (VaR) measures the potential loss in value of an investment over a
specified time horizon at a given confidence level.

VaR at the 95% confidence level represents the loss threshold that is exceeded in
only 5% of the worst outcomes.

---

## Conditional Value at Risk (CVaR)

Conditional Value at Risk (CVaR), also known as Expected Shortfall, measures the
average loss given that the loss has exceeded the VaR threshold. CVaR provides a
more complete description of tail risk than VaR alone.


## Risk Metrics Summary

![P&L Distribution](figures/pnl_hist.png)

The simulated P&L distribution is used to compute:
- Probability of loss
- Value at Risk (95%)
- Conditional Value at Risk (95%)


## Project Structure

## Conclusion

This project demonstrates how Monte Carlo simulation under a Geometric Brownian
Motion framework can be used to analyze equity price uncertainty and quantify
downside risk using VaR and CVaR.

## Reference
Hull, J. C. *Options, Futures, and Other Derivatives*. Pearson Education.
