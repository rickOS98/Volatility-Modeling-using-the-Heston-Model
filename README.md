# Volatility Modeling using the Heston Model

This project focuses on modeling the volatility of financial assets using the **Heston Stochastic Volatility Model**. The Heston model is a popular model in quantitative finance that describes the evolution of asset prices and their volatility over time. This project involves simulating both the asset price and its stochastic volatility using the Heston model.

## Project Overview

The Heston model assumes that volatility is stochastic (changing over time) and mean-reverting, which provides a more realistic representation of market behavior compared to constant volatility models like the Black-Scholes model. This project generates a synthetic stock price and volatility path using the Heston model's mathematical framework, and simulates the asset's price evolution over a given period (e.g., 1 year with 252 trading days).

## Key Features

- **Stock Price Simulation**: The stock price is simulated based on both return dynamics and changing volatility, with volatility modeled as a mean-reverting process.
- **Stochastic Volatility**: The volatility is modeled as a stochastic process with mean-reversion towards a long-term average.
- **Volatility Clustering**: The model captures volatility clustering, which reflects the tendency of high volatility to follow high volatility periods, and low volatility to follow low volatility periods.
- **Mean-Reverting Volatility**: The variance (volatility) path exhibits mean reversion toward a long-term average, represented by the parameter θ.
  
## Model Equations

The Heston model consists of two main equations:

1. **Volatility Process**:  
   $$ v_t = v_{t-1} + \kappa (\theta - v_{t-1}) dt + \xi \sqrt{v_{t-1}} dW_v $$  
   Where:  
   - $v_t$ is the variance at time $t$ (volatility squared)
   - $\kappa$ is the rate of mean reversion
   - $\theta$ is the long-term variance (mean-reverting level)
   - $\xi$ is the volatility of volatility
   - $dW_v$ is the Brownian motion increment for volatility

2. **Stock Price Process**:  
   $$ S_t = S_{t-1} \exp \left[ ( \mu - \frac{1}{2} v_{t-1}) dt + \sqrt{v_{t-1}} dW_S \right] $$  
   Where:  
   - $S_t$ is the stock price at time $t$
   - $\mu$ is the risk-free rate
   - $dW_S$ is the Brownian motion increment for stock price
   - $v_{t-1}$ is the variance at the previous time step

## Project Workflow

1. **Data Fetching**: Historical financial data (e.g., Nifty50 index) is fetched using `yfinance`.
2. **Model Simulation**: The Heston model is implemented using Euler-Maruyama discretization to simulate stock price and volatility over time.
3. **Parameter Estimation**: Model parameters like $\kappa$, $\theta$, $\xi$, and $\rho$ are estimated based on historical data using statistical techniques such as Maximum Likelihood Estimation (MLE).
4. **Simulation Results**: Simulated paths for both stock prices and volatility are plotted, showing how the asset price evolves with changing volatility.

## Dependencies

To run this project, you will need the following Python libraries:

- `numpy`: For numerical computations
- `pandas`: For data manipulation and analysis
- `matplotlib`: For plotting the simulation results
- `yfinance`: For fetching historical financial data
- `scipy`: For optimization and statistical functions

You can install the required dependencies with:

```bash
pip install numpy pandas matplotlib yfinance scipy
