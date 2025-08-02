# Finsearch_A36_OptionPricingModels
End term report of team A36: Neepun, Rishabh, Dev, Prince on the topic of Option pricing Models &amp; their Accuracy.
## 🏁 Conclusion

This project set out to evaluate the effectiveness of the **Black-Scholes Model (BSM)** in pricing options — using a synthetic dataset mimicking real-world Nifty50 index options. We implemented the BSM formula from scratch and benchmarked its predictions against simulated market prices to identify areas where the model aligns with or deviates from expected behavior.

---

### Project Summary

-  **Model Used**: Black-Scholes Analytical Model  
-  **Data Source**: Artificially generated options data inspired by Nifty50 index option structure  
-  **Comparison**: BSM Price vs. Simulated Market Price  
-  **Evaluation Metrics**:
- **Root Mean Squared Error (RMSE)**: **37.49**
- **Mean Absolute Error (MAE)**: **26.67**
- **Mean Absolute Percentage Error (MAPE)**: **4.27%**
- **R² Score**: **0.9922**

These values indicate that the Black-Scholes model performs with **very high predictive accuracy** on average across the dataset, but as expected, some errors still persist based on option characteristics.

---

### Key Visual & Analytical Insights

#### **Scatter Plot: Market vs. BSM Price**
- Shows strong clustering around the ideal diagonal line, especially for ITM and ATM options.
- Deviations visible for OTM options, which the BSM tends to overprice or underprice.

#### **Error Distribution (Histogram & Boxplot)**
- **Call options** had an average pricing error of **+11.49 (OTM)** and **+12.46 (ITM)**, but **-44.53 for ATM**, showing occasional overpricing.
- **Put options** had tighter error ranges with minimal average error: **+2.33 (ITM)** and **-3.50 (OTM)**.
- Visuals suggest that **ATM calls show most instability** under BSM.

#### **Error vs. Time to Expiry**
- Shorter-dated options (low time-to-expiry) had wider spread in pricing error.
- Model appears less reliable as expiry nears, consistent with real-world market inefficiencies near expiration.

#### **Correlation Heatmap**
- Highest correlation of pricing error was with **Implied Volatility** and **Strike Price**, suggesting BSM sensitivity to these variables.
- **Spot Price** and **Time to Expiry** showed moderate correlation with pricing errors.

---

### Final Takeaways

- The **Black-Scholes model is robust but imperfect**, especially when:
  - Volatility is high and variable
  - Options are deep OTM or near expiry
- Our visualizations provide a comprehensive understanding of how different option types and conditions affect pricing accuracy.
- These insights mirror real-world limitations, validating the need for more flexible models such as:
  - **Monte Carlo Simulations**
  - **Stochastic Volatility Models**
  - **Volatility Surface Calibration**

---

### Group Contributions (for video context)

Each member contributed to specific phases:
- Data generation & structuring (e.g., expiry, volatility design), this phase involved getting the data from the NSE site and cleaning it to fit our    parameter needs. This dataframe generation is the essence of getting an accurate and bonafide prediction between the real world
- BSM model coding & integration, coding the math and introducing parameters to compare the real world
- Visualization & error analysis 
- Report writing & video script preparation

This comprehensive workflow highlights the interdisciplinary nature of financial modeling — combining **theory, coding, data analysis, and communication**.

---

