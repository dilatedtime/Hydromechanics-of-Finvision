# Financial Models in Python

This repository contains two finance notebooks created for Finvision work. One studies option pricing with the Black-Scholes model. The other explains and simulates the Vasicek interest-rate process.

## Notebooks

### `BlackScholes.ipynb`

- Implements European call and put pricing
- Calculates delta, gamma, vega, theta, and rho
- Downloads SPY price and option-chain data with `yfinance`
- Compares market option prices with theoretical prices
- Saves the combined option data to `options_data.csv`

The notebook uses a fixed 3% risk-free rate and 20% volatility for demonstration. Live option chains change over time, and contracts at or past expiry can produce divide-by-zero warnings.

### `Vasicek_Model.ipynb`

- Introduces the Vasicek stochastic differential equation
- Derives its conditional expectation and variance
- Simulates mean-reverting rate paths with `aleatory`
- Plots how the starting value, long-run mean, volatility, mean-reversion speed, and time horizon change the process
- Includes a separate Wiener-process simulation

## Run the notebooks

```bash
git clone https://github.com/dilatedtime/Hydromechanics-of-Finvision.git
cd Hydromechanics-of-Finvision
python -m venv .venv
python -m pip install jupyter numpy pandas scipy matplotlib yfinance aleatory
jupyter notebook
```

Open either notebook and run its cells in order. The Black-Scholes notebook needs internet access for current Yahoo Finance data.

These notebooks are educational. Their fixed assumptions and live market inputs are not suitable for trading or risk decisions without further validation.

