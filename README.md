# Volatility Modeling Using the Heston Model

## Project Overview

This project aims to model the volatility of financial assets using the **Heston model**, a popular stochastic volatility model. Unlike the Black-Scholes model, which assumes constant volatility, the Heston model incorporates volatility that changes over time, providing a more realistic representation of market behavior.

The goal of this project is to simulate and analyze stock price movements and volatility patterns over time. The Heston model is particularly useful for pricing options and managing risk in financial markets, as it captures **volatility clustering** and **mean reversion** in volatility, which are key characteristics of real financial data.

## Key Features

- **Stochastic Volatility**: The model assumes that volatility is not constant but follows its own process that is influenced by market dynamics.
  
- **Stock Price Simulation**: The stock price is simulated based on the evolving volatility over time. This allows for more accurate predictions and insights into asset price behavior.

- **Mean Reversion in Volatility**: The variance (volatility) tends to revert toward a long-term average, representing real-world market behavior where volatility tends to stabilize after large movements.

- **Risk Management and Pricing**: The model is useful for **option pricing** and **risk management** by accounting for the fact that volatility is unpredictable and can change rapidly.

## How the Model Works

1. **Initialization**:
   - The initial stock price and volatility are set at the beginning of the simulation.
   - The parameters of the model include the risk-free rate, long-term volatility, volatility of volatility, and the correlation between asset price and volatility.

2. **Simulation Process**:
   - For each time step (e.g., daily trading), the model generates random changes (known as Brownian motions) for both the stock price and its volatility.
   - Volatility is updated based on a mean-reverting process, which means that it tends to return to a long-term average over time.
   - The stock price is updated using a formula that factors in both the expected return and the changing volatility.

3. **Output**:
   - The simulation produces two main outputs: the **stock price path** and the **volatility path**. These show how the stock price and volatility evolve over time, offering insights into potential future price movements.

4. **Applications**:
   - This model is commonly used in **option pricing**, especially for **European options**. It helps in understanding the underlying volatility structure of the market and allows for more accurate predictions of asset price behavior.

## Conclusion

The Heston model provides a more sophisticated and realistic approach to modeling volatility compared to traditional models. By capturing the dynamics of volatility, it helps in making better-informed decisions for pricing options, hedging, and managing financial risks. This project simulates real-world market behavior, making it a valuable tool for those working in financial modeling, risk management, and quantitative finance.

## Requirements

- Python 3.x
- `numpy`
- `pandas`
- `matplotlib`
- `yfinance` (for fetching financial data)

## Installation

To install the necessary dependencies, run the following command:

```bash
pip install numpy pandas matplotlib yfinance

