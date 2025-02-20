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

With the data cleaning stage done and the dataset ready for visualization, Power BI was used to actualize that. The visuals are presented in 5 dashboards for a clearer presentation of the report. The first is an overview of all data in the dataset, comparing stock behaviours in relation to various metrics across the 4 countries under review. The rest consider each country individually. (Click Here)[https://app.powerbi.com/view?r=eyJrIjoiZDU2M2JhYmYtOTAwMC00ZDFiLThiOGMtZTg0ZjNhZGUxMzhkIiwidCI6ImRmODY3OWNkLWE4MGUtNDVkOC05OWFjLWM4M2VkN2ZmOTVhMCJ9] to access the interactive Power BI dashboards, and check out the visuals in the 5 pages. Navigation on the design is made easy by some integrated features. 

### **Key Features on the Dasboards**

- **Dropdown Slicers:** "Category" and "Best for wear" are dynamic and particular metrics can be reviewed by selecting from the Slicer's dropdown menu for both.
- **Country Flag Buttons:** Click on any of the 4 buttons to navigate to the particular Country page represented by the flag.
- **Reset Button:** This is present on all 5 pages, and resets the page to default view after Slicers or other selections have been used to review results.
- **Overview Button:** This is present on individual country pages, and takes you back to the Overview page when clicked.
- **Sizes Buttons:** Displays available data for any shoe sizes selected. This is equally available on all pages.
