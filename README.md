# Finsearch_A36_OptionPricingModels

**End term report of team A36 on the topic of Option pricing Models & their Accuracy**.

## Project Overview

This project aimed to **evaluate the effectiveness of the Black-Scholes Model (BSM) in pricing options**. We implemented the BSM formula from scratch and benchmarked its predictions against simulated market prices to identify areas where the model aligns with or deviates from expected behaviour.

The analysis was conducted using a **synthetic dataset mimicking real-world Nifty50 index options**, artificially generated data inspired by the Nifty50 index option structure. The data generation phase involved obtaining data from the NSE site and cleaning it to fit our specific parameter needs, which was crucial for achieving accurate and bona fide predictions compared to real-world scenarios.

## Group Information

*   **Group Number**: A36
*   **Team Members**: Neepun, Rishabh, Dev, Prince
*   *Contributors listed on GitHub include:* neepun06, SirCoolerArc (Rishabh Kumar)

## Group Contributions

This project involved a comprehensive workflow highlighting the interdisciplinary nature of financial modelling, combining theory, coding, data analysis, and communication. Each member contributed to specific phases of the project:

*   **Data generation & structuring**: This phase involved creating the synthetic dataset, including the design of expiry and volatility parameters, and cleaning data obtained from the NSE site to fit our model's needs.
*   **BSM model coding & integration**: This involved coding the mathematical formulas of the Black-Scholes Model and integrating parameters to facilitate comparison with real-world scenarios.
*   **Visualization & error analysis**: Developing visual representations of the data and conducting detailed analysis of the model's pricing errors.
*   **Report writing & video script preparation**: Compiling the findings into this end-term report and preparing the script for the accompanying video.

## Project Structure

The repository for this project is organised into the following directories and files:

. ├── data/              # Contains data related files ├── report/            # Contains project reports ├── scripts/           # Contains scripts used for analysis and model implementation ├── video/             # Contains video related content └── README.md          # This file, providing an overview of the project


## Key Findings & Conclusions

Our evaluation indicates that the **Black-Scholes model performs with very high predictive accuracy on average across the dataset**, achieving an **R² Score of 0.9922**. However, as expected, some errors persist based on specific option characteristics, highlighting that the **Black-Scholes model is robust but imperfect**.

### Performance Metrics

*   **Root Mean Squared Error (RMSE)**: **37.49**
*   **Mean Absolute Error (MAE)**: **26.67**
*   **Mean Absolute Percentage Error (MAPE)**: **4.27%**

### Visual & Analytical Insights

*   **Scatter Plot (Market vs. BSM Price)**: Shows **strong clustering around the ideal diagonal line, especially for In-The-Money (ITM) and At-The-Money (ATM) options**. **Deviations are visible for Out-of-The-Money (OTM) options**, which the BSM tends to overprice or underprice.
*   **Error Distribution (Histogram & Boxplot)**:
    *   **Call options** showed an average pricing error of **+11.49 (OTM)** and **+12.46 (ITM)**, but **-44.53 for ATM**, indicating occasional overpricing.
    *   **Put options** had tighter error ranges with minimal average error: **+2.33 (ITM)** and **-3.50 (OTM)**.
    *   Visuals suggest that **ATM calls show the most instability under BSM**.
*   **Error vs. Time to Expiry**: **Shorter-dated options (low time-to-expiry) had a wider spread in pricing error**. The model appears less reliable as expiry nears, which is consistent with real-world market inefficiencies near expiration.
*   **Correlation Heatmap**: The **highest correlation of pricing error was observed with Implied Volatility and Strike Price**, suggesting BSM's sensitivity to these variables. **Spot Price and Time to Expiry showed moderate correlation with pricing errors**.

### Final Takeaways

The Black-Scholes model's limitations are particularly evident when:

*   **Volatility is high and variable**.
*   **Options are deep OTM or near expiry**.

These insights mirror real-world limitations and validate the need for more flexible models, such as:

*   **Monte Carlo Simulations**
*   **Stochastic Volatility Models**
*   **Volatility Surface Calibration**

### Group Contributions (for video context)

Each member contributed to specific phases:
- Data generation & structuring (e.g., expiry, volatility design), this phase involved getting the data from the NSE site and cleaning it to fit our    parameter needs. This dataframe generation is the essence of getting an accurate and bonafide prediction between the real world
- BSM model coding & integration, coding the math and introducing parameters to compare the real world
- Visualization & error analysis 
- Report writing & video script preparation

This comprehensive workflow highlights the interdisciplinary nature of financial modeling — combining **theory, coding, data analysis, and communication**.

## Technologies Used

The primary language used for this project was **Jupyter Notebook (100.0%)** [5], indicating the use of Python for implementation and analysis.
