# Retail Profitability & Optimization Suite

## Project Overview

This project is developed using Power BI based on the Sample Superstore Dataset. The objective is to analyze retail sales performance, identify profit and loss trends, evaluate product category performance, and provide actionable business recommendations for improving profitability and operational efficiency.

---

## Dataset

**Dataset Name:** Sample Superstore Dataset

**Source:** Kaggle / Sample Superstore Dataset

### Key Fields

* Order ID
* Order Date
* Customer Name
* Segment
* Category
* Sub-Category
* Product Name
* Sales
* Quantity
* Discount
* Profit
* Region
* State
* Ship Mode

---

## Business Problem

Retail businesses often struggle to identify:

* Loss-making products
* Underperforming regions
* High-discount products reducing profitability
* Inefficient sales distribution across categories

This dashboard helps management make data-driven decisions by highlighting key performance indicators and business risks.

---

## Objectives

* Analyze sales and profit performance.
* Identify profitable and loss-making products.
* Evaluate category and sub-category contribution.
* Compare regional performance.
* Monitor discount impact on profitability.
* Generate recommendations for business improvement.

---

## Power BI Features Used

### Power Query

* Replace Values
* Data Cleaning
* Data Type Conversion
* Conditional Columns
* Group By Transformations

### Data Modeling

* Relationships
* Star Schema Concepts

### DAX Measures

#### Total Sales

```DAX
Total Sales = SUM(Orders[Sales])
```

#### Total Profit

```DAX
Total Profit = SUM(Orders[Profit])
```

#### Profit Margin %

```DAX
Profit Margin % =
DIVIDE(
    SUM(Orders[Profit]),
    SUM(Orders[Sales]),
    0
) * 100
```

#### Total Orders

```DAX
Total Orders = DISTINCTCOUNT(Orders[Order ID])
```

#### Year-To-Date Sales

```DAX
YTD Sales =
TOTALYTD(
    SUM(Orders[Sales]),
    Orders[Order Date]
)
```

---

## Dashboard Components

### KPI Cards

* Total Sales
* Total Profit
* Total Orders
* Profit Margin %

### Visualizations

* Sales by Category
* Profit by Sub-Category
* Sales by Region
* Monthly Sales Trend
* Top Performing Products
* Loss-Making Products
* Discount vs Profit Analysis

### Filters / Slicers

* Region
* Category
* Sub-Category
* Segment
* Year

---

## Key Insights

### High Performing Categories

* Technology generated the highest sales and profit.
* Office Supplies showed stable performance.

### Low Performing Areas

* Some Furniture sub-categories generated losses despite high sales.
* Heavy discounting reduced profit margins significantly.

### Regional Analysis

* Certain regions consistently outperformed others.
* Regional demand variations affected profitability.

---

## Recommendations

1. Reduce excessive discounting on low-margin products.
2. Focus inventory investment on high-profit categories.
3. Review loss-making sub-categories and pricing strategies.
4. Improve regional supply chain planning.
5. Promote high-margin products through targeted campaigns.

---

## Assessment Tasks Covered

### Conceptual Understanding

* Import vs DirectQuery
* Data Types in Power BI
* Sorting Visuals
* Visual-Level Filters
* DAX Measures
* File Path Considerations

### Practical Implementation

* Data Cleaning in Power Query
* Conditional Columns
* DAX Calculations
* KPI Cards
* Top N Filters
* Profit Margin Analysis

---

## Tools Used

* Power BI Desktop
* Power Query Editor
* DAX
* Microsoft Excel
* Sample Superstore Dataset

---

## Expected Outcome

The dashboard provides a comprehensive view of retail performance, enabling stakeholders to identify profit opportunities, reduce losses, and make informed business decisions based on data-driven insights.
