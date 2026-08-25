# E-commerce Sales Data Cleaning & Dashboard — Documentation

## 1. Project Overview

This project involved preparing and analyzing a large e-commerce sales dataset representing a potential e-commerce business.

The dataset contained **34,500 orders** and included information about orders, customers, products, pricing, discounts, payment methods, dates, delivery times, regions, returns, sales amounts, shipping costs, profit margins, and customer demographics.

The project involved:

- Preserving and preparing the source data
- Organizing the dataset into structured tables
- Formatting and validating important fields
- Creating an Order ID lookup/finder
- Performing exploratory data analysis
- Performing profitability analysis
- Performing regional analysis
- Creating an interactive Excel sales dashboard

## 2. Preserving the Raw Data

The original sales dataset was preserved without modification.

A copy of the entire dataset was created, and all preparation, formatting, organization, and analysis activities were performed using the copied dataset.

This ensured that the original source data remained available for reference throughout the project.

## 3. Dataset Structure

The original dataset contained the following fields:

1. Order ID
2. Customer ID
3. Product ID
4. Category
5. Price
6. Discount
7. Quantity
8. Payment Method
9. Order Date
10. Delivery Time (Days)
11. Region
12. Returned
13. Total Amount
14. Shipping Cost
15. Profit Margin
16. Customer Age
17. Customer Gender

The original dataset contained multiple types of information in a single large table.

## 4. Initial Data Preparation

### 4.1 Adjusting Row and Column Dimensions

The widths of rows and columns were adjusted according to the content within the cells.

This improved readability and made the dataset easier to review.

## 5. Splitting the Dataset into Structured Tables

The original dataset contained several unrelated categories of information within one large table.

To improve accessibility, organization, and efficiency when searching for information, the data was divided into three structured tables.

### 5.1 Order Table

The **Order Table** contains information directly related to individual orders.

The fields include:

- Order ID
- Category
- Price
- Quantity
- Discount
- Payment Method
- Order Date
- Delivery Time (Days)
- Region
- Returned
- Total Amount
- Shipping Cost
- Profit Margin

### 5.2 Product Table

The **Product Table** contains product-related information.

The fields include:

- Product ID
- Category

This separated product information from order-specific information.

### 5.3 Customer Table

The **Customer Table** contains customer-related information.

The fields include:

- Customer ID
- Customer Age
- Customer Gender

Separating customer information from order information improved accessibility and made the dataset easier to search and manage.

## 6. Data Validation and Formatting

Because the dataset was already relatively clean, the main preparation work focused on formatting the fields correctly and rechecking calculated values.

The Total Amount, Shipping Cost, and Profit Margin fields were reviewed to ensure that their values were correctly calculated based on the relevant sales information.

### 6.1 Numeric Fields

The following fields were converted into **Number** format with two decimal places:

- Price
- Quantity
- Discount
- Total Amount
- Shipping Cost
- Profit Margin

Two decimal places were retained because the source data contained prices, discounts, and financial values with this level of precision.

### 6.2 Order Date

The Order Date field was converted into **Date** format.

This allowed the date field to be used appropriately for subsequent analysis, including time-based sales analysis.

## 7. Table Identification and Usability Improvements

Large-font headings were added above the respective tables to clearly communicate what each table represented.

The first two rows were also frozen to keep important headings visible while scrolling through the data.

These changes improved the readability and usability of the workbook.

## 8. Order ID Finder Table

After creating the three structured tables, an **Order ID Finder Table** was created.

The finder allows an Order ID to be entered and retrieves the corresponding information associated with that order.

The finder table contains the available fields of the order as rows, while the corresponding values are returned based on the entered Order ID.

The finder table label and first input cell were frozen to make the lookup functionality easier to use while navigating the worksheet.

### 8.1 VLOOKUP

Excel's `VLOOKUP` function was used to retrieve information associated with the entered Order ID.

This allowed the finder to dynamically return the relevant order information without requiring the user to manually search through the entire dataset.

### 8.2 IFERROR

`IFERROR` was also used to provide error handling.

This prevents lookup errors from being displayed when an Order ID cannot be found or when the lookup does not return a valid result.

# 9. Data Analysis Reports

After preparing and organizing the sales dataset, several analysis workbooks were created to explore the information and extract business-relevant insights.

The analysis was divided into:

1. Exploratory Data Analysis
2. Profitability Data Analysis
3. Regional Data Analysis

# 10. Exploratory Data Analysis

