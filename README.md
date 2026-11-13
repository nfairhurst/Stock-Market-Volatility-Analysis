# Stock Market Volatility Analysis

## Project Overview

Our group is looking at whether stock prices fluctuate more on certain weekdays and whether those patterns differ across the 11 S&P 500 sectors. We'll use multiple linear regression to study historical data and see how well our model predicts results for 2025.

## Dataset

**Source:** [S&P 500 Stocks: 25 Years of Data (Updated Daily)](https://www.kaggle.com/datasets/darkmatternet/s-and-p-500-stocks-25-years-of-data-updated-daily)

The dataset has approximately **2.96 million daily stock records** from **2000–2026**, covering **503 companies** and **11 sectors**.

- `sp500_stocks.csv` — Daily stock prices and trading volume
- `sp500_companies.csv` — Company information and sector classifications

We'll keep the original files separate from our cleaned data.

## Measuring Volatility

We'll measure daily price fluctuations using the following formula:

**Daily Price Range (%)**

```math
\frac{H-L}{O} \times 100
```

Where:
- **H** = Highest daily price
- **L** = Lowest daily price
- **O** = Opening price

## Our Plan

1. **Clean the data:** Check for missing values, duplicates, invalid prices, and possible outliers. Match stocks to their sectors and identify each date's weekday and year.

2. **Prepare the data:** Calculate the daily price range for each stock, then average the results by **sector, weekday, and year**. We'll also calculate the previous year's average trading volume.

3. **Run the regression:** Use **weekday, sector, year, and previous-year trading volume** to explain average daily price range. We'll include weekday × sector interactions to see whether weekday patterns differ across sectors.

4. **Test the model:** Fit the regression using **2001–2024** (using 2000 to calculate the first year's lagged volume). We expect around **1,320 grouped observations**. Then we'll predict the **2025** values and compare them with the actual results.

We'll use graphs and summary statistics to explore the data, and a joint F-test to check whether the weekday × sector interactions are statistically significant.

## Team Responsibilities

- **Nathan Fairhurst:** Data cleaning, GitHub, and Streamlit
- **Dave Thomas:** R programming
- **Aleksandre Japaridze:** Python programming

