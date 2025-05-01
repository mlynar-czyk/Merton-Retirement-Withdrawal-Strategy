# Merton Retirement Withdrawal Strategy Calculator

![Merton Strategy](https://img.shields.io/badge/Retirement-Planning-blue)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6-yellow)
![Chart.js](https://img.shields.io/badge/Chart.js-3.9.1-green)

A sophisticated web-based tool that implements Robert Merton's dynamic approach to retirement withdrawal strategies using stochastic modeling of asset returns (geometric Brownian motion).

## Overview

This application provides a comprehensive implementation of Merton's retirement withdrawal strategy, which offers several advantages over traditional fixed-withdrawal approaches like the 4% rule. The calculator helps retirees determine sustainable withdrawal rates that adapt to market conditions while prioritizing essential expenses.

### Key Features

- **Stochastic Modeling**: Uses geometric Brownian motion to realistically simulate thousands of potential market scenarios
- **Essential vs. Discretionary Spending**: Separates necessary expenses from flexible spending
- **Dynamic Withdrawals**: Recalculates annually based on actual portfolio performance
- **Guardrails**: Implements limits on how much withdrawals can change year-to-year for stability
- **Portfolio Construction**: Models combined stock/bond portfolio with correlation effects
- **Rich Visualization**: Interactive charts showing portfolio projections and withdrawal amounts
- **Detailed Results**: Success rates, percentile analyses, and year-by-year breakdowns

## Theoretical Background

The implementation is based on Nobel laureate Robert Merton's portfolio theory and uses:

- **Geometric Brownian Motion (GBM)**: Models stock prices as following a log-normal distribution, capturing both drift (expected return) and volatility
- **Present Value Annuity Factor (PVAF)**: Used to calculate appropriate withdrawal rates based on portfolio value, expected returns, and remaining time horizon
- **Probability Analysis**: Shows the likelihood of meeting financial goals over different time horizons

The stochastic differential equation (SDE) for geometric Brownian motion is:

```
dS = μS dt + σS dW
```

Where:
- S is the asset price
- μ is the drift (expected return)
- σ is the volatility
- dW is a Wiener process (Brownian motion)

## Advantages Over Traditional Methods

Compared to fixed-rate withdrawal strategies like the 4% rule, Merton's approach:

1. **Adapts to market conditions**: Recalculates annually based on actual portfolio performance
2. **Accounts for volatility**: Explicitly models market volatility and correlation between asset classes
3. **Prioritizes essential spending**: Ensures basic needs are covered before allocating to discretionary expenses
4. **Optimizes for time horizon**: Adjusts withdrawals based on remaining life expectancy
5. **Models realistic market behavior**: Uses stochastic processes that better represent actual market behavior

## How To Use

1. Enter your current age and life expectancy
2. Input your portfolio details: current value, asset allocation, and essential expenses
3. Specify your guaranteed income sources (Social Security, pensions)
4. Adjust market parameters (expected returns, volatility, inflation) or use defaults
5. Click "Run Simulation" to generate a comprehensive analysis

## Simulation Results

The application provides:

- **Initial withdrawal amounts**: Annual and monthly suggestions based on your inputs
- **Success rate**: Percentage of simulations where essential expenses remained fully covered
- **Detailed projections**: Median, 10th percentile, and various other statistical measures
- **Interactive charts**: Visual representation of portfolio value and withdrawal projections
- **Year-by-year table**: Detailed breakdown of results for each year of retirement

## Technical Implementation

The calculator is implemented entirely in client-side JavaScript using:

- **JavaScript ES6**: Core implementation of the Merton strategy
- **Chart.js 3.9.1**: For interactive visualization of results
- **Box-Muller transform**: For generating normally distributed random variables
- **Responsive design**: Works on desktop and mobile devices

## Local Installation

1. Clone this repository
2. Open `index.html` in your browser
3. No server-side components or dependencies to install

## License

MIT License

## Acknowledgements

Based on the portfolio theory work of Nobel laureate Robert C. Merton, particularly his contributions to continuous-time finance and lifecycle investing.

## Disclaimer

This tool is for educational and informational purposes only. It is not financial advice. Consult with a financial professional before making investment decisions.