An **Exploratory Data Analysis** workbook was created to explore the prepared dataset using:

- Pivot Tables
- Charts
- Column charts
- Pie charts
- Conditional formatting

The purpose was to use the prepared sales data to identify patterns and answer business-related questions.

## 10.1 Questions Addressed by the Exploratory Analysis

The analysis was used to answer the following questions:

1. Which product category received the most orders?

2. Which product category generated the most profit?

3. Which region contributed the most to profits?

4. What was the most used payment method by region?

5. Which product category was purchased the most in each region?

6. What proportion of orders were returned versus not returned?

7. Which region placed the most orders?

8. Which product category had the most returned orders?

9. What were the sales figures for each month?

10. What was the most commonly used payment method?

# 11. Profitability Data Analysis

A separate **Profitability Data Analysis** workbook was created to focus specifically on questions related to sales and profit.

The analysis addressed four major areas.

### 11.1 Sales by Month

Monthly sales were analyzed to identify changes in sales over time.

### 11.2 Profit Earned by Month

Monthly profit was analyzed to understand how profitability changed across the period.

### 11.3 Profit by Product Category

Profit was analyzed across product categories to determine which categories generated the highest levels of profit.

### 11.4 Profit by Region

Profit was also analyzed across regions to identify which regions contributed most to overall profitability.

# 12. Regional Data Analysis

A separate **Regional Data Analysis** workbook was created to examine sales activity across different regions.

The analysis addressed the following questions:

1. Which region contributed the most profit?

2. How many orders came from each region?

3. What were the sales figures for each region?

4. What was the most used payment method by region?

5. Which product category was purchased the most in each region?

This analysis provided a region-focused view of sales activity, profitability, customer purchasing behavior, and payment-method usage.

# 13. Interactive Sales Dashboard

An interactive **Sales Dashboard** was created in Microsoft Excel to provide a consolidated visual representation of the prepared sales data.

The dashboard contains dynamic data visualizations designed to make the analysis easier to understand and explore.

The dashboard uses Excel's interactive filtering functionality, including:

- **Product Category Slicers**
- **Region Slicers**
- **Timeline**

These controls allow the user to filter the dashboard and dynamically explore the underlying sales information.

## 13.1 Dashboard KPI Section

The dashboard was divided into two major sections.

The first section contains key performance indicators covering important sales and operational metrics.

The KPIs include measures such as:

- Total Sales
- Total Discount
- Net Sales
- Total Profit
- Average Delivery Days
- Total Expenses
- Total Quantity of Product Sold
- Quantity of Returned Products
- Shipping Cost per Product
- Profit Margin per Product

The Net Sales metric is calculated as:

> **Net Sales = Total Sales − Total Discount**

These KPIs provide a concise summary of the overall sales and profitability performance.

## 13.2 Dashboard Visualization Section

The second section of the dashboard contains visualizations designed to make patterns in the sales data easier to understand.

The visual analysis covers areas such as:

- Sales trends
- Profitability
- Product categories
- Regional performance
- Order distribution
- Payment methods
- Returned orders

The visualizations respond to the dashboard's interactive filters, allowing the user to explore different segments of the dataset.

# 14. Dashboard PDF Summary

A PDF version of the sales dashboard was also created.

The PDF provides a consolidated view of the overall dashboard and serves as a static summary of the analysis and visual reporting.

The Excel workbook remains the interactive version of the dashboard, while the PDF provides a convenient non-interactive representation of the final dashboard.

# 15. Final Outcome

The project produced several outputs:

### Structured Sales Data

The original large dataset was reorganized into:

- Order Table
- Product Table
- Customer Table

### Order Finder

An Order ID Finder was created using `VLOOKUP` and `IFERROR` to retrieve order information efficiently.

### Exploratory Data Analysis

An interactive Excel-based analysis was created using:

- Pivot Tables
- Charts
- Conditional Formatting
- Slicers
- Timeline

### Profitability Analysis

A dedicated analysis was created to examine:

- Sales by month
- Profit by month
- Profit by product category
- Profit by region

### Regional Analysis

A dedicated analysis was created to examine:

- Regional profit
- Regional order volume
- Regional sales
- Payment methods by region
- Product categories by region

### Interactive Sales Dashboard

A dynamic Excel dashboard was created containing:

- Sales and profitability KPIs
- Data visualizations
- Product Category Slicers
- Region Slicers
- Timeline filtering

A PDF version of the dashboard was also produced as a static summary.
