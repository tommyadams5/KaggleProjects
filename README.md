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

In this project, I use a K-means clustering algorithm to group S&P 500 stocks into clusters based on their 5-day percentage price changes, utilizing PyTorch to implement the K-means algorithm. The goal of this project is to determine if I can come up with better sectors than the existing ones for showing which stocks are correlated with each other.

## Background

K-means clustering is a simple but effective clustering algorithm. It works by first randomly selecting k points in the data set. These points are called the centroids. The algorithm then iteratively assigns each data point to the cluster with the closest centroid. The centroids are then updated to the mean of the points in each cluster. This process is repeated until the centroids no longer move.

PyTorch is a popular deep learning framework that is used for natural language processing, computer vision, and other machine learning tasks. It is also a good choice for clustering tasks because it is fast and efficient.

## Graphs

I showed several stacked bar charts of the groupings that resulted from the Kmeans algorithm. In each bar chart, the y-axis is the number of stocks in each cluster and the x-axis is the cluster number for each cluster. The legend color labels correspond to how the finance industry has currently classified each stock into a sector.

## Results

In the first bar chart, was able to outperform the current sector groupings by generating a lower inertia with 11 clusters than the inertia of the current sector groupings. This means that my clustering algorithm was able to group the stocks more effectively than the traditional sector groupings.

After examining the results, I noticed that there were multiple clusters that were quite small. This implied that a smaller number of clusters might be a better fit.

I then ran more iterations with 7 clusters and found a result that still had less inertia than the current sectors despite having 4 less groups. This is a significant improvement, and suggests that the clustering algorithm is able to identify meaningful patterns in the data that the traditional sector groupings do not.

I also looked at the 9 iteration groupings with the lowest inertias. From the bar charts of their groupings, I made the following observations:

-  The energy sector is consistently its own group, showing that energy stocks tend to be some of the least correlated stocks to the rest of the market and that this current sector grouping is justified.
-  Utilities and real estate industries tend to be grouped together; this makes sense because both sectors have large assets that produce consistent dividends.
-  In a majority of the 9 iterations, consumer staples is also in the same group as utilities and real estate. This makes sense because all three of these sectors are somewhat conservative investments in that they produce reliable cash flows but do not have much potential for large gains.
-  The industrial and material sectors are often grouped together, probably because the demand for industrial goods also affects the demand for the raw materials that the industrial companies use.
-  In half of the 9 iterations, there is a large chunk of financials that is also grouped with the industrial and material sectors. My guess is that this occurs because these are all somewhat cyclical sectors that are tied to the business cycle; when the economy is expanding, there is an increasing demand for goods which leads to expansions in industrials, materials, and financing.
-  The rest of the sectors (information technology, health care, consumer discretionary, communication services) tend to be more dispersed across the groupings, implying that these sectors are more diverse and that the stocks in these sectors are not as strongly correlated with each other.
-  In particular, consumer discretionary and communication services are consistently dispersed across several groups, implying that these sectors should be removed or reworked to identify a group of stocks that are more correlated with each other.

In conclusion, I was able to generate stock groupings that better reflected price movement than the existing sectors defined by the finance industry. My recommendation for improving the existing sectors is to rework the consumer discretionary and communication services sectors and possibly the health care and information technology sectors.



