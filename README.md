# US_Inflation_Effects_Analysis

## Project Synopsis

In this project, I will analyze **how inflation impacts interest rates, consumer spending, investment, GDP (growth domestic product) and overall economy in the US**. The goal is to understand the relationships between these economic factors, identifying patterns and correlations using publicly available economic data. This debated topic could be of great significance and usefulness as understanding these relationships could explain the role of inflation in both economic recessions and expansions. I have chosen the United States as the subject of this project due to its rich availability of economic data, making it an ideal case for thorough and data-driven analysis.

---
  
## Objectives

1. **Understand Inflation and Interest Rates**  
   Investigate how inflation influences Federal Reserve decisions on interest rate adjustments. 
   
2. **Examine the Impact of Inflation on Consumer Spending**  
   Assess whether rising inflation leads to a decline in household spending using various systems such as CPI (consumer price index).

3. **Evaluate how Inflation Affects Business Investment**  
   Determine whether inflation discourages businesses from making long-term investments as a response.

4. **Integrate and Take Other Factors in Account**  
   Since economy is very vast and does not just depend on few factors, I will compare the CPI inflation data with other factors such as wages, savings rate, and unemployment rate.

5. **Round Up and Point Out Indirect Effect To GDP**  
   Finally after plotting all the data, understand and analyze the bigger effect inflation will have in the economy, as in towards the GDP, which is biggest indicator of economic performance.

6. **Provide Data-Driven Insights for Economic Trends**  
   Use historical data to track patterns in economic recessions and expansions and use the data science concepts I have learned in DSA210 to analyze and visualize the data.
   
---

## Motivation

Inflation, interest rates, and their effects on economic growth and development have long been a topic of debate in economics, particularly between classical and neo-Keynesian economists. By analyzing real-world data, this project aims to uncover the relationships between inflation, interest rates, consumer behavior, and general economic performance by providing valuable insights into both short-term and long-term economic shifts, as well as considering other factors like wages and unemployment.

---

## Dataset

The dataset for this project consists of publicly available economic indicators that track inflation, interest rates, consumer spending, investment, etc. over time. All data will be taken from the **Federal Reserve Economic Data (FRED)**, a publicly accessible database maintained by the **Federal Reserve Bank of St. Louis** which provides accurate, up-to-date U.S. economic time series data. Here’s what I’ll be analyzing:  

- **Date:** The specific month and year for each recorded data point.

- **Recession Periods:** The specific time periods of U.S. recessions that took place that were influential in economic shifts.

- **Inflation (CPI):** Measures the percentage change in consumer prices over time.  
  *(Source: U.S. Bureau of Labor Statistics via FRED)*

- **Interest Rates (Federal Funds Rate):** The key interest rate set by the Federal Reserve to manage inflation and stabilize the economy.  
  *(Source: Board of Governors of the Federal Reserve System (US) via FRED )*

- **Consumer Spending (PCE):** Measures the total value of goods and services consumed by households, reflecting behavioral responses to inflation and rate changes.  
  *(Source: U.S. Bureau of Economic Analysis via FRED)*

- **Investment (GPDI, Gross private domestic investment):** Tracks how much businesses are spending on long-term capital assets like buildings, equipment, and intellectual property.  
  *(Source: U.S. Bureau of Economic Analysis via FRED)*

- **Savings Rate (Personal Savings Rate):** Measures the percentage of disposable income that households save instead of spend, especially during periods of uncertainty.  
  *(Source: U.S. Bureau of Economic Analysis via FRED)*

- **Wages (Average Hourly Earnings):** Captures the monthly average wage for private sector employees, used to assess purchasing power under inflation.  
  *(Source: U.S. Bureau of Economic Analysis via FRED)*
  
- **Unemployment Rate:** Measures the percentage of the labor force that is unemployed and actively seeking work; a key indicator of labor market health.  
  *(Source: U.S. Bureau of Economic Analysis via FRED)*
  
- **Gross Domestic Product (GDP):** Tracks the total value of goods and services produced in the U.S., serving as a key measure of economic growth and overall economic cycles.  
  *(Source: U.S. Bureau of Economic Analysis via FRED)*

# Final Report

## Introduction

This project investigates how inflation (CPI) influenced key U.S. economic indicators between 2006 and 2025. The main variables analyzed include interest rates, wages, consumer spending, investment, savings rate, unemployment rate, and GDP (gross domestic product) as well as taking factors such as global recessions into consideration. The United States is chosen as the subject of this project due to its wide accessibility of economic data which is unlike any other country. Using real-world economic data from the U.S. Federal Reserve, this case study explores correlations and relationships between economic variables through visualizations, statistical tests, and machine learning models.

---

## Data Analysis

### Dataset Description

Source: All data collected from U.S. Federal Reserve (FRED)

Time Range: April 2006 to October 2024 (per 3 months frequency due to GDP data)

