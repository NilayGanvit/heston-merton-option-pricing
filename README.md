# Heston & Merton Option Pricing via Monte Carlo

This repository contains the implementation of advanced **option pricing models**. The focus is on extending beyond the Black-Scholes framework to incorporate **stochastic volatility** (Heston model) and **jump diffusion** (Merton model).

**Monte Carlo simulation** to price European, American, and barrier options, and compute option sensitivities (Greeks). Results are reported both in technical (model-driven) and non-technical (investment decision) formats.

---

## 📊 Models Implemented

* **Black-Scholes Model** (baseline reference)
* **Heston Model** (stochastic volatility, correlated with asset returns)
* **Merton Jump-Diffusion Model** (random price jumps)

---

## 🧮 Tasks & Features

* **European Options**: ATM call & put pricing under Heston and Merton models
* **American Options**: Pricing and comparison with European counterparts
* **Barrier Options**:

  * Up-and-In European Call (Heston)
  * Down-and-In European Put (Merton)
* **Greeks**: Delta and Gamma approximated via finite differences
* **Put-Call Parity Validation** across models
* **Strike Sweep Analysis**: Pricing options across multiple OTM, ATM, and ITM strikes

---

## ⚙️ Parameters

General parameters used throughout the project:

* Initial Stock Price: `S0 = 80`
* Risk-free Rate: `r = 5.5%`
* Volatility (BS baseline): `σ = 35%`
* Time to Maturity: `T = 0.25 years (3 months)`

**Heston Model parameters**:

* Initial Variance: `ν0 = 0.032`
* Mean Reversion Speed: `κν = 1.85`
* Long-term Variance: `θν = 0.045`
* Correlation: tested at `ρ = -0.30` and `ρ = -0.70`

**Merton Model parameters**:

* Jump Mean: `µ = -0.5`
* Jump Volatility: `δ = 0.22`
* Jump Intensities: `λ = 0.75` and `λ = 0.25`

---

## 🛠️ Technologies

* Python 3.x
* Jupyter Notebook / Google Colab
* Libraries: `numpy`, `pandas`, `matplotlib`, `scipy`

## 📈 Results

* Option prices are rounded to **two decimals** for clarity.
* Results are tabulated in both Jupyter outputs and included in the final PDF report.
* Comparison highlights how **volatility clustering (Heston)** and **price jumps (Merton)** create deviations from Black-Scholes prices.

## 📚 References

* Heston, S. L. (1993). *A Closed-Form Solution for Options with Stochastic Volatility with Applications to Bond and Currency Options*.
* Merton, R. C. (1976). *Option Pricing when Underlying Stock Returns are Discontinuous*.
* Hull, J. C. (2022). *Options, Futures, and Other Derivatives*.

---

Would you like me to **add example code snippets** (like a minimal Monte Carlo for the Heston model) in the README so your repo is more engaging for visitors?
