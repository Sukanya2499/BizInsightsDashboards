# BizInsightsDashboards

## Overview
**BizInsightsDashboards** is an interactive Power BI dashboard providing key business insights with dynamic visuals, DAX calculations, tooltips, and bookmarks. It helps users analyze metrics like sales, profit margin, and customer performance across various dimensions.

## Key Features
- **Interactive Visuals**: Bar charts, line graphs, and matrix visuals for dynamic data exploration.
- **Dynamic Filters**: Slicers and filters for categories and time periods.
- **Tooltips**: Custom tooltips for deeper insights on hover.
- **Bookmarks**: Predefined bookmarks for easy navigation between views.
  
## Critical Measures (DAX)
1. **Total Sales**:
   ```DAX
   total_sales = SUM(product_sales_details[Sales])
   ```
2. **Total Sales Per Year**:
   ```DAX
   totalSalesIn2011 = CALCULATE(SUM(product_sales_details[Sales]),product_sales_details[orderYear]=2011)
   ```
3. **Customer Rank**:
   ```DAX
   CustomerRank = RANKX(ALL('customer'[Customer Name]), [total_sales], , DESC, DENSE)
   ```
4. **Percentage of Sales Based on Product Category**:
   ```DAX
   %_of_productCategory_sales = DIVIDE([total_sales],[total_sales_removefilters])
   ```

## Usage
1. **Filter Data**: Use slicers to filter by order year, order month.
2. **Bookmarks**: Toggle between views using bookmarks for quick access.
3. **Tooltips**: Hover over visuals to view additional information.

## Screenshots


![Screenshot (106)](https://github.com/user-attachments/assets/a3274762-257b-424d-b845-188a00d13c37)

![Screenshot (107)](https://github.com/user-attachments/assets/3e4db731-e324-4f06-9135-b0aa6295c774)

![Screenshot (114)](https://github.com/user-attachments/assets/3503c66d-574d-4ad5-a93f-bc77a627c096)

![Screenshot (113)](https://github.com/user-attachments/assets/aa7c36b6-b625-424c-aa4b-d57645a24505)

![Screenshot (109)](https://github.com/user-attachments/assets/08722ed2-2d42-4632-9eea-b23245a9887f)

![Screenshot (110)](https://github.com/user-attachments/assets/eb2edc4a-c33b-4f9c-b039-b0e524b1b883)

