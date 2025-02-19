# Adidas-Webstore-Shoe-Data-Analysis

**OBJECTIVE:**

To assess the performance of Adidas footwear and optimize resource allocation for maximum profitability, the Adidas Global Sales Director has requested an analysis of stock levels across various shoe categories in the USA, UK, Germany, and Belgium. This analysis, based on a 12-day dataset, will provide insights into inventory distribution and sales potential in these key markets.


**DATA DESCRIPTION AND COLLECTION:**

The data is sourced from Kaggle. [Click here to access it.](https://www.kaggle.com/datasets/tamsnd/adidas-webstore-shoe-data)
The dataset is presented in 3 CSV files: country_dim.csv, shoes_dim.csv, and shoes_fact.csv, and contains around 3400 shoe's data with daily updates.

The dataset, sourced from Kaggle, required extensive cleaning and exploratory analysis to understand its structure and refine it for effective use in this project.

**DATA EXPLORATION AND CLEANING**

During our initial exploration of the dataset, we observed that some columns contained values in inconsistent formats, which required standardization to ensure accurate analysis. Notable issues included:  

- **Size Column (shoes_fact.csv):** Shoe sizes were recorded in varying formats across regions.  
  - In the USA, sizes included 'M' or 'W' to indicate Men's and Women's shoes, respectively.  
  - Some UK sizes had a 'K' suffix, representing Kids' sizes.  
  - German and Belgian (EU) sizes were purely numerical, with some including fractions (e.g., 10 1/2).  

- **Price Column:** Regardless of the country (USA, UK, Germany, or Belgium), all prices were recorded in Euros (€), requiring currency adjustments for region-specific analysis.  

- **Irrelevant Data:** The dataset contained more columns than necessary for our analysis, making it essential to remove redundant fields from the three tables to streamline insights.  

Addressing these inconsistencies was crucial for ensuring data accuracy and reliability in our findings.

Because the dataset is not ready for our use in its raw state
