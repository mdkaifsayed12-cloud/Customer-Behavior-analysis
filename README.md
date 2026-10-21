# Customer Shopping Behavior Analysis

An end-to-end data analysis project on 3,900 retail purchases. It uses **Python** for cleaning and EDA, **PostgreSQL** for business analysis, and **Power BI** for an interactive dashboard.

## Project Overview

The goal is to understand spending patterns, customer segments, product preferences and subscription behavior, and to turn those findings into business recommendations.

## Dataset

- 3,900 rows and 18 columns
- Demographics: age, gender, location, subscription status
- Purchase details: item, category, purchase amount, season, size, color
- Shopping behavior: discount applied, previous purchases, purchase frequency, review rating, shipping type, payment method
- 37 missing values in `Review Rating`

## Tools Used

| Area | Tools |
|---|---|
| Data cleaning and EDA | Python, pandas |
| Database and analysis | PostgreSQL, SQL |
| Dashboard | Power BI |

## Workflow

### 1. Data preparation (Python)
- Loaded the data with pandas and checked it with `info()` and `describe()`
- Filled 37 missing review ratings with the median rating of each category
- Renamed columns to snake_case
- Created `age_group` (Young Adult, Adult, Middle-aged, Senior) and `purchase_frequency_days`
- Found that `promo_code_used` duplicates `discount_applied` and dropped it
- Loaded the cleaned data into PostgreSQL

### 2. SQL analysis
Answered 10 business questions, including:
1. Revenue by gender
2. High-spending customers who used discounts
3. Top 5 products by rating
4. Average spend by shipping type
5. Subscribers vs. non-subscribers
6. Most discount-dependent products
7. Customer segmentation (New, Returning, Loyal)
8. Top 3 products per category
9. Repeat buyers and subscriptions
10. Revenue by age group

### 3. Power BI dashboard
An interactive dashboard with KPI cards, subscription split, revenue and sales by category, revenue and sales by age group, and slicers for subscription status, gender, category and shipping type.

## Key Insights

- Total revenue is **$234,994**, with an average purchase of **$60.25** and an average rating of **3.75**
- **Apparel** brings the most revenue (44.7%), and **Winter Wear** the least (8.0%)
- Only **31%** of customers subscribe, and subscribers spend about the same as non-subscribers ($60.27 vs. $60.25)
- Male customers generate about **68%** of revenue
- **Young Adults (18-31)** are the highest revenue age group
- **80%** of customers are Loyal (more than 10 previous purchases)
- 43% of purchases use a discount, and products like Cap, Trainers and Overcoat are discounted in about half of their sales
- Two-Day and Priority shipping customers have the highest average spend

## Business Recommendations

- **Boost subscriptions** with real subscriber benefits
- **Build loyalty programs** to move Returning customers into the Loyal segment
- **Review the discount policy** to protect margins
- **Promote top-rated and best-selling products** in campaigns
- **Target Young Adults** and faster-shipping customers in marketing

## Dashboard Preview

![Dashboard](dashboard.png)

## How to Run

1. Clone the repository
2. Install the libraries: `pip install pandas sqlalchemy psycopg2-binary`
3. Run the Python notebook or script to clean the data and load it into PostgreSQL
4. Run the SQL queries in PostgreSQL
5. Open the `.pbix` file in Power BI Desktop

## Author

Mohammed Kaif Sayed
