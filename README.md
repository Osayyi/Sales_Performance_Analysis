# Sales_Performance_Analysis
The Sales Data dataset provides comprehensive details on transactions made at a retail store.

### Table of Content
[Project Overview](#project-overview)

[Key Fields](#key-fields)

[Data Sources](#data-sources)

[Tools Used](#tools-used)

[Data Cleaning](#data-cleaning)

[Data Analysis](#data-analysis)

[Findings and Insights](#findings-and-insights)

[Conclusion](#conclusion)

[Future Recommendations](#future-recommendations)



### Project Overview:
---
*Objective*:
This dataset is used to assess sales patterns by product, region and month and also analyze retail performance by examining top-selling products, identifying regional sales trends, and tracking monthly performance.

### Key Fields:
---
The key fields includes the following features related to sales data:
 - OrderID: A unique identifier for each sale.
 - Customer Id: A unique identifier for each customer.
 - Product: The type of product sold.
 - Region: Geographical region where the sale took place.
 - OrderDate: Date on which the sale occurred.
 - Quantity: Number of units sold in each transaction.
 - UnitPrice: Price per individual unit of the product. 
 - Total Sales: Total revenue for the transaction, calculated as Quantity Sold * Unit Price.

### Data Sources
---
This data set is a Capstone Dataset and was gotten from The Incubator Hub (LITA) as a task for my final Project.

### Tools Used
---
- Microsoft Excel [Download Here](https://www.microsoft.com)
   1. For Data Cleaning
   2. Analysis
      
- SQL - Structured Query Language
   1. for Quring of Data
  
- PowerBi [Download Here](https://www.PowerBi.com)
    1. for Data Visualization

### Data Cleaning
 - Removing Duplicates: Checked for duplicate rows to ensure each transaction is unique.
   - "Remove Duplicates Feature"
1. Select the data range (including headers).
2. Go to "Data" tab.
3. Click "Remove Duplicates" (in "Data Tools" group).
4. Choose "Select All" or specific columns.
5. Click
 - Handling Missing Values: There was no missing values.
 - Standardizing Dates: Converted OrderDate to a standard date format.
 - Calculating Total Sales: Ensured Total sales was calculated as Quantity Sold * Unit Price for consistency.

### Data Analysis
 - Excel Analysis

   - Pivot Tables for Sales data:
1. Created pivot tables in Excel to summarize Total Sales by Product Category, Region, and Month.
2. Analyzed Average Sales per Product and Total Revenue by Region to identify high-performing products and regions.

#### Total Sales By Product
The Highest revenue came from the sales of *Shoes* 
![Screenshot (9)](https://github.com/user-attachments/assets/12e0eb2b-ba18-4ff7-9bcf-1bf6e44e00de)

#### Total Sales By Region
The most Sales was recorded in the Southern Region
![Screenshot (10)](https://github.com/user-attachments/assets/cff63e62-5ae0-476c-b8e6-2cda871c229a)

#### Total Sales BY Month
Monthly Sales peaked in February, likely due to valentine shopping
![Screenshot (11)](https://github.com/user-attachments/assets/3e60b6dd-e970-4ab6-bb77-f67cea3df840)

#### Average sales Per Product
Avearge Sales per product calculated as =AVERAGE(H2:H9922)
Average sales is 211.7820784
![Screenshot (12)](https://github.com/user-attachments/assets/34ac1ba7-c5a6-4c8b-bf6b-10814d7ed1cc)

#### Total Revenue By Region
The South generated the highest revenue at 927,820
![Screenshot (13)](https://github.com/user-attachments/assets/71173050-c26e-4813-a80a-6c5081fd12c5)

*Other Reports*
I created a report in Excel analyzing the monthly sales trend
**In my analysis of the monthly sales trend, February showed the highest total sales compared to other months**
![Screenshot (14)](https://github.com/user-attachments/assets/a040167c-5df3-422c-8762-adab10c7dd51)


*Insights:*
 - The highest revenue came from the sales of shoe, mainly in the southern region.
 - Monthly sales peaked in February, likely due to valentine shopping.

 #### SQL Analysis
```
 SELECT * FROM TABLE [dbo].[LITA Capstone Dataset Osayi favour Sales Data]

 ---- Total Sales For Each Product Category ----
SELECT Product, SUM(UnitPrice) AS TotalSales
FROM [dbo].[LITA Capstone Dataset Osayi favour Sales Data] 
GROUP BY Product
```

*Insights*
This query sums up the total sales for each product category, allowing us to see which category performs best.
Shoes perform best.

```
---- Number of Sales Transactions in Each Region ----
SELECT Region, COUNT(*) AS SalesTransaction
FROM [dbo].[LITA Capstone Dataset Osayi favour Sales Data]
GROUP BY Region;
```

*Insights*
Shows the count of transactions per region, highlighting areas with higher sales activity.

```
---- Highest-selling Product by Total Sales Value ----
SELECT Product, SUM(UnitPrice) As TotalSales
 FROM [dbo].[LITA Capstone Dataset Osayi favour Sales Data] 
 GROUP BY Product
 ORDER BY 1 DESC
```

*Insights*
This query gives insight into your best seller.

```
```

 - Power BI Dashboard

*Insights*

### Findings and Insights

### Conclusion

### Future Recommendations
1. Introduce a loyalty program for long-term customers.
2. Expand popular product categories in high-performing regions.
