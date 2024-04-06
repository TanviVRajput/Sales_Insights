# Sales_Insights Data Analysis Project

**Project Description:**

**Data Extraction and Transformation**

- Developed an ETL (Extract, Transform, Load) process using SQL to extract data from unstructured data sources.

- Transformed the extracted data and loaded it into a staging area to conduct data cleaning.

**Data Modeling**

- Designed a star schema data model using the cleaned and transformed data in the staging area.

- This data model provides a structured foundation to support efficient data analysis and visualization in Tableau.

**Data Visualization and Analysis**

- Utilized Tableau to develop a comprehensive dashboard for analyzing the sales performance of an India-based hardware company.

- The dashboard includes quantitative visualizations that provide valuable insights into the company's performance over time, considering various parameters that affect the business.

- The analysis and insights derived from the Tableau dashboard can help the company identify areas for improvement and inform strategic business decisions.

**About ATLIQ**

AtliQ Hardware is a company which supplies Computer Hardware and peripheral networking equipments to different clients.

**Software Used**

- MySQL

- Tableau

- Descriptive Statistics

**Problem Statement**

The key points are:

- The sales director needs to examine the sales data by state in India to pinpoint where sales are falling.

- With this information, the director can offer selective discounts or other measures to address the declining business in those specific states.

- This data-driven approach will help the struggling sales manager identify the root causes of the sales decline and take appropriate actions to improve performance.

**Sales insights:** 

Q1. Revenue breakdown by cities.

Q2. Revenue breakdown by years & months.

Q3. Top 5 customers by revenue & sales quantity.

Q4. Top 5 Products by revenue.

Q5. Net Profit & Profit Margin by Market.

**Aim of the Project**

**Unlocking Sales Insights**

- The goal was to uncover sales insights that were not readily visible before, in order to provide decision support for the sales team.
  
- By leveraging data analysis and automation, the aim was to reveal new, valuable insights that could guide the sales team's decision-making.

**Automating Data Gathering**

- The project involved automating the data gathering process, which previously required significant manual effort from the sales team.
  
- By automating the data collection and aggregation, the sales team could spend less time on manual data gathering and focus more on analyzing the insights and making informed decisions.

**Empowering the Sales Team**

- The unlocked sales insights, combined with the automated data gathering, were intended to empower the sales team with the information and tools they need to make more strategic and data-driven decisions.
  
- This approach aimed to enhance the sales team's decision support capabilities and improve the overall sales performance of the organization.

**Stake Holders:**

- Sales Team

- I.T Team

- Data & Analytics Team

**Outcome:**

- The automated dashboard aimed to empower the sales team with real-time, data-driven insights to inform their strategic decisions and actions.
  
- The goal was to develop an automated dashboard that would provide the latest and most relevant sales insights to support data-driven decision-making.

**Success Criteria:**

- Dashboards uncovering sales order insights with latest data available.

- Sales team able to take better decision & prove 10% cost savings of total spend.

- Sales analysts stop data gathering manually in order to save 20% of their business time & reinvest it in value added activity.

**Data Analysis Using SQL**

-- Show all customer records

SELECT * FROM customers;

-- Show total number of customers

SELECT COUNT(*) AS total_customers FROM customers;

-- Show transactions for Chennai market (market code for Chennai is Mark001)

SELECT * FROM transactions WHERE market_code = 'Mark001';

-- Show distinct product codes that were sold in Chennai.

SELECT DISTINCT product_code FROM transactions WHERE market_code = 'Mark001';

-- Show transactions where currency is US dollars.

SELECT * FROM transactions WHERE currency = 'USD';

-- Show transactions in 2020 join by date table.

SELECT transactions., date. FROM transactions INNER JOIN date ON transactions.order_date = date.date WHERE date.year = 2020;

-- Show total revenue in the year 2020.

SELECT SUM(transactions.sales_amount) AS total_revenue_2020 FROM transactions INNER JOIN date ON transactions.order_date = date.date WHERE date.year = 2020 AND (transactions.currency = 'INR' OR transactions.currency = 'USD');

-- Show total revenue in the year 2020, January Month.

SELECT SUM(transactions.sales_amount) AS total_revenue_jan_2020 FROM transactions INNER JOIN date ON transactions.order_date = date.date WHERE date.year = 2020 AND date.month_name = 'January' AND (transactions.currency = 'INR' OR transactions.currency = 'USD');


## **Tableau Dashboard : Key insights**

![Screenshot 2024-04-04 154852](https://github.com/TanviVRajput/Sales_Insights/assets/151743641/bec34981-3550-47fc-a533-45814a8a253b)


## **Recommendation**
* Should Maintain healthy relationship with the customers in Bhubaneshwar, Surat, Patna as they are highest profit % by market.

* Make some stategy for Bengaluru market as its revenue are less and also profit % are in negative.

* Figure out what need to be done as sales quantity in Kanpur, Bengaluru, Patna, Bhubaneshwar, Surat are the lowest.

* North zone have highest revenue contribution but lowest profit % whereas South zone have lowest revenue contribution but highest profit %. Try to increase customers in South zone.

* Delhi is the highest revenue contibutor and eightth highest profit contributor whereas Mumbai is the second highest revenue contributor and sixth highest profit contributor. So its need to be implement the same market strategy as in mumbai to increase the profit % in Delhi
