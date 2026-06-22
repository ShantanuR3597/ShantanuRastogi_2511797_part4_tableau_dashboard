# Chart Selection Justification

## 1. Monthly Sales Trend

### What Question Does This Chart Answer?
How are sales changing over time?

### Why Is This Chart Type Appropriate?
A line chart is the best choice for displaying trends across months because it clearly shows increases, decreases, and overall movement over time.

### What Field Is Used?
- X-Axis: Order Date (Month)
- Y-Axis: Sales

### Design Principle Applied
Used a simple line chart with minimal clutter to emphasize trend visibility.

### What Mistake Was Avoided?
Avoided using pie charts or categorical charts that do not effectively display time-series data.

---

## 2. Regional Performance View

### What Question Does This Chart Answer?
Which region generates the highest sales?

### Why Is This Chart Type Appropriate?
A horizontal bar chart allows easy comparison of sales performance across regions.

### What Field Is Used?
- Dimension: Region
- Measure: Sales
- Color: Profit

### Design Principle Applied
Regions are displayed side-by-side to enable quick comparison and ranking.

### What Mistake Was Avoided?
Avoided stacked charts that could make regional comparisons more difficult.

---

## 3. Category Profitability View

### What Question Does This Chart Answer?
Which product sub-categories generate the highest profit?

### Why Is This Chart Type Appropriate?
A horizontal bar chart clearly ranks categories by profitability and highlights top contributors.

### What Field Is Used?
- Dimension: Sub Category
- Measure: Profit

### Design Principle Applied
Bars are sorted by profit to improve readability and business interpretation.

### What Mistake Was Avoided?
Avoided unsorted charts that make performance ranking difficult to identify.

---

## 4. Customer Segment View

### What Question Does This Chart Answer?
Which customer segment contributes the most sales?

### Why Is This Chart Type Appropriate?
Bar charts provide straightforward comparison between customer groups.

### What Field Is Used?
- Dimension: Customer Segment
- Measure: Sales
- Color: Profit

### Design Principle Applied
Used clear labels and limited categories for quick executive interpretation.

### What Mistake Was Avoided?
Avoided pie charts that become difficult to compare accurately.

---

## 5. Shipping Performance View

### What Question Does This Chart Answer?
Which shipping mode has the highest average delivery time?

### Why Is This Chart Type Appropriate?
Bar charts make it easy to compare delivery performance across shipping methods.

### What Field Is Used?
- Dimension: Ship Mode
- Measure: Average Delivery Days

### Design Principle Applied
Focused on operational performance using a single, easy-to-read metric.

### What Mistake Was Avoided?
Avoided complex visualizations that could distract from delivery comparisons.

---

## 6. Return Analysis View

### What Question Does This Chart Answer?
Which categories experience the highest return volume?

### Why Is This Chart Type Appropriate?
A stacked bar chart shows both total returns and regional contribution simultaneously.

### What Field Is Used?
- Dimension: Category
- Measure: Return Flag
- Color: Region

### Design Principle Applied
Color segmentation helps identify return patterns across regions.

### What Mistake Was Avoided?
Avoided separate charts for each region, which would reduce dashboard efficiency.

---

## Dashboard-Level Design Decisions

### Filters Included
- Region
- Customer Segment
- Category

### Why These Filters Were Chosen
These filters allow executives to quickly explore performance across key business dimensions without overwhelming the dashboard.

### KPI Cards Included
- Total Sales
- Total Profit
- Total Orders

### Why KPI Cards Were Added
These metrics provide an immediate business summary before users analyze detailed charts.

### Interactivity Used
Dashboard filters update all charts simultaneously, allowing dynamic business exploration.

### Design Principles Applied Across Dashboard
- Consistent chart formatting
- Consistent color usage
- Clear chart titles
- Minimal clutter
- Readable labels
- Business-focused layout
- Easy comparison across views

### Misleading Design Choices Avoided
- 3D charts
- Excessive colors
- Unnecessary visual effects
- Overcrowded layouts
- Complex visualizations without business value

