# Customer Satisfaction Analysis on E-commerce Data

## Project Objective
The objective of this project is to perform an in-depth analysis of customer satisfaction within the context of shipping times and product reviews in the e-commerce sector. The goal is to uncover the relationships between product characteristics (such as volume, weight, and density) and shipping times, assess the impact of shipping performance on customer satisfaction, and identify product categories that experience the most shipping issues.

## Table of Contents
- [Project Objective](#project-objective)
- [Dataset Description](#dataset-description)
- [Project Breakdown](#project-breakdown)
  - [Section 1: Data Loading](#section-1-data-loading)
  - [Section 2: Data Pre-processing](#section-2-data-pre-processing)
  - [Section 3: Exploratory Data Analysis & Data Visualization](#section-3-exploratory-data-analysis--data-visualization)
- [Insights & Reporting](#section-4-insights--reporting)
  - [Key Findings](#1-key-findings)
  - [Recommendations](#2-recommendations)
  - [Conclusion](#3-conclusion)
- [Technologies Used](#technologies-used)
- [Acknowledgements & Dataset Source](#acknowledgements--dataset-source)

## Dataset Description
This dataset contains e-commerce order information from Olist, the largest department store on Brazilian marketplaces. It includes data on 100,000 orders made between 2016 and 2018 across various marketplaces in Brazil. The dataset features allow for analyzing an order from multiple dimensions, including order status, price, payment and freight performance, customer location, geolocation information, product attributes, and customer reviews.

This is real commercial data released by Olist through Kaggle (a web-based platform for data science containing thousands of datasets for public use). The dataset has been anonymized for privacy purposes.

## Project Breakdown

### Section 1: Data Loading
*Details on data loading within project file.*

### Section 2: Data Pre-processing
The following actions were taken to pre-process the dataset:
1. Dropped irrelevant or redundant columns.
2. Removed duplicate rows.
3. Filled null values in numerical datatype columns with the median.
4. Removed rows with null values that could not be replaced, such as *order_delivered_customer_date*.
5. Renamed columns to more suitable naming conventions.
6. Optimized column datatypes for analysis.
7. Created custom columns.

### Section 3: Exploratory Data Analysis & Data Visualization
The primary questions addressed include:
1. **Do product attributes (weight, dimensions) influence shipping time?**
   - This insight helps ascertain whether heavier or bulkier items might have more complicated shipping and handling, potentially leading to increased shipping times.
2. **Does shipping time affect product reviews?**
   - This insight assesses whether longer shipping times correlate with lower customer satisfaction.
3. **What product category has the most shipping issues?**
   - This insight highlights impacts on product quality perceptions due to external factors like shipping and handling delays, even if the product itself meets customer expectations.

## Section 4: Insights & Reporting

### 1. Key Findings

#### 1.1 Do Product Attributes Influence Shipping Time?
- **Product Volume:**
  - Products were divided into quintiles based on their volume, ranging from the smallest (under 2,450 cm³) to the largest (over 22,050 cm³). The analysis showed that products in the largest volume bin took an average of 11 days to deliver, while those in the lowest volume quintile averaged only 9 days.
  - This indicates that bulkier items are likely to encounter more logistical challenges, contributing to longer delivery times.
- **Product Weight:**
  - The analysis revealed that heavier items (over 2,450 grams) experienced an average shipping time of 11 days, whereas lighter products (under 500 grams) averaged 9 days.
  - This trend suggests that heavier items may require additional handling or specialized shipping services, leading to delays.
- **Product Density:**
  - Items with higher density (over 57 SI units) showed a slight increase in shipping times (an average of 10 days) compared to items with lower density (under 57 SI units, averaging 9 days). The impact of density on shipping time was less pronounced than that of volume and weight.

#### 1.2 Does Shipping Time Influence Product Reviews?
- **Correlation Between Shipping Time and Review Score:**
  - Orders with a review score of 5 were, on average, delivered within 8 or 9 days, while those with low review scores (3 or less) were, on average, delivered between 10 to 12 days. This negative correlation suggests that longer shipping times are associated with lower customer satisfaction.
  - When shipping times equal or exceed 13 days, nearly 18% of reviews were low (1 star), highlighting the importance of timely deliveries in maintaining high review scores.

#### 1.3 What Product Categories Have the Most Shipping Issues?
- **Late Deliveries by Product Category:**
  - The *Bed, Bath, & Table* product category accounted for the highest number of late deliveries, with approximately 800 late deliveries. This category experienced delays in about 7% of their orders, accounting for approximately 11% of all late deliveries. This pattern suggests that the larger or more complex items in this category tend to face more logistical challenges.
- **Low Review Scores by Product Category:**
  - The category with the most low review scores (1 or 2) was the *Bed, Bath, & Table* product group, indicating potential quality issues or dissatisfaction due to their history of shipping delays.

### 2. Recommendations
- **Focus on Improving Logistics for Bulky and Heavy Items:**
  - Given the longer shipping times for large and heavy products, consider partnering with logistics providers who specialize in handling these items. Reducing delays could help improve customer satisfaction in these categories.
- **Improve Shipping Time for High-Impact Categories:**
  - Prioritize faster shipping for large furniture to minimize delays and enhance the customer experience.
- **Use Incentives to Boost Positive Reviews:**
  - Encourage customers to leave reviews for items delivered on time. This could help counteract the impact of negative reviews associated with delayed orders.

### 3. Conclusion
This analysis highlights the significant role that shipping time plays in customer satisfaction. Items that are larger, heavier, or belong to certain categories (such as Bed, Bath & Table) are more prone to shipping issues. Addressing these areas can enhance customer experiences, boost review scores, and drive repeat business.

## Technologies Used
- **Python** (Pandas, NumPy, Matplotlib, Seaborn)
- **Jupyter Notebook** for data analysis and visualization
- **Kaggle** for dataset access

## Acknowledgements & Dataset Source
- [Olist](https://www.olist.com) for providing the dataset through Kaggle.
- [Link to dataset](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce/data)
