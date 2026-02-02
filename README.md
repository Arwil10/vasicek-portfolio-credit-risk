## Credit Risk Portfolio Simulator (Vasicek Model)
A Python-based tool to simulate credit portfolio losses using Monte Carlo method. This project demonstrates the fundamental difference between independent defaults and correlated credit risk using the Vasicek Model.

# Overview
The simulator compares two worlds:
1. Naive Model: Assumes defaults are independent (Correlation = 0).
2. Vasicek Model: Assumes defaults are driven by a common systemic factor (e.g., the economy), introducing Asset Correlation ($\rho$).

# Key Metrics Calculated 
Expected Loss (EL): The average loss anticipated (the mean).
Value at Risk (VaR 99.9%): The maximum loss at a high confidence level, showing the "worst-case scenario."
Economic Capital (EC): The capital cushion needed to survive systemic shocks ($VaR - EL$).

# The Math
The model uses the Asset Value approach:
# $$A_i = \sqrt{\rho} * Z + \sqrt{1-\rho} * \epsilon_i$$

$Z$ is the Systemic Factor (Global Economy).
$\epsilon_i$ is the Idiosyncratic Risk (Specific to the firm).
$\rho$ is the Asset Correlation.

# Results
The simulation clearly visualizes the "Fat Tail" phenomenon: while both models share a similar Expected Loss, the correlated model shows significantly higher extreme losses (VaR), requiring much more Economic Capital.
