# Loan Loss Reserve Calculation

This project calculates the reserves needed to compensate potential loan losses, providing a "safety buffer" to cover expected losses over a one-year planning horizon. The goal is to estimate the expected losses (EL) and determine the required reserve using Monte Carlo simulations.

## Overview

The calculation of expected losses involves the following formula:

`EL = EAD × PD × LGD`

Where:
- **EAD (Exposure at Default)**: The outstanding loan amount at the time of default.
- **PD (Probability of Default)**: The likelihood that a borrower will default on the loan.
- **LGD (Loss Given Default)**: The percentage of loss in case of default, considering factors like collateral or financial guarantees.

In addition to the simple calculation, Monte Carlo simulations are used to model the uncertainty in **PD** and **LGD**:
- **PD** is modeled using a log-normal distribution, with the mean (`PD-mean`) and standard deviation (`PD-sigma`).
- **LGD** is modeled using a BetaPERT distribution with specified minimum, mode, and maximum values.

The simulation will run 50,000 iterations, and the following statistics will be computed:
- Median
- Mean
- 95th percentile

The 95th percentile will represent the "safety buffer" (expected losses) for the planning horizon.

## Data

The dataset includes loans with the following parameters:

| Loan  | EAD  | PD (Mean) | PD (Sigma) | LGD (Min) | LGD (Mode) | LGD (Max) |
|-------|------|-----------|------------|-----------|------------|-----------|
| Loan A | 1000 | 0.02      | 0.007      | 0         | 0.2        | 1         |
| Loan B | 2000 | 0.01      | 0.005      | 0         | 0.3        | 1         |
| Loan C | 2500 | 0.015     | 0.01       | 0         | 0.4        | 1         |

## Methodology

1. **Expected Loss Calculation**: Calculate the simple expected loss (EL) for each loan based on the formula provided.
2. **Monte Carlo Simulation**: Simulate 50,000 iterations of **PD** and **LGD** using the log-normal and BetaPERT distributions, respectively.
3. **Statistical Analysis**: Calculate the median, mean, and 95th percentile of the simulated expected losses.
4. **Visualization**: Generate a histogram of the simulated expected losses and display the results.

## Results

The 95th percentile of the simulated expected losses will represent the "safety buffer" required to cover potential loan defaults
