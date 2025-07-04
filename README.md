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
| 1   | What is the average discount percentage by product category?                      | Used an Excel Pivot Table. 'Product Category' was placed in the Rows area, and 'Discount (%)' was placed in the Values area, set to show the 'Average'. | Home Improvements, Computer & Accessories and Health & Personal Care had the highest average discounts                   |
| 2   | How many products are listed under each category?                                 | Used Excel Pivot Table. 'Product Category' was placed in the Rows area, and 'product_name' was placed in the Values area, set to show the 'Count'.  | Distribution varies, with Electronics having the highest number of listings (498) closing followed by Home & Kitchen (448). Whereas Toys & Games, Cars & Motorbikes and Health & Personal Care only had one (1) product listing        |
| 3   | What is the total number of reviews per category?                                 | Used an Excel Pivot Table. 'Product Category' was placed in the Rows area, and 'rating_count' was placed in the Values area, set to show the 'Sum'.   | The total number of reviews per category dramatically highlights customer engagement levels. Electronics absolutely dominates with 14.2M reviews reinforcing its position as the most popular and actively reviewed product category. Categories like Car & Motorbike, Health & Personalcare, and Toys & Games have very low review counts. This indicates very ow consumer engagements or less popular products within this category.   |
| 4   | Which products have the highest average ratings?                                  | Used an Excel Pivot Table. 'product_name' was placed in the Rows area, and 'rating' was placed in the Values area, set to show the 'Average'. The results were then sorted in descending order by 'Average of rating'. | Several products scored 5.0 average rating. This include "Syncwire LTG to USB, Amazon Basics Wireless Mouse and REDTECH USB-C to lighthning. This indicates strong customer satisfaction and positive product experiences for these specific items. Followed closely are the Oratech Coffee Frother Electric and Instant Pot Air Fryer wuth average ratings of 4.8  |
| 5   | What is the average actual vs discounted price by category?                       | Used an Excel Pivot Table with `Average of Actual Price` and `Discounted Price` per Category                              | Electronics show the largest gap between actual and discounted prices, indicating aggressive pricing—likely due to high competition or frequent product updates. High discounts on electronics suggest a competitive strategy, likely aimed at clearing stock or attracting price-sensitive buyers. |
| 6   | Which products have the highest number of reviews?                                | Used an Excel Pivot Table. 'product_name' was placed in the Rows area, and 'rating_count' was placed in the Values area, set to show the 'Sum'. The results were then sorted in descending order by 'Sum of rating_count'.   | Amazon Basics High-Speed HDMI leads with 850,000 reviews, followed by boAT Bassheads and Redmi 9A Sport Coral), highlighting their high customer engagement and popularity. These products likely enjoy strong visibility and sustained consumer trust on the platform  |
| 7   | How many products have a discount of 50% or more?                                 | A calculated field or helper column was created to categorize products based on whether their 'Discount (%)' was 50% or more. An Excel Pivot Table was then used to count the number of products that falls in this category  | Nearly 49% of products (662) have discounts of 50% or more, reflecting an aggressive pricing strategy to attract buyers, boost sales, or clear inventory in a competitive e-commerce space.|
| 8   | What is the distribution of product ratings?                                       | Used Pivot Table: Count of products grouped by `Rating` the ratings were furhter grouped in the pivot table using the order 0-1, 2-3, 3-4, 4-5 | Most products are rated between 3.5 and 4.5          |
| 9   | What is the total potential revenue by category?                               | Calculated column: `Actual Price × Rating_Count`, then summed using Pivot Table per Category                |  The total potential revenue by category reveals immense market opportunities, particularly dominated by Electronics with an astounding ₹91,323.9 billion. Other categories, while much smaller in comparison, still represent substantial markets (e.g., "Musicalinstruments" with ₹151 million, "Officeproducts" with ₹60 million).  |
| 10   | What is the number of unique products per price range bucket (e.g., <₹200, ₹200–₹500, >₹500)?   | A calculated column named was calculated 'Price Bucket' was created based on the `Actual Price` to categorize products into '< ₹200', '₹200-₹500', and '> ₹500'. ` Then, an Excel Pivot Table was used with 'Price Bucket' in the Rows area and 'product_name' was placed in the Values area, set to show the 'Count'. |  The distribution of unique products across price ranges reveals a clear focus on higher-priced items. A dominant majority of products, 850 out of 1351 products fall into the "> ₹500" price bucket. Products in the "₹200-₹500" range are fewer (342 products), and there are very few products in the "< ₹200" range (only 153 products) |
| 11  | How does the rating relate to the level of discount?                              | First, a calculated field or helper column was created to categorize products into specific discount ranges ('0-10%', '11-20%', '20–30%', etc). Then, an Excel Pivot Table was used with these 'Discount Range' categories in the Rows area and 'rating' was placed in the Values area, set to show the 'Average'.  | Interestingly, products with the lowest discount range (0-10%, 21-30%) have the highest average rating (4.2). Products with 90-100% discount however had slightly high rating of 4.22. This indicates that high discounts don’t necessarily lead to higher ratings    |
| 12  | How many products have fewer than 1,000 reviews?                                  | An Excel Pivot Table was then used with the 'Ratings Count' in the Rows area and 'product_name' was placed in the Values area, set to show the 'Count'. The 'Ratings Count' were then grouped using the order (0-999 and >1000)| The analysis reveals that 310 products have fewer than 1,000 reviews. These low-review products present an opportunity for targeted marketing, review generation campaigns, or re-evaluation of their product-market fit. |
| 13  | Which categories have products with the highest discounts?                        | Used Pivot Table: Max of `Discount_Percent` by Category                                                      | The analysis showed that Computer & Accessories had the highest discounts (94%) followed closely by electronics and Home & Kitchen with 91% & 90% respectively. This indicates these are highly competitive categories where sellers frequently employ aggressive pricing strategies to attract customers or manage inventory. |
| 14  | Identify top 5 products in terms of rating & number of reviews combined           | A new calculated column named 'Combined Score' was created to evaluate products based on both their 'rating' and 'rating_count'. An Excel Pivot Table was then used with 'product_name' in the Rows area and 'Sum of Combined Score' in the Values area, sorted in descending order to identify the top 5. | The top 5 products that excel in both customer satisfaction (rating) and popularity (review count) are: **Amazon Basic High Speed HDMI**, **boAT Bassheads 100 in**, **Redmi 9A Sports (Coral)**, **Amazon Basics Flexible Premium HDMI** and **JBL C**. **Amazon Basic High Speed HDMI** stands out significantly with the highest combined score, reinforcing its position as a highly popular and well-regarded product. These products are invaluable assets for RetailTech Insights' clients. They represent flagship items that drive sales, build brand reputation, and foster customer loyalty due to their combination of high quality (high rating) high review count. Management should focus on maintaining the success of these products through continued quality assurance, active community engagement, and leveraging their popularity in marketing strategies  |



## 📊 Dashboard Preview

> The final dashboard includes slicers, interactive filters, KPI cards, and charts that allow business managers to explore product performance by category, rating, and discount level.

## Dashboards
![Dashboard](https://github.com/david-theking/Amazon-Product-Review-Analysis/blob/main/Dashboard%201.png)
![Dashboard](https://github.com/david-theking/Amazon-Product-Review-Analysis/blob/main/Dashboard%202.png)
![Pivot](https://github.com/david-theking/Amazon-Product-Review-Analysis/blob/main/Pivot.png)


# Recommendations

### 1. Leverage Core Categories:
- Invest Heavily in Electronics, Computers & Accessories and Home & Kitchen: Given their market dominance in products, reviews, and potential revenue, prioritize inventory, marketing, and new product development within these categories.
- Analyze High-Rated Products: Study the attributes, marketing, and customer service strategies behind consistently high-rated products to replicate their success across other listings.

### 2. Enhance Product Visibility & Customer Engagement:
- Review Generation Campaigns: Implement targeted campaigns for the 310 products with fewer than 1,000 reviews to boost their visibility and gather valuable customer feedback. This could include post-purchase email sequences, incentivized reviews, or improved product descriptions.

### 3. Continuous Monitoring & Adaptation:
- Regularly monitor key performance indicators (KPIs) related to sales, customer segments, shipping costs, and returns to ensure ongoing strategic alignment and identify new opportunities or challenges.

