# Monte Carlo Simulation GBM with VaR/CVaR

## Overview
This project implements a Monte Carlo Simulation Framework to model the future price behaviour of an equity index (VOO) using Geomwtric Brownian Motion (GBM).

According to John C.Hull (*Options, Futures, and Other Derivatives*), financial assest prices are often modeled as stochatic processes in order to capture uncertainty.
Geometric Brownian Motion is one of the most commonly used models for equity prices
because it ensures positive prices and normally distributed returns.

Monte Carlo simulation is a numerical technique that generates many possible future
outcomes by repeatedly simulating random price movements. 

----

## Monte Carlo Simulation Methodology

1. The GBM process is discretized over daily time steps.
2. Random shocks are drawn from a standard normal distribution.
3. Thousands of price paths are simulated over the investment horizon.
4. The distribution of terminal prices is analyzed.

----

## Value at Risk (VaR)

Value at Risk (VaR) measures the potential loss in value of an investment over a
specified time horizon at a given confidence level.

VaR at the 95% confidence level represents the loss threshold that is exceeded in
only 5% of the worst outcomes.

----

## Conditional Value at Risk (CVaR)

Conditional Value at Risk (CVaR), also known as Expected Shortfall, measures the
average loss given that the loss has exceeded the VaR threshold. 

The simulated P&L distribution is used to compute:
- Probability of loss
- Value at Risk (95%)
- Conditional Value at Risk (95%)

----

## Conclusion

This project demonstrates how Monte Carlo simulation under a Geometric Brownian
Motion framework is used to analyze equity price uncertainty and quantify
downside risk using Value at Risk and Conditional Value at Risk.

---

## Reference
Hull, J. C. *Options, Futures, and Other Derivatives*. Pearson Education.
