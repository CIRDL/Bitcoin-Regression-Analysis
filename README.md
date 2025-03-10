# **Bitcoin and U.S. Financial Confidence: A Regression Analysis**

## **Project Overview**  
This repository contains an analysis of Bitcoin's relationship with U.S. financial confidence, using various economic indicators as proxies for global trust in the U.S. economy. The project explores whether Bitcoin behaves as a **"digital gold" safe haven asset** during economic instability or if its price is more correlated with traditional financial markets like the **S&P 500**.  

The study applies **regression modeling techniques** including **Ordinary Least Squares (OLS), ElasticNet, and Multivariate Adaptive Regression Splines (MARS)** to predict Bitcoin price movements based on macroeconomic factors.  

## **Repository Structure**  
📄 **Analysis.Rmd** – Primary R Markdown file for data analysis and modeling.  
📄 **bitcoin_data.csv** – Processed dataset containing financial indicators and Bitcoin price data.  
📄 **Technical Report.pdf** – A detailed write-up of the study, methodology, and key findings.  
📄 **Presentation.pdf** – A concise visual summary of the study’s results.  

## **Key Findings**  
- **Bitcoin and the S&P 500 are strongly correlated, with an asymmetric influence.**  
  - Bitcoin behaves somewhat like a **high-growth tech asset**, reacting disproportionately to shifts in equity market sentiment.  
  - Early adoption and speculative investors may have driven this correlation.  
- **Gold and S&P 500 interaction has a significant impact on Bitcoin’s price.**  
  - When the S&P 500 is strong and gold prices are low, Bitcoin’s appeal as a hedge asset diminishes.  
  - This suggests that Bitcoin is influenced by **two distinct investor groups**: tech-driven speculators and digital gold advocates.  
- **Non-linearity exists in Bitcoin’s relationship with economic indicators.**  
  - The **MARS model outperformed** linear models (OLS, ElasticNet), achieving an **adjusted R² of 0.945 and RMSE of 0.295**.  
  - This suggests that non-linear effects play a crucial role in Bitcoin price dynamics.  
- **Bitcoin’s price tends to grow under neutral market conditions, but key economic events can trigger declines.**  
  - High bias in the model indicates Bitcoin’s historical tendency to rise unless external market pressures intervene.

## **Methodology**  
1. **Data Collection & Processing:**  
   - Monthly data on **Bitcoin prices, S&P 500, gold prices, bond yields, and other economic indicators** was aggregated.  
   - Data was transformed (e.g., log transformations, OHLC feature engineering) and scaled for consistency.  
2. **Modeling Approaches:**  
   - **OLS:** A baseline linear regression model.  
   - **ElasticNet:** A regularized regression approach to handle multicollinearity.  
   - **MARS:** A non-linear regression model that captured key interactions and breakpoints.  
3. **Validation:**  
   - Models were evaluated using **10-fold cross-validation** on non-chronological training and testing splits.  

## **Reproducibility**  
To reproduce the analysis:  
1. Clone the repository:  
   ```bash
   git clone https://github.com/your-repo-name.git
   cd your-repo-name
   ```  
2. Open the **R Markdown** files in RStudio.  
3. Install required R packages (if needed):  
   ```r
   install.packages(c("tidyverse", "caret", "earth", "glmnet"))
   ```  
4. Run the **Analysis** scripts to generate results.  

## **Authors**  
- **Cesar Ramirez**  
- **Judah Anttila**  
- **Tyler Brassfield**  
- **Advisor: Dr. Charles Nicholson**  

## **License & Citation**  
This project is for **academic and research purposes**. While it has not been formally published, please reference the authors if you use or modify this work in any capacity.  
