# Customer Shopping Behavior Analysis

### An End-to-End Data Analytics Project Using Python, SQL, and Power BI

---

## 1. Project Overview

Customer Shopping Behavior Analysis is an end-to-end data analytics project focused on understanding customer purchasing patterns and generating actionable business insights from retail transaction data.

The project analyzes **3,900 customer purchase records across 18 attributes**. The complete workflow covers data preparation and exploration using Python, database integration with PostgreSQL, business analysis using SQL, and visualization through Power BI.

The overall objective is to transform raw customer shopping data into meaningful insights that can support customer engagement, loyalty, marketing, product positioning, and data-driven business decisions.

---

## 2. Project Objective

The primary objective of this project is to analyze customer shopping behavior and identify important trends in purchasing patterns, customer segments, product preferences, subscription behavior, and spending.

### Specific Objectives

- Clean and preprocess customer shopping data using Python and Pandas.
- Perform exploratory data analysis to understand the dataset and identify patterns.
- Handle missing values and improve data quality.
- Create useful derived features such as age groups and purchase frequency.
- Integrate the cleaned data with PostgreSQL.
- Use SQL queries to answer important business questions.
- Segment customers based on their previous purchase behavior.
- Build an interactive Power BI dashboard.
- Identify meaningful customer, product, revenue, and purchasing trends.
- Develop practical business recommendations based on the analysis.

---

## 3. Business Problem

A leading retail company wants to better understand its customers' shopping behavior in order to improve sales, customer satisfaction, and long-term loyalty.

Management has observed changes in purchasing patterns across customer demographics, product categories, and shopping behavior. The company wants to understand factors such as discounts, customer reviews, seasons, subscription status, and purchasing frequency that may influence customer decisions and repeat purchases.

### Main Business Question

> **How can the company leverage consumer shopping data to identify trends, improve customer engagement, and optimize marketing and product strategies?**

---

## 4. Dataset Description

The dataset contains customer shopping and transaction information collected from **3,900 purchases**.

| Dataset Attribute | Value |
|---|---:|
| Total Records | 3,900 |
| Total Columns | 18 |
| Missing Values | 37 |
| Missing Column | Review Rating |
| Data Type | Customer Shopping / Transaction Data |

### Main Features

#### Customer Demographics
- Age
- Gender
- Location
- Subscription Status

#### Purchase Details
- Item Purchased
- Category
- Purchase Amount
- Season
- Size
- Color

#### Shopping Behavior
- Discount Applied
- Promo Code Used
- Previous Purchases
- Frequency of Purchases
- Review Rating
- Shipping Type

#### Other Customer Information
- Payment Method

---

## 5. Project Workflow

```text
Raw Customer Data
        ↓
Data Loading – Python / Pandas
        ↓
Data Exploration & EDA
        ↓
Data Preprocessing
        ↓
Feature Engineering
        ↓
PostgreSQL Database
        ↓
SQL Business Analysis
        ↓
Power BI Dashboard
        ↓
Key Insights & Business Findings
        ↓
Business Recommendations
```

---

## 6. Data Preparation and Exploratory Data Analysis

Python and Pandas were used to prepare the raw customer shopping data for further analysis.

### 6.1 Data Loading

The dataset was imported into Python using Pandas and examined to understand its structure and contents.

### 6.2 Initial Exploration

Initial analysis was performed using:

- Dataset structure inspection
- Data type checks
- Summary statistics
- Missing-value analysis
- Basic exploratory analysis

Functions such as `df.info()` and `df.describe()` were used during the initial exploration.

### 6.3 Missing Value Handling

The dataset contained **37 missing values in the Review Rating column**.

These missing ratings were handled by imputing them using the **median review rating of the corresponding product category**.

### 6.4 Column Standardization

Column names were standardized into a consistent **snake_case** format to make them easier to work with in Python and SQL.

### 6.5 Feature Engineering

Additional features were created to support business analysis, including:

- `age_group`
- `purchase_frequency_days`

### 6.6 Redundant Column Check

