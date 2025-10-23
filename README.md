# Ecommerce Data Analysis by Theodosia Ndefru 
## Dataset from Kaggle 
## Data Summary : 
The dataset presents e-commerce transaction records, detailing a high volume of sales over a period from early 2020 to late 2022. 
Each entry records specific information, including a unique order ID, the state where the transaction took place, the customer's name, the date of the order, and the status of the order (e.g., Order, Processing, Shipped, Delivered). Crucially, the data lists the item purchased, its category (like Motherboard, CPU, Graphic Card, RAM), the brand, the unit cost and price, the quantity ordered, and the total monetary value of the transaction before and after tax. Finally, each record indicates an associate's name linked to the sale.

## Project Objectives 
- Identify which product categories generate the highest revenue 
- Determine profit margin per product category 
- Determine Sales Performance by region - Geographical Analysis
- Evaluate the efficiency or sales volume handled by each supervisor
- Analyze sales trends over time

## Data Analysis Process
## Data Cleaning 
Showcasing: 
- Handling Nulls
- Use of DISTINCT to check for duplicates.
- Checking Data types for consistency
- Use of REPLACE and CAST functions
## Data Analysis in HEX IDE
Showcasing:
- Aggregate Functions 
- Group By
- Order By 
- Date_trunc
  
## Link to SQL code in HEX 
- <a href="https://app.hex.tech/019982ef-3609-7007-adea-e89bd5734ac7/hex/E-commerce---Basic-SQL-Project-1-031MXKffs3fpNKoAtDkf0P/draft/logic">SQL queries

## Link to Dashboard in Tableau Public
- <a href="https://public.tableau.com/app/profile/theodosia.ndefru/viz/EcommerceDataViz_17611575808030/SupervisorSalesperyear">Ecommerce KPIs

## Insights from Analysis and Recommendations.
- The Data Entry Department needs to pay close attention to Data Entry flaws. Product Category "Motherboard" was entered as "Motherboard" in some instances and "MotherBoard" in other cases, making them look like two separate categories. This can lead to faulty results in analysis.
- The Product Category 'Monitors' accounted for most of the sales and 'Keyboards', the least consumed. Monitors were closely followed by CPUs. With the rise of AI and Machine Learning, massive computational power is required as Data Centers expand, hence the uptick in CPU purchases. The comapny should invest more in Monitors, CPUs, as well as Graphic cards which account for most of the sales in the computer accessory business.
- A consistent profit margin is observed across all product categories. This reflects a business model with a consistent Pricing and Markup structure, which may be good. However, there are lots of missed opportunities. This indicates that high-value products with high-demand are under-priced, leaving money on the table. Also, no drop in activity or sales during the COVID 19 Pandemic years raises eyebrows. The data presented shows no market volatility,supply chain issues, disruption in distribution channels, which were characteristic of the Pandemic period. It makes the data very questionable.
- Sales Volume by supervisor metric indicates that Aarvi Gupta did a phenomenal job in driving sales over the 3 years. Vijay Singh and Roshan Kumar had the best sales numbers in 2020 and 2021 respectively, but overall Aarvi Gupta took the lead. The comapny should consider promotions or awards to these sales people. 








