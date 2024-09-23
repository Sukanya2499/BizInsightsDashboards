# BizInsightsDashboards

## Overview
**BizInsightsDashboards** is an interactive Power BI dashboard providing key business insights with dynamic visuals, DAX calculations, tooltips, and bookmarks. It helps users analyze metrics like sales, profit margin, and customer performance across various dimensions.

## Key Features
- **Interactive Visuals**: Bar charts, line graphs, and matrix visuals for dynamic data exploration.
- **Dynamic Filters**: Slicers and filters for top N customers, categories, and time periods.
- **Tooltips**: Custom tooltips for deeper insights on hover.
- **Bookmarks**: Predefined bookmarks for easy navigation between views.
  
## Critical Measures (DAX)
1. **Total Sales**:
   ```DAX
  total_sales = SUM(product_sales_details[Sales])
   ```
2. **Total Sales in Each Year**
   ```DAX
  totalSalesIn2011 = CALCULATE(SUM(product_sales_details[Sales]),product_sales_details[orderYear]=2011)
   ```
3. **Customer Rank**:
   ```DAX
   CustomerRank = RANKX(ALL('customer'[Customer Name]), [total_sales], , DESC, DENSE)
   ```
4. **Product Category Wise Sales Percentage**:
   ```DAX
   total_sales_removefilters = CALCULATE([total_sales],REMOVEFILTERS(product_sales_details[Category]))
  %_of_productCategory_sales = DIVIDE([total_sales],[total_sales_removefilters])
   ```
## Usage

1. **Filter Data**: Use slicers to filter by top N customers, product categories, or time periods.
2. **Bookmarks**: Toggle between views using bookmarks for quick access.
3. **Tooltips**: Hover over visuals to view additional metrics like top five products on the basis of sales in each category.


![Screenshot (106)](https://github.com/user-attachments/assets/33c01a10-320c-4dbf-85df-886abdcf1f76)
![Screenshot (107)](https://github.com/user-attachments/assets/239489c9-bd08-4cb4-b19e-b950cc3cf9a2)

![Screenshot (114)](https://github.com/user-attachments/assets/e99b210c-e2e6-4eb6-bd7f-711109fd06d4)

![Screenshot (113)](https://github.com/user-attachments/assets/d46f9a81-d746-40bd-836b-0bc96bf0cf60)
![Screenshot (109)](https://github.com/user-attachments/assets/1679507b-38f1-4074-9354-071d6b7efa34)
![Screenshot (110)](https://github.com/user-attachments/assets/6aef3725-5d8f-4f26-9860-a70da5999342)
