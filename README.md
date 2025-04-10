# Customer Segmentation of the Superstore - Power BI Report

![Power BI Report](https://github.com/taarikakanauji/customer-segmentation-of-the-superstore/raw/main/images/power-bi-report.jpg)

## Problem Statement

Stakeholders across various departments lack a centralized, data-driven view to effectively monitor and analyze profit and sales trends across customer segments, product categories, and geographic regions within the USA. This gap makes it challenging to identify underperforming areas, optimize strategies, and drive informed decision-making. There is a need for an interactive dashboard that provides actionable insights.

This dashboard helps stakeholders to track and analyse profit and sales across customer segment, category, and regions in the USA. It provides data-driven insights, to identify patterns, optimize strategies, and improve performance. The dashboard is designed for key stakeholders:

- Business Owners & Decision Makers

- Sales & Marketing Teams

- Store & Inventory Managers

- Customer Engagement Teams

## Objective

- Tracking Profitability by monitoring key metrics, including total, maximum, and minimum profit

- To analyze and compare total profit by different customer segments and improve weaker segments

- Balance regional sales performance 

- Boost sales in weak categories

- To identify potential challenges and recommendations

## Key Questions

    Q : How much total profit is generated from the East region?

    Q : How do profit and sales metrics vary based on different Ship Modes, Customer Segments, Product Categories, and Order Dates?

    Q : What are the overall profit insights including total, maximum, minimum profit and average sales?

    Q : Which geographic locations/states contribute most to the total profit and which need attention?

    Q : How is profit distributed across different customer segments?

    Q : Which combinations of customer segments and product categories generate higher or lower profits?

    Q : How does total profit vary by region?

    Q : What is the profit contribution of each product category?

    Q : Which categories perform the best?

    Q : Where to focus marketing, inventory, and sales strategies based on this data?

## Steps followed 

As a Business analyst for a retail superstore, I was tasked with developing an interactive report/dashboard to help stakeholders track profitability and sales performance across customer segments, product categories, and regions. The goal was to provide actionable insights to optimize marketing, inventory, and sales strategies. Below, I explain my step-by-step approach to designing this dashboard in Power BI.

- Step 1 : Load data into Power BI Desktop, dataset is a csv file.

- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.

- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".

- Step 4 : After cleaning the data, It was observed that in none of the columns errors & empty values were present.

- Step 5 : In the report view, under the view tab, default theme was selected.

- Step 6 : Creating KPI Cards for Key Metrics - I created four KPI cards to present high-level business performance. These cards offer a quick snapshot for executives to monitor financial health.

        Total Profit – Shows overall profitability.
        Measure Used : SUM(Orders[Profit])

        Max Profit – Identifies the highest single profit value.
        Measure Used : MAX(Orders[Profit])

        Min Profit – Reveals losses or low-margin transactions.
        Measure Used : MIN(Orders[Profit])

        Avg Sales – Tracks average transaction value.
        Measure Used : AVERAGE(Orders[Sales])

   I formatted these cards with currency symbols and conditional coloring (e.g., red    for negative Min Profit) to make trends immediately visible. These KPIs help executives quickly assess performance without diving into granular data.

  ![KPI Cards](https://github.com/taarikakanauji/customer-segmentation-of-the-superstore/raw/main/images/cards.jpg)

- Step 7 : Visualizing Profit by State with a Map - To geographically analyze profitability, I used a filled map to understand which U.S. states contribute most to profit. This gives a geographic overview of performance across the U.S.

        Fields used:

        Location: State

        Color Saturation: Total Profit (Color Intensity: darker shades = higher profit)

  This visual quickly highlights top-performing states (e.g., California) and underperforming regions (e.g., the Central, east). The map helps regional managers focus efforts where they’re needed most.

  ![Geographical Map](https://github.com/taarikakanauji/customer-segmentation-of-the-superstore/raw/main/images/map.jpg)
           
- Step 8 : Analyzing Customer Segments with Pie Chart (Customer Segment Distribution by Profit) - I added a pie chart to show how profits are split among different customer segments. 

        Fields Used:

        Legend: Customer Segment (Consumer, Corporate, Home Office)

        Values: Total Profit

   The chart revealed that Consumer clients contribute ~49% of total profit, making them the most valuable segment. This insight suggests prioritizing sales strategies.

  ![Pie Chart 1](https://github.com/taarikakanauji/customer-segmentation-of-the-superstore/raw/main/images/pie-1.jpg)

- Step 9 : Comparing Performance with a Bar Chart for Profit by Segment and Category - To dig deeper into how customer segments interact with product categories, I created a stacked bar chart. This chart helps analyze product performance within each customer segment.

        Fields used:

        Y-Axis: Customer Segment

        Legend: Category

        X-axis: Total Profit

   This showed that Technology products drive the highest profits for Consumer customers, while Furniture lags. The sales team can use this to push high-margin products to other buyers.

  ![Bar Chart 2](https://github.com/taarikakanauji/customer-segmentation-of-the-superstore/raw/main/images/bar-2.jpg)

- Step 10 : Regional Profit Trends with a Bar Chart - To compare total profit across regions (East, West, Central, South), I used a simple Stacked bar chart. Helps spot strong vs. underperforming regions quickly.

        Fields used:

        Y-Axis: Region

        X-Axis: Total Profit

  The West emerged as the top-performing region, while the East, Central struggled. This could prompt a review of regional pricing or marketing strategies. 

  ![Bar Chart 1](https://github.com/taarikakanauji/customer-segmentation-of-the-superstore/raw/main/images/bar-1.jpg)

- Step 11 : Product Category Breakdown with a Pie Chart - Another pie chart displayed profit distribution by category. This pie chart highlights which product categories generate the most profit. A great way to visualize which categories are driving revenue.

        Fields used:

        Legend: Category (Technology, Office supplies, Furniture)

        Values: Total Profit

  Technology (46%) and Office Supplies (42%) dominated profits, while Furniture contributed just 12%. This suggests reevaluating Furniture pricing or promotions.  

  ![Pie Chart 2](https://github.com/taarikakanauji/customer-segmentation-of-the-superstore/raw/main/images/pie-2.jpg)

- Step 12 : In the report view, under the insert tab, text box is added to the canvas, to Name/Title the report "Customer Segmentation of the Superstore".

  ![Top Navigation Bar](https://github.com/taarikakanauji/customer-segmentation-of-the-superstore/raw/main/images/top-bar.jpg)

- Step 13 : Implementing Collapsible Filters Using Bookmarks in Power BI - To enhance user experience in our report, I implemented a collapsible filter panel using Power BI's bookmark functionality. This design allows users to show/hide filters with a single click, maximizing screen space for data visualization while keeping filtering options easily accessible.Added Filter Icon:

  First Added Filter Icon, Under the Insert tab, in the Elements group, I selected "Image" to add a filter icon to the canvas. This icon serves as a button to open/expand the filter pane.

  I placed all slicers (Ship Mode, Customer Segment, Category, Order Date) together in a side panel on the report canvas. Positioned them to the right side as a slide-out filter section.

  Setting Up Slicers for Interactive dynamic Filtering - To ensure users could dynamically explore the data by interacing and filtering the entire Report, I implemented slicers and These filters help in narrowing down the analysis to specific dimensions of interest.

  I added slicers for:

  Ship Mode (First Class, Same Day, Second Class, Standard Class)

  Customer Segment (Consumer, Corporate, Home Office)

  Product Category (Furniture, Office Supplies, Technology)

  Order Date (with a hierarchical drill-down by Year -> Quarter -> Month -> Date)

  I chose dropdown-style slicers for a clean interface, ensuring they influence all report visuals. This allows business teams to filter data—for example, comparing profitability between Corporate and Home Office customers or analyzing seasonal trends. 

  I created two bookmarks to enable the expand/collapse functionality:

  Bookmark 1 – "Open Pane": Captures the state where all filters are visible and highlights the "close" icon. Configured to show the full filter panel. Slicers are visible.

  Bookmark 2 – "Close Pane": Captures the state with filters hidden  Hides the filter pane. Only the "filter" icon is visible to expand again.

  Both bookmarks were configured by, Checking “Data” off (to avoid changing data context), Enabling only “Display” and “Selected visuals”.

  ![Filter Pane](https://github.com/taarikakanauji/customer-segmentation-of-the-superstore/raw/main/images/filter-pane.jpg)


- Step 14 : Implementing a Reset Filters - To enhance the usability and interactivity of the Power BI report, I added a Reset Filter icon that allows users to quickly clear all slicer selections and revert the report back to its default view. Reduces hesitation to apply filters ("What if I can't undo?").

  First, Using the Insert > Image option, I added a reset or refresh icon. This icon was placed near the filters for visibility and ease of access.

  I cleared all slicer selections (Ship Mode, Customer Segment, Product Category, and Order Date). Then, I created a new bookmark titled “Clear All/Reset Filters”. 

  Bookmark options were configured with Data (checked) – this ensures that all slicer/filter states are saved.

  I enabled Action on the reset filters icon by setting, Type- Bookmark and Bookmark- Clear all Filters. This ensures that when the icon is clicked, all slicers and filters return to their default (unselected) state.

  ![Reset Icon](https://github.com/taarikakanauji/customer-segmentation-of-the-superstore/raw/main/images/reset-icon.jpg)

# Snapshot of Report (Power BI Service)

  ![Power BI Service Report](https://github.com/taarikakanauji/customer-segmentation-of-the-superstore/raw/main/images/power-bi-service.jpg)

# Report Snapshot (Power BI DESKTOP)

  ![Full Power BI Dashboard](https://github.com/taarikakanauji/customer-segmentation-of-the-superstore/raw/main/images/power-bi-full.jpg)

# **Project Resources: Customer Segmentation of the Superstore**  

### **Detailed Report (PDF)**  
[Insights of Customer Segmentation of the Superstore](https://github.com/taarikakanauji/customer-segmentation-of-the-superstore/blob/main/Insights%20of%20Customer%20Segmentation%20of%20the%20Superstore.pdf)  

### **Power BI Desktop Demo**  
[Power BI Demo (MKV)](https://github.com/taarikakanauji/customer-segmentation-of-the-superstore/blob/main/Power%20BI%20Demo.mkv)  

### **Power BI Service Demo**  
[Power BI Service Demo (MKV)](https://github.com/taarikakanauji/customer-segmentation-of-the-superstore/blob/main/Power%20BI%20Service%20Demo.mkv)  

### **Dataset Folder**  
[Dataset Files](https://github.com/taarikakanauji/customer-segmentation-of-the-superstore/tree/main/Dataset)  

### **PBIP Files**  
- **Report:** [Report Files](https://github.com/taarikakanauji/customer-segmentation-of-the-superstore/tree/main/Customer%20Segmentation%20of%20%20the%20Superstore.Report)  
- **Semantic Model:** [Semantic Model Files](https://github.com/taarikakanauji/customer-segmentation-of-the-superstore/tree/main/Customer%20Segmentation%20of%20%20the%20Superstore.SemanticModel)  
- **Project File:** [Customer Segmentation PBIP](https://github.com/taarikakanauji/customer-segmentation-of-the-superstore/blob/main/Customer%20Segmentation%20of%20%20the%20Superstore.pbip)  
- **Gitignore:** [.gitignore](https://github.com/taarikakanauji/customer-segmentation-of-the-superstore/blob/main/.gitignore)  

### **Project README (Setup Guide)**  
[README.md](https://github.com/taarikakanauji/customer-segmentation-of-the-superstore/blob/main/README.md)  

# Conclusion

This dashboard empowers stakeholders to:
- Identify high-value segments (Consumer + Technology)
- Spot regional opportunities (invest in the West, improve the South, Central, East)
- Optimize inventory (Furniture, Office Supplies were relatively underperforming)

By leveraging these insights, the superstore can allocate resources more effectively, boost profitability, and address underperforming areas.


