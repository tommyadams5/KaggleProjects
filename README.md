# Creating New S&P 500 Sectors with Kmeans

## Project Summary

The stock market is a complex system with many different types of companies. One way to make sense of the stock market is to group stocks into sectors. Sectors are groups of stocks that are similar in terms of their industry or economic activity. This can help investors to view the stock market at a macro economic level, determine which stocks are similar to others, and anticipate price moves for a given stock based on changes in its sector.

The finance industry has traditionally divided the S&P 500 stocks into 11 sectors:

- Energy: Oil and gas companies
- Materials: Mining and metals companies
- Industrials: Manufacturing companies
- Consumer Discretionary: Consumer goods companies that sell non-essential products
- Consumer Staples: Consumer goods companies that sell essential products
- Healthcare: Healthcare companies
- Financials: Banks, insurance companies, and other financial services companies
- Information Technology: Technology companies
- Communication Services: Telecom companies and media companies
- Real Estate: Real estate investment trusts and other real estate companies
- Utilities: Public utility companies

One of the main purposes for the sector groupings is to help an investor limit the price volatility of their portfolio by investing in each of the sectors. To serve this purpose, it is important that stocks within a given sector are more correlated with each other than stocks in other sectors. For example, an increase in energy demand should boost the prices of stocks in the energy sector by a similar amount, but should not necessarily affect the prices of stocks outside the energy sector in the same way. 

In this project, I will use a K-means clustering algorithm to group S&P 500 stocks into clusters based on their 5-day percentage price changes, utilizing PyTorch to implement the K-means algorithm. The goal of this project is to determine if I can come up with better sectors than the existing ones for showing which stocks are correlated with each other.