The relationship between `discount_applied` and `promo_code_used` was examined. Since these fields contained overlapping information for the analysis, `promo_code_used` was removed from the cleaned dataset.

---

## 7. PostgreSQL Database Integration

After preprocessing, the cleaned customer shopping dataset was integrated with **PostgreSQL**.

The Python workflow was used to connect the cleaned Pandas DataFrame to the PostgreSQL database and load the prepared data.

This created a structured database environment where SQL could be used to perform business-focused analysis.

---

## 8. SQL Business Analysis

SQL was used to answer key business questions related to customer behavior, revenue, products, discounts, subscriptions, and customer segmentation.

### Business Questions

1. **Revenue by Gender** — Analyze total revenue generated by male and female customers.
2. **High-Spending Discount Users** — Identify customers who used discounts while spending at or above the overall average purchase amount.
3. **Top 5 Products by Rating** — Find the five products with the highest average customer review ratings.
4. **Shipping Type Comparison** — Compare average purchase amounts between Standard and Express shipping customers.
5. **Subscribers vs Non-Subscribers** — Compare customer count, average purchase amount, and total revenue between subscribers and non-subscribers.
6. **Discount-Dependent Products** — Calculate the discount rate for products and identify products with higher dependence on discounts.
7. **Customer Segmentation** — Classify customers into New, Returning, and Loyal groups based on their previous purchase count.
8. **Top 3 Products per Category** — Rank products within each category and identify the top three products using SQL window functions.
9. **Repeat Buyers and Subscriptions** — Analyze repeat buyers and compare their subscription status.
10. **Revenue by Age Group** — Analyze revenue contribution across different customer age groups.

---

## 9. Customer Segmentation

Customer segmentation was performed based on the number of previous purchases.

- **New** — customers with 1 previous purchase
- **Returning** — customers with 2–10 previous purchases
- **Loyal** — customers with more than 10 previous purchases

This segmentation helps the business understand customer maturity and identify opportunities to convert new customers into returning and loyal customers.

---

## 10. Power BI Dashboard

Power BI was used to transform the analyzed data into an interactive dashboard.

The dashboard provides a visual view of customer shopping behavior and helps communicate important findings in a business-friendly format.

### Dashboard Analysis Areas

- Revenue by gender
- Customer spending behavior
- Discount usage
- Product ratings
- Shipping type and purchase amount
- Subscription behavior
- Customer segments
- Product performance
- Age-group revenue
- Customer purchasing patterns

---

## 11. Key Insights

### Revenue by Gender
Female customers generated slightly higher total revenue than male customers.

### High-Value Discount Users
The analysis identified customers who use discounts while still making relatively high-value purchases. These customers represent an opportunity for targeted promotional strategies and exclusive offers.

### Top-Rated Products
Products such as **Blouse, Dress, and Shirt** showed strong customer ratings, indicating positive customer satisfaction for these products.

### Shipping Behavior
Customers using **Express Shipping** showed a higher average purchase amount than customers using Standard Shipping. This suggests that shipping preference may be associated with higher-value purchases.

### Subscription Behavior
The comparison between subscribers and non-subscribers provides insight into differences in customer spending and purchasing behavior. Subscription customers represent an important group for customer engagement and retention strategies.

### Customer Segmentation
Customers were grouped into New, Returning, and Loyal segments based on previous purchase behavior. This provides a useful framework for developing different strategies for different customer groups.

---

## 12. Business Recommendations

### 12.1 Boost Subscriptions
Promote subscription programs by offering exclusive benefits and improving the value proposition for customers.

### 12.2 Customer Loyalty Programs
Reward repeat buyers and encourage customers to move from the New and Returning segments toward the Loyal segment.

### 12.3 Review Discount Policy
Use discounts strategically and balance promotional activity with profitability and margin control.

### 12.4 Product Positioning
Highlight highly rated and strong-performing products in marketing campaigns and product promotions.

### 12.5 Targeted Marketing
Use customer characteristics, spending behavior, age groups, subscription status, and purchasing patterns to create more targeted marketing strategies.

---

## 13. Real-World Business Impact

This project demonstrates how customer transaction data can be transformed into actionable business intelligence.

