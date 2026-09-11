# 📈 Quantitative Portfolio Management & Risk Analytics

[![Python](https://img.shields.io/badge/Python-3.9%2B-3776AB.svg?logo=python&logoColor=white)](#)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626.svg?logo=jupyter&logoColor=white)](#)
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458.svg?logo=pandas&logoColor=white)](#)
[![NumPy](https://img.shields.io/badge/NumPy-Numerical%20Computing-013243.svg?logo=numpy&logoColor=white)](#)
[![Finance](https://img.shields.io/badge/Domain-Quantitative%20Finance-emerald.svg)](#)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

> A rigorous computational finance repository covering risk-adjusted returns, downside volatility, historical drawdowns, and Value at Risk (VaR) models implemented in Python and Jupyter Notebooks.

---

## 🧮 Mathematical Formulations & Methodologies

### 1. Compounded Returns & Annualization
For a monthly return series $r_t$ over $N$ observation periods:
$$\text{Compounded Return} = \prod_{t=1}^N (1 + r_t) - 1$$
$$\text{Annualized Return } R_{ann} = (1 + R_{comp})^{12 / N} - 1$$
$$\text{Annualized Volatility } \sigma_{ann} = \sigma_{monthly} \cdot \sqrt{12}$$

### 2. Risk-Adjusted Performance (Sharpe Ratio)
Measuring excess return per unit of volatility relative to the risk-free rate $R_f$:
$$\text{Sharpe Ratio} = \frac{R_p - R_f}{\sigma_p}$$

### 3. Maximum Drawdown & Wealth Index
Tracking capital degradation from previous historical peaks:
$$\text{Wealth Index}_t = W_0 \cdot \prod_{i=1}^t (1 + r_i)$$
$$\text{Peak}_t = \max(\text{Wealth Index}_{1 \dots t})$$
$$\text{Drawdown}_t = \frac{\text{Wealth Index}_t - \text{Peak}_t}{\text{Peak}_t}$$

### 4. Value at Risk (VaR) & Downside Risk
- **Historic VaR:** Percentile distribution cutoff based on empirical historical price behavior.
- **Parametric Gaussian VaR:** $VaR_\alpha = -(\mu + z_\alpha \sigma)$.
- **Cornish-Fisher VaR:** Correcting for non-Gaussian properties (excess skewness $S$ and kurtosis $K$):
  $$\tilde{z}_\alpha = z_\alpha + \frac{1}{6}(z_\alpha^2 - 1)S + \frac{1}{24}(z_\alpha^3 - 3z_\alpha)(K - 3) - \frac{1}{36}(2z_\alpha^3 - 5z_\alpha)S^2$$
- **Conditional VaR (Expected Shortfall):** Expected loss given that a loss exceeds the VaR threshold:
  $$CVaR_\alpha = -\mathbb{E}[R \mid R \le -VaR_\alpha]$$

---

## 📓 Notebook Directory

| Notebook | Focus Area | Key Metrics & Topics Covered |
| :--- | :--- | :--- |
| **`Returns Lab Basics.ipynb`** | Return series analytics | Compounded returns, price-to-return transformations, volatility annualized scaling, multi-asset comparison. |
| **`Risk Adjusted Returns.ipynb`**| Downside & tail risk | Sample variance, Sharpe Ratio rankings, Skewness, Kurtosis, Semi-deviation, Historic & Parametric VaR, Cornish-Fisher expansion. |
| **`LabSessionDrawdown.ipynb`** | Capital preservation | Wealth index construction, cumulative peak calculation, historical drawdown trajectories, crash analysis (1975, 1987, 2000, 2008). |

---

## 📊 Datasets Included

- **`Portfolios_Formed_on_ME_monthly_EW (1).csv`**: Kenneth French Data Library monthly equally-weighted portfolio returns categorized by market capitalization deciles (SmallCap to LargeCap) spanning multiple market cycles.
- **`sample_prices.csv`**: Controlled synthetic price series used for testing return and drawdown formulas.

---

## 🚀 Environment Setup & Quickstart

```bash
# 1. Clone the repository
git clone https://github.com/arslantariq364/Investment-Management-.git
cd Investment-Management-

# 2. Create virtual environment
python3 -m venv venv
source venv/bin/activate

# 3. Install analytical stack
pip install numpy pandas matplotlib scipy jupyter

# 4. Launch Jupyter Notebook
jupyter notebook
```

---

## 👨‍💻 Author

**Arslan Tariq**  
*Computer Science Undergraduate @ FAST NUCES*  
*Specialization: AI, Machine Learning & Quantitative Systems*  
[GitHub Profile](https://github.com/arslantariq364)

---

## 📜 License

Distributed under the MIT License. See [LICENSE](LICENSE) for details.
