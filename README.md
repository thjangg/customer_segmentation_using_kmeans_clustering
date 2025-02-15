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

### Overview of Findings

Through the analysis of customer purchasing behavior over the past year applying K-means clustering, I have identified four key customer segments: **Potential Loyalists, Lost Customers, Loyal Customers, and Champions**.

**The Champions and Loyal Customers** groups are the **most valuable** to the business, with high purchase frequency and monetary value, making them the primary targets for retention strategies. Interestingly, the **Lost Customers** segment ranks second in total revenue despite having the highest recency, indicating a significant opportunity for re-engagement. 

**The Sales and Marketing team**, in collaboration with the **Data team**, should develop targeted campaigns to win back these high-spending customers, despite the challenge of their large segment size.

Excel Visualization file can be found [here]

![image](https://github.com/user-attachments/assets/34e9421f-d2d3-4020-b81d-3f819d05e538)

# Insights Deep Dive

### Insight 1: Understanding purchasing behavior of the two most important customer groups - Champions and Loyal Customers

![image](https://github.com/user-attachments/assets/d53fcfa5-d409-40a9-bd85-018334d45d5e)

**Champions** maintain very low recency values (R = 3-8) throughout the year indicating their **highly engagement  with very recent purchases**.
Moreover there were no major fluctuations, meaning they have a **consistent shopping pattern**. On the other hand, the drop of Frequency  in March (F = 48) suggests seasonal fluctuations after the holiday peak. Afterwards, frequency stabilizes at ~48 purchases per month. Interesting Observation here is, in March, **Champions witnessed a growing Recency and lower Frequency**, suggesting that there maybe the cause of **Post-Holiday Fatigue or Seasonal Demand Shift.** It happened due to high purchasing behavior from the last period (Christmas, New Year Promotions) so customers were taking a break from shopping

**Loyal Customers** have **significantly higher recency values**(R = 10-92), peaking in Feb (R = 92). In February, many Loyal Customers had been inactive for a long time. Afterwards, recency significantly decreases, **a sharp drop from 92** (Feb) to 10 (Dec) suggests **successful re-engagement strategies** toward the end of the year.	A bit different from Champions Group, Loyals customers witnessed both decresing trend of Frequency and Recency in March. Business got more Loyals customers starting to buy products again but with a slightly lower frequency

With the **top 5 best-selling categories** of Champions and Loyal Customers, business will be e**asier to suggest products based on customers' preferences:**

![image](https://github.com/user-attachments/assets/75777d2b-0347-4a47-9a50-c2bf8fa6219a)



### Insight 2: The mystery behind Lost Customers' Sales Amount

![image](https://github.com/user-attachments/assets/1db7a146-ce31-425c-81cb-dce6363e1f23)



### Insight 3: Potential Loyalist can be missed!

As provided in the Executive Summary, **Potential Loyalists** took up to about **50% of all customers**, also **brought back the highest revenue** for the business. However, their Frequency and Monetary were not the highest which makes them our Potential Loyal Customers. Our goal is to **encourage frequent purchases and transition these customers to Loyal or Champions.**





# Recommendations - Strategic Growth Plan for Key Customer Segments

Based on the insights and findings above, we would recommend the business could focus in each customers with different actions as follow:


 **1. Champions: Keep Them Engaged & Spending More** 
While these are our most valuable customers—they purchase frequently and consistently; moreover, in March, we saw a slight drop in frequency, likely due to post-holiday fatigue. My suggested business strategy will be: 

- **VIP Exclusive Access:** Give them early access to new products and premium experiences.
- **Subscription Model:** Offer them a convenient way to purchase regularly with subscription-based discounts.
- **Personalized Bundles & Upselling:** Encourage them to spend more per order by offering tailored product bundles.

With the expected impact:<br/>
✔️ **Higher retention & stronger loyalty** from our best customers.<br/>
✔️ **Increased AOV** through premium pricing & subscriptions.<br/>
✔️ **Stable frequency** throughout the year, reducing seasonal fluctuations.



**2. Loyal Customers: Keep Them Coming Back More Often**

They stopped buying in early Q1 but re-engaged towards the end of the year—a clear success story. However, in March, their frequency dropped, meaning they need an extra push to stay engaged as: 

- **Tiered Loyalty Rewards:** Reward for repeat purchases—the more they buy, the bigger the perks
- **Personalized Upselling**: Using past purchase behavior to recommend premium add-ons.
    
With the expected impact:<br/>
✔️ **Increased frequency**—we keep them engaged year-round, not just seasonally.<br/>
✔️ **Higher customer lifetime value** (CLV)—they spend more over time.<br/>
✔️ **Stronger brand attachment**, making them resistant to competitors.



**3. Lost Customers: Win Them Back & Boost Order Value**

They represent a massive untapped revenue opportunity—they’ve spent with us before, but they stopped coming back.
The good new is Recency is decreasing, meaning some are already returning. However, their order values and frequency remain low, meaning they need an extra incentive to stay.

- **We Miss You! Campaigns:** Email with exclusive discounts and personalized incentives.
- **Flash Sales for Returning Customers**
- **Easy One-Click Reordering:** Remove friction—make it super simple for them to buy again.
  
With the expected impact:<br/>
✔️ **Higher reactivation rates**<br/>
✔️ **Unlock new revenue streams** from customers we previously considered “lost.”



**4. Potential Loyalists: Convert Them Into Our Next Champions**

Their AOV is high, meaning they have the potential to be high-value customers but they don’t buy frequently enough.
- **Exclusive Subscription Discounts:** Lock them in with subscription-based perks—"Buy Monthly, Save Big!"
- **Bundling & Cross-Selling:** If they love a product, offer them complementary products at a discount.

With the expected impact:<br/>
✔️ Turn casual buyers into committed, high-value customers.<br/>
✔️**Increase frequency** by reducing time between purchases.<br/>