The analysis can help a retail business:

- Understand customer purchasing behavior
- Identify valuable customer segments
- Improve customer engagement
- Encourage repeat purchases
- Strengthen customer loyalty
- Optimize discount strategies
- Improve product positioning
- Support targeted marketing
- Understand subscription-related behavior
- Make data-driven business decisions

---

## 14. Technology Stack

| Technology | Purpose |
|---|---|
| Python | Data preparation and analysis |
| Pandas | Data manipulation and preprocessing |
| Jupyter Notebook | Python-based analysis environment |
| PostgreSQL | Database storage and integration |
| SQL | Business analysis and querying |
| Power BI | Dashboard and visualization |
| GitHub | Project repository and documentation |

---

## 15. Project Execution

### Step 1 – Business Problem Identification
The retail business problem was defined by focusing on customer shopping behavior, purchasing patterns, customer engagement, and loyalty.

### Step 2 – Data Preparation and EDA
The raw dataset was loaded into Python, explored, cleaned, and prepared for analysis. Missing review ratings were handled and useful features were created.

### Step 3 – Database Integration
The cleaned data was connected to PostgreSQL and loaded into the database.

### Step 4 – SQL Analysis
SQL queries were written to answer the defined business questions and identify meaningful patterns.

### Step 5 – Power BI Dashboard Development
The analyzed data was visualized using Power BI to create a dashboard containing key business metrics and insights.

### Step 6 – Insight Generation and Recommendations
The results from SQL and Power BI were interpreted to identify customer behavior patterns and develop business recommendations.

### Step 7 – Documentation and Presentation
The complete project was documented through the project report, presentation, and GitHub repository.

---

## 16. Project Deliverables

1. **Data Preparation & Modeling** — Python
2. **Data Analysis** — PostgreSQL / SQL
3. **Visualization & Insights** — Power BI
4. **Project Report**
5. **Project Presentation**
6. **GitHub Repository**

---

## 17. Project Structure

```text
Customer-Shopping-Behavior-Analysis/
│
├── customer_shopping_behavior.csv
├── customer-shopping-behaviour.ipynb
├── customer_behavior_sql_queries.sql
├── Power BI Dashboard
├── Customer-Shopping-Behavior-Analysis.pptx
├── Customer_Segment_Behaviour_Report.pdf
└── README.md
```

---

## 18. Limitations

- The analysis is based on the available customer shopping dataset.
- The dataset represents purchase records rather than a complete view of every customer interaction.
- The analysis identifies relationships and patterns but does not establish causal relationships.
- Some business decisions may require additional information such as profit margins, marketing costs, inventory data, and customer lifetime value.

---

## 19. Future Scope

The project can be extended with:

- Customer lifetime value analysis
- More advanced customer segmentation
- Time-series purchasing analysis
- Product recommendation systems
- Churn prediction
- Marketing campaign analysis
- Profit and margin analysis
- Real-time business dashboards
- Integration with additional customer and sales data

---

## 20. Conclusion

The **Customer Shopping Behavior Analysis** project successfully analyzed customer purchasing patterns using an end-to-end data analytics approach involving **Python, PostgreSQL/SQL, and Power BI**.

The dataset consisted of **3,900 purchase records across 18 attributes**. Python was used for data loading, exploration, cleaning, missing-value handling, and feature engineering. The cleaned data was then integrated with PostgreSQL, where SQL queries were used to answer important business questions related to revenue, products, discounts, subscriptions, shipping, and customer segmentation.

Power BI was used to convert the analytical results into an interactive dashboard, making the findings easier to understand and communicate.

Overall, the project demonstrates how raw customer shopping data can be transformed into meaningful business insights. The findings highlight opportunities related to subscription growth, customer loyalty, targeted marketing, discount strategies, and product positioning.

The project shows how data analytics can help retail businesses better understand customers, improve engagement, optimize marketing strategies, and support data-driven business decisions.

---

## Author

**Customer Shopping Behavior Analysis**

*An End-to-End Data Analytics Project Using Python, SQL, and Power BI*
