# Exotic Option Pricing Engine (Monte Carlo & Python)

This project, developed for the M.Sc. in Quantitative Banking and Finance, builds a Python-based Monte Carlo engine to price complex, path-dependent exotic options.

---
### 📄 Key Project Documents
* **[View the Jupyter Notebook (Main Code)](Exotic_Options.ipynb)**
* **[View the Final Assignment (PDF)](docs/HW_03_exercises.pdf)**
---

## Project Objectives & Features

The pricing engine is built to value complex derivatives not solvable with closed-form solutions:

1.  **Basket Call Option:**
    * [cite_start]Prices a European call option whose payoff depends on a weighted basket of **three correlated assets** [cite: 909-910].
    * [cite_start]Implements **Cholesky decomposition** to accurately model the correlated random walks of the underlying assets[cite: 918, 972].

2.  **Path-Dependent Barrier Options:**
    * [cite_start]**Up-and-Out Call:** Prices a standard barrier option where the payoff is contingent on the asset's price never crossing an upper barrier (`B_up`) during its lifetime[cite: 1011, 1017].
    * **Complex Dual-Barrier Option:** Prices a custom-defined option with two distinct, time-dependent barriers:
        * Must stay **above** `B_down` for the first half of its life ($t_0$ to $T/2$).
        * [cite_start]Must stay **below** `B_up` for the second half of its life ($T/2$ to $T$) [cite: 1170-1171].

## Methodology & Tools

* **Valuation Model:** Monte Carlo Simulation
* [cite_start]**Stochastic Process:** Geometric Brownian Motion (GBM) [cite: 1026]
* **Core Tools:** Python, NumPy, SciPy, Matplotlib
* [cite_start]**Mathematical Core:** Cholesky Decomposition (for correlation) [cite: 918][cite_start], Statistical Analysis (Sampling vs. Discretization Error) [cite: 1100-1107].
