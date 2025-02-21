# Adidas-Webstore-Shoe-Data-Analysis

**OBJECTIVE:**

To assess the performance of Adidas webstore shoe data and optimize resource allocation for maximum profitability, the Adidas Global Sales Director has requested an analysis of stock levels across various shoe categories in the USA, UK, Germany, and Belgium. This report analyzes Adidas' webstore shoe data for the USA, UK, Germany, and Belgium over a 12-day period. The objective is to assess stock levels, pricing trends, and inventory distribution to optimize resource allocation and maximize profitability. The analysis provides insights into the availability of different shoe categories, pricing variations, and country-specific trends.


**DATA DESCRIPTION AND COLLECTION:**

The data is sourced from Kaggle. [Click here to access it.](https://www.kaggle.com/datasets/tamsnd/adidas-webstore-shoe-data)
The dataset is presented in 3 CSV files: country_dim.csv, shoes_dim.csv, and shoes_fact.csv, and contains around 3400 shoe's data with daily updates.

The dataset, sourced from Kaggle, required extensive cleaning and exploratory analysis to understand its structure and refine it for effective use in this project.

**DATA EXPLORATION AND CLEANING**

During our initial exploration of the dataset, we observed that some columns contained values in inconsistent formats, which required standardization to ensure accurate analysis. Notable issues included:  

- **Size Column (shoes_fact.csv):** Shoe sizes were recorded in varying formats across regions.  
  - In the USA, sizes included 'M' or 'W' to indicate Men's and Women's shoes, respectively.  
  - Some UK and USA sizes had a 'K' suffix, representing Kids' sizes.  
  - German and Belgian (EU) sizes were purely numerical, with no distinction between men and women, and some including fractions (e.g., 10 1/2).  

- **Price Column:** Regardless of the country (USA, UK, Germany, or Belgium), all prices were recorded in Euros (€), requiring currency adjustments for region-specific analysis.  

- **Irrelevant Data:** The dataset contained more columns than necessary for our analysis, making it essential to remove redundant fields from the three tables to streamline insights.  

Addressing these inconsistencies was crucial for ensuring data accuracy and reliability in our findings.

Since the datasets were not immediately suitable for analysis in their raw state, we performed extensive data cleaning to refine them for our purpose. The goal was to structure the data effectively, ensuring it was accurate, consistent, and ready for analysis.  

The cleaned dataset needed to meet the following criteria and constraints:  

- **Retention of Relevant Columns:** Only necessary columns were kept to streamline the analysis.  
- **Appropriate Data Types:** Each column's data type was standardized to accurately represent its contents.  
- **Completeness:** No column contained null values, ensuring that all records were fully populated.

### **Key Data Cleaning Steps:**  

To standardize the dataset and ensure consistency, the following transformations were applied:  

- **Created a New "Section" Column:** Categorized shoe sizes into "Adults" and "Kids" for clarity.  
- **USA Sizes:** Filtered entries with 'M' or 'W' in the "Size" column and classified them as **"Adults"**.  
- **UK Sizes:** Identified sizes with 'K' (Kids) and labeled them as **"Kids"**, while all other UK sizes were assigned to **"Adults"**.  
- **EU Sizes (Germany & Belgium):**  
  - Researched standard EU size ranges for kids using Google search.  
  - Selected corresponding sizes and categorized them under **"Kids"** in the "Section" column.  
  - Assigned all remaining EU sizes to **"Adults"**.  

These steps ensured uniformity in size classification across different regions, making the data more structured and ready for analysis.

These refinements were essential to enhance data quality and facilitate meaningful insights.

### **ANALYSIS AND VISUALIZATION USING POWER BI**

With the data cleaning stage completed and the dataset prepared for visualization, Power BI was utilized to create interactive and insightful dashboards. The report is organized into five distinct dashboards to ensure a clear and comprehensive presentation of the findings.

The first dashboard provides an overview of the entire dataset, highlighting stock behaviors in relation to various metrics across the four countries under review. The remaining four dashboards focus on individual country analyses, offering a detailed breakdown of trends and insights for each location.

To explore the interactive Power BI dashboards, [Click Here](https://app.powerbi.com/view?r=eyJrIjoiZDU2M2JhYmYtOTAwMC00ZDFiLThiOGMtZTg0ZjNhZGUxMzhkIiwidCI6ImRmODY3OWNkLWE4MGUtNDVkOC05OWFjLWM4M2VkN2ZmOTVhMCJ9). The visuals are spread across five pages, and the design incorporates user-friendly navigation features for seamless exploration.

### **Key Features on the Dasboards**

- **Dropdown Slicers:** "Category" and "Best for wear" are dynamic and particular metrics can be reviewed by selecting from the Slicer's dropdown menu for both.
- **Country Flag Buttons:** Click on any of the 4 buttons to navigate to the particular Country page represented by the flag.
- **Reset Button:** This is present on all 5 pages, and resets the page to default view after Slicers or other selections have been used to review results.
- **Overview Button:** This is present on individual country pages, and takes you back to the Overview page when clicked.
- **Sizes Buttons:** Displays available data for any shoe sizes selected. This is equally available on all pages.

![Overview Dashboard](https://github.com/user-attachments/assets/b53180c9-46ee-4658-898a-b3d09e9a191b)

### **Key Findings**

**Overall Stock and Pricing Overview**
  
  - **Total Stock:** 299K shoes across all regions.
  - **Units Available:** 2 million shoes.
  - **Average Price:** €99.72.
  - **Total Number of Categories:** 17.

**Stock Availability & Pricing by Gender**

- **Men:** 139K units available (€110.47 average price).
- **Women:** 432K units available (€107.90 average price).
- **Kids:** 427K units available (€45.83 average price).
- **Unisex:** 758K units available (€121.80 average price).

**Stock Availability & Pricing by Country**

- **Germany:** 1.17M units available (€95.99 average price).
- **USA:** 0.39M units available (€119.12 average price).
- **Belgium:** 0.16M units available (€95.37 average price).
- **UK:** 0.04M units available (€63.58 average price).

**Top-Selling Shoes by Price**

- **Adizero Prime X 2.0 STRUNG Laufschuh** - €175,350.
- **Adizero Adios Pro Evo 1** - €110,000.
- **Adizero Boston 12 Laufschuh** - €104,720.

**Daily Stock Trends**

- Stock levels fluctuated significantly, with peaks on specific days (e.g., Jan 7 and Jan 9 showing the highest availability).

- The UK and Belgium had the lowest stock levels compared to other regions.

**Stock and Pricing by Dominant Color**

- Popular colors include "Aurora Black," "Core Black," and "Cloud White."

- Certain colors had significantly higher stock levels, indicating inventory concentration in specific designs.

**Results Interpretation**

1. **High Inventory Concentration in Germany:** Germany has the highest stock levels (1.17M units), indicating a strong supply chain presence or slower sales compared to other regions.

2. **USA Has the Highest Average Price (€119.12):** This suggests a premium pricing strategy or higher demand in the US market.

3. **Kids’ Shoes Have the Lowest Average Price (€45.83):** This aligns with market expectations but could indicate an opportunity for premium kids' offerings.

4. **UK Has the Lowest Stock Levels (40K units):** The UK webstore has significantly lower inventory, suggesting a limited market or supply chain constraints.

5. **Pricing and Stock Disparities Across Regions:** Belgium and Germany have similar pricing structures, while the US commands a higher average price.


### **Recommendations**

1. **Optimize Stock Allocation:**

- Reduce excess inventory in Germany and reallocate stock to the UK, where availability is lower.

- Increase stock for high-demand shoe categories and colors.

2. **Adjust Pricing Strategy:**

- Consider localized pricing adjustments to maximize revenue in high-demand regions.

- Evaluate promotional strategies for kids' shoes to increase profitability.

3. **Monitor Sales Trends and Replenish Efficiently:**

- Track daily stock fluctuations to improve demand forecasting.

- Implement data-driven restocking strategies to minimize overstock and shortages.

4. **Expand UK and Belgium Offerings:**

- The low stock in the UK suggests either high demand or supply limitations. Expanding stock levels and marketing efforts could drive sales.

- Evaluate demand trends in Belgium to determine whether stock increases are justified.


### **Final Note**

This analysis highlights key insights into Adidas' online shoe inventory, pricing trends, and stock distribution. By optimizing stock allocation, refining pricing strategies, and closely monitoring demand trends, Adidas can enhance profitability and improve customer satisfaction across its webstores in the USA, UK, Germany, and Belgium.
