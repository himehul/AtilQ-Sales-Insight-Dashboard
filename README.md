
# AtliQ Hardware Sales Insights Dashboard



## Project Overview

AtliQ Hardware, a leading supplier of Computer Hardware & Peripherals across India, faced challenges in tracking sales due to the dynamic nature of the market. To address this, we initiated the AtliQ Sales Insights Dashboard project. The primary goal is to provide a comprehensive view of sales data, enabling the sales director and other stakeholders to make informed decisions in a rapidly evolving market.

## Aim's Grid

1. **Purpose:** The purpose of this project is to enhance sales tracking for AtliQ Hardware in response to the dynamic market conditions.
2. **Stakeholders:** The project involves collaboration with the sales director and other key stakeholders responsible for decision-making.
3. **End Result:** The end result is a powerful dashboard that visualizes key sales insights, enabling stakeholders to make data-driven decisions.
4. **Success Criteria:** The success of the project is measured by achieving a clear understanding of top-performing customers, products, and identifying opportunities for improvement.

## Data Analysis with SQL

### Step 1: Top Customer Analysis
- Identified MARKET004 (Delhi-NCR) as the top customer in terms of both total revenue and total sales.
#
  
![3](https://github.com/himehul/AtilQ-Sales-Insight-Dashboard/assets/139626006/6151cbbc-d2a4-4c2e-8018-c337f6adb6f5)
#
![5](https://github.com/himehul/AtilQ-Sales-Insight-Dashboard/assets/139626006/779a8bb8-15a7-41e2-8e9d-e7c28d7ca84c)

#
#



### Step 2: Most Revenue-Generating Product
- Discovered that the most revenue-generating product in Delhi-NCR is Prod316.

  #
![4](https://github.com/himehul/AtilQ-Sales-Insight-Dashboard/assets/139626006/04be5287-64db-4e29-92ba-c3b8e789597e)
#
#



### Step 3: Most Sold Product
- Identified Prod239 as the most sold product in Delhi-NCR.
#
  
![6](https://github.com/himehul/AtilQ-Sales-Insight-Dashboard/assets/139626006/1797c2bc-d1ab-44d5-8a5b-577cf5465e38)
#
#


### Step 4: Currency Analysis
- Noted discrepancies in currency flow, which needs to be addressed.
#
  
![7](https://github.com/himehul/AtilQ-Sales-Insight-Dashboard/assets/139626006/0ee85fab-4fbd-4467-bc32-4b7b1047eeac)
#
#


### Step 5: Finding the Cause of Currency Disparity
- Identified two distinct values for both INR and USD.

  #
-![9 ii](https://github.com/himehul/AtilQ-Sales-Insight-Dashboard/assets/139626006/e15ad45c-97f2-49a9-b62e-8b9ec53dd3ed)
#


- Resolved discrepancies in currency representation (e.g., INR/r) and decided to go with INR/r & USD/r.
#
  
- ![9 iii](https://github.com/himehul/AtilQ-Sales-Insight-Dashboard/assets/139626006/9f1b403b-a819-4df3-8d6b-f374691e95d9)
# 
![9 iv](https://github.com/himehul/AtilQ-Sales-Insight-Dashboard/assets/139626006/deb69124-3c8f-40bc-ba11-4c2b56c350a2)
#
- Planned to implement currency standardization in Power BI's Power Query.
#
#


  ### Step 6: Sales Overview
- Discovered that 2018 recorded the highest sales at Rs 41.43 Cr.
#
  
- ![8](https://github.com/himehul/AtilQ-Sales-Insight-Dashboard/assets/139626006/ae2b6a53-b0b0-403b-982d-360b6a9c6f72)

#
- Observed a declining trend in revenue since 2018, prompting further analysis in Power BI.
#
#

## Next Steps

The SQL analysis provided valuable insights, setting the stage for a more in-depth exploration using Power BI. The identified issues will be addressed, and the data will be further refined to ensure accurate and actionable insights.



# Creating Dashboard with Power BI

## Data Modeling

### 1. Understanding Tables:
   - Identified the Transaction table as the fact table, and Customers, Products, Date, and Markets as dimension tables.
   - Implemented a star schema model with four dimension tables connected to a single fact table.
  #
     
![1](https://github.com/himehul/AtilQ-Sales-Insight-Dashboard/assets/139626006/9b476a55-346e-46e4-935e-efcac39e7c94)
#
#


## Data Cleaning and ETL with Power Query Editor

### 2. Data Cleaning:
   - i) Removed null values from the Markets table.

#
   - ![2](https://github.com/himehul/AtilQ-Sales-Insight-Dashboard/assets/139626006/7c09f4e1-b073-4fdb-b47e-8aff8432a16d)
#

   - ii) Excluded 0 and -1 values from the sales amount in the Transaction table.
 # 
     
  ![2 ii](https://github.com/himehul/AtilQ-Sales-Insight-Dashboard/assets/139626006/d51afabd-3b26-4d04-9bb2-5a5cc9e67a57)
#



   - iii) Converted USD sales amounts to INR sales amounts for consistency.
#
     
![2 iii](https://github.com/himehul/AtilQ-Sales-Insight-Dashboard/assets/139626006/0e07e4d8-364a-4ed4-bdd9-2d6a7e9eec24)
#
#

3. **Currency Standardization:**
   - Retained only INR/r and USD/r, ensuring consistency in the model.
#

   - ![3](https://github.com/himehul/AtilQ-Sales-Insight-Dashboard/assets/139626006/900d5848-7e4c-4e8b-8b9b-6f99bae3c3c6)

#
#


## Dashboard Building

### 4. Measures Creation:
   - i) Created the "Revenue" measure: SUM('sales transactions'[norm_sales_amount]).
   - ii) Created the "Sales Quantity" measure: SUM('sales transactions'[sales_qty]).
#

![4](https://github.com/himehul/AtilQ-Sales-Insight-Dashboard/assets/139626006/7ed73259-79db-4b58-b088-437601b222f9)


   - Total Revenue: 984.7 M; Total Sales Quantity: 2M.

#
#
### 5. Revenue Analysis by Market:
   - Added visuals for Revenue by Market and Sales Quantity by Market.
   - Identified Delhi NCR as the top-performing region in both revenue and sales, consistent with previous SQL findings.
#

![5](https://github.com/himehul/AtilQ-Sales-Insight-Dashboard/assets/139626006/8b05bc50-9824-445d-a6d1-3d7d0165a53c)
#
#

### 6. Top 5 Customers and Products:
   - Showcased the top 5 customers and products based on revenue.
   - Top Customer: Electricalsara Store (Revenue: 413.33 M).
   - Top Product: Prod040 (Revenue: 23.58 M).
  
    # 
![7](https://github.com/himehul/AtilQ-Sales-Insight-Dashboard/assets/139626006/6a8171ac-9e71-4c05-9e13-70c84eae7dd8)
#
#


### 7. Revenue Trend Line Chart:
   - Created a trend line chart to visualize the revenue trend over time.
#

   - ![6](https://github.com/himehul/AtilQ-Sales-Insight-Dashboard/assets/139626006/b46cd6cd-f7ff-45f4-9f4d-fa63f12e835f)

#
#

## Conclusion Analysis


### 8. Overall Revenue Trend:
   - Observed a declining trend in overall revenue.
  
     #
  ![8 i](https://github.com/himehul/AtilQ-Sales-Insight-Dashboard/assets/139626006/d6a4d2c7-c6a8-4772-81ef-8050773d51f8)
#
   - ![8 i 2](https://github.com/himehul/AtilQ-Sales-Insight-Dashboard/assets/139626006/bb6b359f-d30f-4129-8105-54a06adc8e6e)
#
   - Noted a significant drop from around 42.50M in revenue in 2018 1st Quarter to 14.71M in 2020 2nd Quarter, indicating a 65% decline.
#
#
#
#
**Possible Reasons for Decline:**
   - 1) **Impact of Covid-19:** The decline in 2020 could be attributed to the pandemic.
   - 2) **Change in Product Quality:** Shifts in product quality might have affected customer satisfaction.
   - 3) **Promotions/Advertisements:** Lack of effective promotions or advertising strategies.
   - 4) **Discounts:** Competitor discounts impacting sales.
   - 5) **Customer Service Issues:** A decline in the quality of customer service or responsiveness could result in dissatisfied customers, leading to reduced repeat business and negative word-of-mouth.
 #   

**Possible Ways to Overcoming this Decline in Revenue:**

1. **Enhance Product Quality:**
   - Invest in rigorous quality assurance and product development to ensure that the offered products meet or exceed customer expectations. Communicate improvements in product quality through marketing channels to rebuild trust and attract discerning customers.

2. **Strategic Marketing and Promotion:**
   - Develop a targeted marketing strategy that highlights the unique selling points of AtliQ Hardware's products. Utilize digital marketing, social media, and other channels to increase brand visibility. Consider promotions and discounts to attract new customers and retain existing ones.

3. **Customer Relationship Management (CRM):**
   - Strengthen customer relationships by investing in CRM systems and practices. Engage with customers for feedback, address concerns promptly, and personalize interactions to build long-term loyalty. A satisfied customer base is more likely to repeat purchases and recommend the brand to others.
    #
     #
   ![PBI](https://github.com/himehul/AtilQ-Sales-Insight-Dashboard/assets/139626006/ade8eb99-4231-4e43-a1b2-e17e674f837a)

   #
   
   #   
This comprehensive Power BI dashboard provides valuable insights into sales performance, enabling stakeholders to delve deeper into the reasons behind the decline and strategize accordingly. Further analysis and exploration can uncover actionable steps to revitalize AtliQ Hardware's revenue trajectory.

