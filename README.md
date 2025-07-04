# KMS-INVENTORY-ANALYSIS-PROJECT

## PROJECT TOPIC; Kultra Mega Stores (KMS) Inventory Analysis — SQL Project

## 🏢 Company Overview

Kultra Mega Stores (KMS), headquartered in Lagos, specializes in office supplies and furniture. Its customer base includes individual consumers, small businesses (retail), and large corporate clients (wholesale) across Lagos, Nigeria.

As part of my Data Analysis journey, I was engaged as a Business Intelligence Analyst to support the Abuja division of KMS. I received historical order data (2009–2012) and was tasked with analyzing the data to provide actionable business insights.

## 🛠 Objective

The project leverages advanced SQL analysis skills from my DSA Data Analysis training to uncover key insights on sales, profitability, customer segments, and operational efficiency for KMS.
![Screenshot (9)](https://github.com/user-attachments/assets/014b3290-3ac4-4d56-a2f6-440fe3fe0702)

### 📄 Case Scenarios & Business Questions Solved

#### ✅ Case Scenario I

1️⃣ Which product category had the highest sales?
Analyzed total sales across all product categories to identify top performers.

![Screenshot (8)](https://github.com/user-attachments/assets/4261a66d-bd76-46fe-a976-6bcb041bf084)
``` SQL

SELECT 
   Product_Category,
    SUM(Sales) AS TotalSales
FROM 
   [KMS Sales]
GROUP BY 
    Product_Category
ORDER BY 
    TotalSales DESC;
```
(PRODUCT CATEGORY SALES QUERZ)


2️⃣ What are the Top 3 and Bottom 3 regions in terms of sales?
Ranked regions to highlight strong and weak markets.

```SQL

SELECT TOP 3
    Region,
    SUM(Sales) AS TotalSales
FROM 
    [KMS Sales]
GROUP BY 
    Region
ORDER BY 
    TotalSales DESC;
```
```SQL

SELECT TOP 3
    Region,
    SUM(Sales) AS TotalSales
FROM 
    [KMS Sales]
GROUP BY 
    Region
ORDER BY 
    TotalSales ASC;
```

3️⃣ What were the total sales of appliances in Ontario?
Filtered product category and province to get precise sales insights.

4️⃣ Advice to management on increasing revenue from the bottom 10 customers
Provided actionable strategies to uplift engagement and purchasing among least active customers.

![Screenshot (10)](https://github.com/user-attachments/assets/2aa77885-2f2a-4849-a1c5-dc2e1f5d8bb5)
``` SQL

SELECT TOP 10
    Customer_Name,
    SUM(Sales) AS TotalSales
FROM 
    [KMS Sales]
GROUP BY 
    Customer_Name
ORDER BY 
    TotalSales ASC;
```

5️⃣ Which shipping method incurred the most shipping cost?
Analyzed aggregate shipping costs across different shipping modes to optimize logistics spending.

#### ✅ Case Scenario II

6️⃣ Who are the most valuable customers, and what products or services do they typically purchase?
Identified top customers by sales and analyzed their product preferences.

7️⃣ Which small business customer had the highest sales?
Focused analysis on the retail segment to find the top contributor.

8️⃣ Which corporate customer placed the most number of orders (2009–2012)?
Ranked corporate clients by order volume for targeted relationship management.



```SQL
SELECT TOP 1
    Customer_Name,
    COUNT(DISTINCT Order_ID) AS NumberOfOrders
FROM 
    [KMS Sales]
WHERE 
    Customer_Segment = 'Corporate'
    AND Order_Date >= '2009-01-01'
    AND Order_Date <= '2012-12-31'
GROUP BY 
    Customer_Name
ORDER BY 
    NumberOfOrders DESC;
```


9️⃣ Which consumer customer was the most profitable?
Ranked individual consumers by profitability to inform loyalty strategies.

🔟 Which customers returned items, and what segment do they belong to?
Analyzed returned orders to identify patterns by segment.

1️⃣1️⃣ Analysis of shipping methods vs. order priorities
Evaluated if shipping choices aligned appropriately with order priority, balancing speed and cost efficiency.

#### 💡 Key Skills Applied
	•	Advanced SQL querying and aggregation
	•	Window functions and subqueries
	•	Business insight generation
	•	Data cleaning and transformation (pre-processing)
	•	Customer and product segmentation

#### Personal Reflection

This project helped deepen my hands-on SQL analysis experience, translating complex business requirements into clear, data-driven insights. I enjoyed connecting operational data with strategic decision-making, and this strengthened my confidence in building data-driven recommendations for real businesses.


*💬 Note*

This repository showcases my individual learning journey and is meant for educational and portfolio demonstration purposes only.

*Let’s Connect!*

Feel free to reach out if you’d like to discuss the analysis in detail or collaborate on similar data projects!
