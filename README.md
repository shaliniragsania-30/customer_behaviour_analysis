# customer_behaviour_analysis
Data analytics project showcasing Customer Shopping Behaviour Analysis using Python, SQL and Power BI
Customer Shopping Behaviour Analysis
**Overview**
  This project analyses customer shopping behaviour using transactional data from 3,900 purchases across various product categories. The primary goal is to   uncover actionable insights into customer spending patterns, demographics, product preferences, and subscription behaviours to drive data-backed, strategic business decisions. 

**Dataset**
•	Rows: 3,900 
•	Columns: 18 

•	Key Features: 
* Demographics: Age, Gender, Location, Subscription Status 
o	Purchase Details: Item Purchased, Category, Purchase Amount, Season, Size, Colour 
o	Behavioural Data: Discount Applied, Shipping Type, Review Rating, Frequency of Purchases 
•	Data Quality: Handled 37 missing values found in the Review Rating column. 

**Tools Used**
•	Data Cleaning & Preprocessing: Python (Pandas) 
•	Database Management & Querying: MySQL Workbench / PostgreSQL 
•	Data Visualization & BI: Power BI 
•	Presentation & Reporting: Gamma App (AI Presentation Tool)

**Project Steps**
**1. Exploratory Data Analysis & Cleaning (Python)**
•	Data Assessment: Conducted structural evaluations using df.info() and statistical summaries via df.describe(). 
•	Missing Data Imputation: Imputed the 37 missing values in Review Rating using the median rating of each respective product category. 
•	Standardization: Converted all column names to standard snake_case for cleaner coding and documentation. 
•	Feature Engineering: * Created an age_group column to bin customers into logical age categories. 
o	Engineered a purchase_frequency_days metrics column. 
•	Redundancy Filter: Analyzed discount_applied and promo_code_used; dropped the redundant promo_code_used column. 

**2. Database Integration & SQL Analysise**
•	Connected the Python script directly to the SQL database engine and loaded the cleaned dataset. 
•	Executed targeted SQL business transactions to extract deep insights, including: 
o	Revenue distribution by gender and age groups. 
o	Profiling high-spending discount users. 
o	Customer segmentation into New, Returning, and Loyal buckets based on transaction history. 
o	Identifying item rankings and discount dependencies per product category. 

**3. Interactive Power BI Dashboard**
•	Imported the processed SQL tables into Power BI.
•	Built a comprehensive, dynamic tracking dashboard using multi-page architectures, high-level KPI cards, donut charts, and granular horizontal bar charts to map revenue and sales metrics visually. 

**4. Reporting & Presentation**
•	Synthesized project findings into a formal report.
•	Utilized Gamma AI to rapidly generate a professional client-ready presentation deck highlighting key charts, performance indicators, and business strategies.

**Dashboard Preview**
The interactive Power BI dashboard provides a bird's-eye view of key business performance indicators:
•	Top-Level Metrics: Displays 3.9K unique customers, a $59.76 average purchase amount, and a 3.75 average review rating.
•	Subscription Breakdown: Visualizes that 27% of customers are subscribers versus 73% non-subscribers.
•	Category Performance: Highlights Clothing and Accessories as the primary volume and revenue drivers.

**Key Results & Business Insights**
•	Demographic Drivers: Male shoppers generated significantly higher total revenue ($157,890) compared to female shoppers ($75,191) within this dataset. 
•	Age Contribution: "Young Adults" and "Middle-aged" cohorts lead total revenue generation, bringing in $62,143 and $59,197 respectively. 
•	Subscription Spending: While non-subscribers bring in higher overall revenue due to volume, the average spend between subscribers ($59.49) and non-subscribers ($59.87) remains neck-and-neck. 

**	Strategic Recommendations:**
o	Boost Subscriptions: Introduce premium, exclusive benefits to convert the high-volume 73% non-subscriber base. 
o	Loyalty Programs: Focus marketing retention plans on the 701 "Returning" customers to move them sustainably into the "Loyal" tier. 
o	Optimize Pricing: Evaluate discount limits on highly discount-dependent items like hats and sneakers to protect product profit margins. 

**How to Run**
Prerequisites
Ensure you have the following installed:
•	Python 3.8+ (with pandas and sqlalchemy libraries)
•	MySQL Server / PostgreSQL Engine
•	Power BI Desktop

**Execution File Path**
1.	Clean Data: Run the notebook file data_cleaning.ipynb to handle null values and extract engineered features. 
2.	Database Load: Execute the migration block at the bottom of the script to automatically host tables in your local SQL schema. 
3.	Run Queries: Open business_queries.sql inside your SQL workbench to view structural queries. 
4.	View Dashboard: Open shopping_behavior_dashboard.pbix using Power BI Desktop to interact with live dashboard slices. 
