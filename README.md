# Project Background
Dataset obtained from a consumer retail business which, during the year, recorded 64,682 transactions, including 5,242 products (SKUs) sold to 22,625 customers.

Despite having a large amount of data on customer shopping behavior, exploiting this data to optimize business strategies has not been done comprehensively. Therefore, the main goal of this project is to apply Customer Segmentation using the K-means Clustering algorithm, aiming to:

- **Understand potential customer groups**, helping to **personalize marketing strategies.**
- **Improve the effectiveness of promotional programs** through analyzing the characteristics of each group.
- **Support optimizing inventory management**, based on spending patterns and shopping frequency.

#### Key Analytical Approaches
The project will use two approaches to cluster customers and evaluate the effectiveness of each:

- K-means clustering on the entire dataset, including all detailed transactions.
- K-means clustering based on the **RFM (Recency, Frequency, Monetary)** model, a popular method in customer behavior analysis.
**Silhouette Score and Calinski-Harabasz Index** will be used to measure the quality of clusters, helping to determine the most optimal method.

# Dataset Structure

Dataset provided detailed information about quantities, characteristics and values of goods sold as well as their prices.
![image](https://github.com/user-attachments/assets/d44748ef-4d78-48f9-a964-36110642f9be)

The data is organized into 8 columns, each representing key attributes of retail store transactions and could be used contains enough information to perform RFM then segment customers.
Prior to beginning the analysis, a variety of checks were conducted for quality control and familiarization with the datasets. The Pyspark codes utilized to inspect and perform quality checks can be found [here].

# Executive Summary
Using Excel for better data visualization, after using K-means clustering to figure out the right amount of group customers, there are four segmentation: **Potential Loyalists, Lost Customers, Loyal Customers and Champions.**
![image](https://github.com/user-attachments/assets/e29ff25d-794d-4e25-b491-2c51cf6159f5)

