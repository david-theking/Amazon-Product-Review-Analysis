# Case Study 1: Amazon-Product-Review-Analysis
This project showcases an end-to-end data analysis case study using Microsoft Excel. It explores customer reviews and product data scraped from Amazon to provide actionable business insights that can help sellers enhance their pricing strategies, product listings, and customer engagement. 

## 1. Project Overview
You are working as a Junior Data Analyst at RetailTech Insights, a company that provides e-commerce analytics solutions to sellers on platforms like Amazon. Your team has been
tasked with analysing product and customer review data to generate insights that can guide product improvement, marketing strategies, and customer engagement.

## 2. 🎯 Project Objectives
- Analyze discounts across different product categories
- Explore product rating distribution and averages
- Identify top-rated and most-reviewed products
- Examine customer engagement patterns
- Determine potential revenue by category
- Build an interactive dashboard for business users

The dataset contains aggregated information scraped from Amazon product pages. Each row represents a **unique product** and includes the following fields:

| Column Name       | Description                                                  |
|-------------------|--------------------------------------------------------------|
| Product_Name      | Name of the product                                          |
| Category          | Product category (e.g., Electronics, Fashion, etc.)          |
| Actual_Price      | Original listed price of the product                         |
| Discounted_Price  | Final price after discount                                   |
| Discount_Percent  | Percentage discount offered                                  |
| Rating            | Average product rating (e.g., 4.2)                           |
| Rating_Count      | Number of customer reviews                                   |
| Review_Title      | Aggregated review title content                              |
| Review_Content    | Aggregated review body content                               |

## 🛠 Tools and Techniques
- ✅ Microsoft Excel (Data Cleaning & Analysis)
- 📌 Pivot Tables & Pivot Charts
- ✏️ Calculated Columns (e.g., discount percentage, revenue estimates)
- 📈 Interactive Dashboards (with Slicers & Cards)
- 🧠 Analytical Thinking & Business Insight Generation

## 🔍 Analytical Approach

### 1. Data Cleaning
- Checked for missing values and inconsistencies
- Ensured correct data types for numerical and text fields
- Created calculated columns:
  - `Discount % = (Actual Price - Discounted Price) / Actual Price * 100`
  - `Potential Revenue = Actual Price * Rating Count`

### 2. Exploratory Data Analysis (EDA)
- Built pivot tables to answer business questions:
  - Average discount by category
  - Product rating distribution
  - Total reviews per category
  - Top-rated and most-reviewed products

### 3. Data Visualization
- Designed a dynamic dashboard with:
  - KPI Cards (e.g., Total Reviews, Average Rating, Revenue)
  - Bar & Column Charts (e.g., reviews by category, ratings distribution)
  - Slicers for interactivity by category and rating

## Analysis Tasks & Key Findings:
| S/N | Business Question                                                                 | Approach / Steps Taken                                                                                      | Key Insight / Output                                                                 |
|-----|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| 1   | What is the average discount percentage by product category?                      | Used Pivot Table to group by Category and averaged `Discount_Percent`                                       | Home Improvements, Computer & Accessories and Health & Personal Care had the highest average discounts                   |
| 2   | How many products are listed under each category?                                 | Pivot Table: Count of Product Names by Category                                                              | Distribution varies, with Electronics having the highest number of listings (498) closing followed by Home & Kitchen (448). Whereas Toys & Games, Cars & Motorbikes and Health & Personal Care only had one (1) product listing        |
| 3   | What is the total number of reviews per category?                                 | Pivot Table: Sum of `Rating_Count` by Category                                                               | The total number of reviews per category dramatically highlights customer engagement levels. Electronics absolutely dominates with 14.2M reviews reinforcing its position as the most popular and actively reviewed product category. Categories like Car & Motorbike, Health & Personalcare, and Toys & Games have very low review counts. This indicates very ow consumer engagements or less popular products within this category.   |
| 4   | Which products have the highest average ratings?                                  | Sorted dataset by `Rating` (descending) and filtered top-rated products                                     | Several products scored 5.0 average rating. This include "Syncwire LTG to USB, Amazon Basics Wireless Mouse and REDTECH USB-C to lighthning. This indicates strong customer satisfaction and positive product experiences for these specific items. Followed closely are the Oratech Coffee Frother Electric and Instant Pot Air Fryer wuth average ratings of 4.8  |
| 5   | What is the average actual vs discounted price by category?                       | Pivot Table with `Average of Actual Price` and `Discounted Price` per Category                              | Electronics show the largest gap between actual and discounted prices, indicating aggressive pricing—likely due to high competition or frequent product updates. High discounts on electronics suggest a competitive strategy, likely aimed at clearing stock or attracting price-sensitive buyers. |
| 6   | Which products have the highest number of reviews?                                | Sorted dataset by `Rating_Count` (descending)                                                                | Amazon Basics High-Speed HDMI leads with 850,000 reviews, followed by boAT Bassheads and Redmi 9A Sport Coral), highlighting their high customer engagement and popularity. These products likely enjoy strong visibility and sustained consumer trust on the platform  |
| 7   | How many products have a discount of 50% or more?                                 | A calculated field or helper column was created to categorize products based on whether their 'Discount (%)' was 50% or more. An Excel Pivot Table was then used to count the number of products that falls in this category  | Nearly 49% of products (662) have discounts of 50% or more, reflecting an aggressive pricing strategy to attract buyers, boost sales, or clear inventory in a competitive e-commerce space.|
| 8   | What is the distribution of product ratings?                                       | Pivot Table: Count of products grouped by `Rating` the ratings were furhter grouped in the pivot table using the order 0-1, 2-3, 3-4, 4-5 | Most products are rated between 3.5 and 4.5                                          |
| 9   | What is the total potential revenue by category?                                  | Calculated column: `Actual Price × Rating_Count`, then summed using Pivot Table per Category                | Electronics and Office Supplies had the highest potential revenue                   |
| 10  | How does the rating relate to the level of discount?                              | Created a Scatter Plot: `Discount_Percent` vs `Rating`                                                       | Weak correlation; high discounts don’t necessarily lead to higher ratings           |
| 11  | How many products have fewer than 1,000 reviews?                                  | Applied filter: `Rating_Count < 1000` and counted                                                            | Majority of products have under 1,000 reviews                                        |
| 12  | Which categories have products with the highest discounts?                        | Used Pivot Table: Max of `Discount_Percent` by Category                                                      | Electronics, Fashion, and Appliances showed the deepest discounts                   |
| 13  | Identify top 5 products in terms of rating & number of reviews combined           | Created a calculated score: `Rating × Rating_Count`, sorted to get Top 5                                     | Highlighted most impactful, high-volume products                                    |
