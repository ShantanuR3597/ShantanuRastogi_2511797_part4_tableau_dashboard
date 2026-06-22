# Retail Executive Dashboard using Tableau

## Project Overview

This project focuses on designing and building an interactive executive dashboard using Tableau to support business decision-making.

The dashboard analyzes retail sales performance across multiple dimensions, including sales trends, regional performance, product profitability, customer segments, shipping efficiency, and product returns.

The objective is to transform raw transactional data into actionable business insights through effective data visualization and dashboard design.

---

# Business Problem

Retail leaders require a centralized view of business performance to monitor key metrics and identify growth opportunities.

The dashboard aims to answer the following business questions:

* How are sales performing over time?
* Which regions generate the highest sales?
* Which product categories generate the most profit?
* Which customer segments contribute the most revenue?
* How efficient are shipping operations?
* How do discounts relate to profitability?
* Which product categories experience the highest return rates?

The final dashboard enables leadership to monitor performance and make data-driven decisions.

---

# Dataset Overview

The dataset contains retail transaction data with approximately 4,200 records.

### Key Fields

#### Date Fields

* Order Date
* Ship Date

#### Geographic Fields

* Region
* State
* City

#### Product Fields

* Category
* Sub Category
* Product Name

#### Customer Fields

* Customer Segment
* Customer ID

#### Operational Fields

* Ship Mode
* Delivery Days
* Return Flag

#### Financial Measures

* Sales
* Profit
* Discount
* Quantity

#### Customer Metrics

* Customer Rating
* Campaign Channel

---

# Assumptions

The following assumptions were made during analysis:

1. Order ID represents a unique transaction.
2. Customer ID represents a unique customer.
3. Sales represents total revenue generated from an order.
4. Profit represents profit earned after costs.
5. Return Flag identifies returned orders.
6. Delivery Days measures shipping duration.
7. Order Date is used for trend analysis.
8. Ship Date is used for shipping performance analysis.

---

# Tableau Calculated Fields

The following calculated fields were created:

## Profit Margin

Used to evaluate profitability relative to sales.

```text
SUM([Profit]) / SUM([Sales])
```

---

## Cost

Estimated order cost.

```text
[Sales] - [Profit]
```

---

## Average Order Value

Average revenue generated per order.

```text
SUM([Sales]) / COUNTD([Order Id])
```

---

## Return Rate

Percentage of returned orders.

```text
SUM([Return Flag]) / COUNT([Order Id])
```

---

## Shipping Delay Bucket

Categorizes delivery performance.

```text
IF [Delivery Days] <= 2 THEN "Fast (0-2 Days)"
ELSEIF [Delivery Days] <= 5 THEN "Medium (3-5 Days)"
ELSE "Slow (6+ Days)"
END
```

---

# Dashboard Components

The executive dashboard contains the following visualizations:

## 1. Monthly Sales Trend

**Chart Type:** Line Chart

**Business Question:** How are sales changing over time?

---

## 2. Regional Performance View

**Chart Type:** Horizontal Bar Chart

**Business Question:** Which regions generate the highest sales?

---

## 3. Category Profitability View

**Chart Type:** Horizontal Bar Chart

**Business Question:** Which product categories generate the highest profit?

---

## 4. Customer Segment View

**Chart Type:** Horizontal Bar Chart

**Business Question:** Which customer segments contribute the most revenue?

---

## 5. Shipping Performance View

**Chart Type:** Horizontal Bar Chart

**Business Question:** Which shipping modes have the highest delivery times?

---

## 6. Discount vs Profit View

**Chart Type:** Scatter Plot

**Business Question:** How does discounting relate to profitability?

---

## 7. Return Analysis View

**Chart Type:** Stacked Bar Chart

**Business Question:** Which categories experience the highest returns?

---

# Dashboard KPIs

The dashboard includes three KPI cards:

### Total Sales

Overall sales generated across all transactions.

### Total Profit

Overall profit generated across all transactions.

### Total Orders

Total distinct orders in the dataset.

---

# Dashboard Interactivity

The dashboard includes interactive filtering capabilities.

### Available Filters

* Region
* Category
* Customer Segment

### Filter Behavior

Filters apply across all visualizations, allowing users to dynamically explore performance across different business dimensions.

### Interactive Actions

Selected charts can be used as dashboard filters to support deeper analysis.

---

# Key Business Insights

The dashboard highlights several important findings:

1. South region generates the highest sales.
2. Monthly sales remain relatively stable throughout the year.
3. Copiers are the most profitable product sub-category.
4. Home Office customers contribute the highest sales.
5. Standard Class shipping has the longest average delivery time.
6. Furniture experiences the highest number of returns.
7. High profitability is concentrated within a small number of product categories.
8. The business generates strong overall profit performance.

Detailed analysis is available in:

```text
outputs/business_insights.md
```

---

# Files Included

## Data

```text
data/dashboard_sales_data.xlsx
```

---

## Tableau Workbook

```text
tableau/executive_dashboard.twbx
```

---

## Outputs

```text
outputs/business_insights.md

outputs/dashboard_story.md

outputs/chart_selection_justification.md
```

---

## Screenshots

```text
screenshots/full_dashboard.png

screenshots/sales_trend_view.png

screenshots/regional_performance_view.png

screenshots/category_profitability_view.png

screenshots/filter_interaction_view.png
```

---

# Dashboard Design Principles Applied

The dashboard was designed using established data visualization best practices.

### Principles Applied

* Consistent chart formatting
* Clear chart titles
* Appropriate chart selection
* Limited and meaningful color usage
* Minimal visual clutter
* Easy comparison between categories
* Executive-focused layout
* Interactive exploration capability

### Visualization Mistakes Avoided

* 3D charts
* Excessive color palettes
* Unnecessary visual effects
* Overcrowded dashboard layouts
* Misleading chart types

---

# Limitations

The dashboard is based on historical transactional data and may not capture external factors such as:

* Seasonality
* Competitor activity
* Market conditions
* Promotional campaigns
* Economic changes

Additional analysis may be required before making strategic business decisions.

---

# Conclusion

This project demonstrates how Tableau can be used to transform raw retail transaction data into an interactive executive dashboard.

The dashboard provides leadership with a centralized view of business performance, enabling faster decision-making, operational monitoring, and identification of growth opportunities through data-driven insights.