Variables included:
- **CPI:** Consumer Price Index. A measure of inflation        (CPIAUCNS.csv)
- **Federal Funds Rate:** Interest rate set by the Federal Reserve              (FEDFUNDS.csv)
- **Average Hourly Earnings:** Wages for private employees (in dollars/hour)          (CES0500000003.csv)
- **Unemployment Rate:** Monthly civilian unemployment rate                  (UNRATE.csv)
- **Personal Savings Rate:** Percentage of disposable income saved                   (PSAVERT.csv)
- **Consumer Spending (PCE):** Personal consumption expenditures (in billion $)          (PCE.csv)
- **Investment (GPDI):**  Gross private domestic investment (in billion $)           (GPDI.csv)
- **GDP:** Real Gross Domestic Product (quarterly, in billion $)       (GDP.csv)

All datasets merged on date index.

### Methodology and Techniques Used
- **Data Preprocessing**: Merged and aligned macroeconomic datasets from FRED so that they fit in same timeline and frequency.
- **EDA**: Time-series plots showing CPI alongside other indicators, with recession zones indicated.
- **Correlation Heatmap**: Used to identify relationships between features.
- **Hypothesis Testing**: Spearman correlation and t-test.
- **Machine Learning**: Linear Regression, Random Forest, and K-Nearest Neighbors (KNN) models applied to predict CPI.

### Analysis Stages
1. Data Cleaning and Formatting  
2. Visual Trends Analysis (CPI vs each variable)  
3. Correlation Heatmap  
4. Hypothesis Testing Results  
5. Machine Learning Regression Models

---

## Findings

### EDA Graphs

- **CPI vs Federal Funds Rate**  
  - No consistent pattern observed. In some periods, interest rates rose with inflation, while in others they lagged behind.
  - The Fed’s response to inflation appears more reactive than directly proportional.

- **CPI vs Wages (Average Hourly Earnings)**  
  - Both trends show steady increases over time.
  - Wages often outpaced inflation, but monthly changes were not statistically different.

- **CPI vs Consumer Spending (PCE)**  
  - Very strong positive relationship.
  - As inflation rose, consumer spending increased consistently — expected in nominal terms.

- **CPI vs Investment (GPDI) and Personal Savings Rate**  
  - Investment followed inflation closely with sharp rises, especially during expansion periods.
  - Savings rate spiked during recessions and dropping during stable periods.
  - The relationship between inflation and savings was weak compared to investment.

- **Recession Zones**  
  - All graphs shaded the 2008 Financial Crisis and the 2020 COVID-19 Recession.
  - These periods clearly disrupted trends across all variables — especially unemployment and savings.

- **Correlation Heatmap**  
  - CPI showed strong positive correlations with PCE and GPDI.
  - CPI had a moderate negative correlation with unemployment.
  - Most variables were positively related, especially GDP and investment.

---

### Hypothesis Testing

  - Spearman correlation confirmed a significant positive relationship between CPI and both consumer spending and investment.
  - A negative correlation was found between CPI and unemployment.
  - Although wages grew faster than CPI, a t-test showed no significant difference in monthly % changes.

---

### ML Models

- **Linear Regression**  
  - Moderate performance with R² ≈ 0.40 — CPI was somewhat predictable using economic indicators.
  - Model captured trend but missed sharp fluctuations.

- **Random Forest Regression**  
  - Poor performance (negative R²). Model failed to generalize, likely due to small test size and volatile data.

- **KNN Regression**  
  - Also failed (negative R²), indicating that macroeconomic patterns are not well-suited to local-distance models like KNN.


---

##  Limitations and Future Work

### Limitations:
- Time-based split limited test size (~15 rows), causing weak model performance.
- CPI affected by complex global and local forces not captured in this dataset.
- 2008 Financial Crisis and 2020 COVID Recession severely disrupted trends and ML models causing some to fail.
- Economy, specifically inflation, is highly difficult to predict. Even central banks with economic experts get it wrong sometimes. This shows that inflation is not merely dependant on a bunch of factors like interest rate and consumer spending. Many "endogenous" factors like political dynamics and stock market performance play a role.

### Future Improvements:
- Model % changes or inflation rate instead of raw CPI.
- Try time-series algorithms (e.g. LSTM, ARIMA).
- Include oil prices, interest rate expectations, global inflation indices, fiscal policy variables, election periods and so much more.

**Note**: None of these will get us direct answers but will guide us closer to the actual CPI.

---

## Conclusion

This project confirmed many economic principles such as, CPI rises with consumer demand and investment and falls with unemployment, but also highlighted the **challenges of modeling real-world economic data**. While correlation is often strong, prediction is complex due to policy, shocks, and ,what is known between economists, "endogenous" factors. Nevertheless, this project forms a solid analytical base, with meaningful insights and opportunities for future refinement.
