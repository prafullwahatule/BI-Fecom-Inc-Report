# 📊 Fecom Inc – Power BI Business Intelligence Report

This **Power BI project** delivers a comprehensive **Business Intelligence (BI) Report** for **Fecom Inc**, consolidating insights across **sales, customers, products, sellers, payments, reviews,** and **geographic data**.  

The dashboard empowers business users and decision-makers to **analyze trends, track revenue, monitor customer behavior, evaluate seller and product performance, and make data-driven strategic decisions**.

---

## 📌 Problem Statement

In a modern e-commerce marketplace, companies face multiple challenges:

- **Fragmented or messy data** across orders, customers, sellers, and products.  
- Difficulty in **tracking customer behavior, product performance, and seller efficiency**.  
- Limited visibility into **revenue trends, payments, and installment patterns**.  
- Challenges in **analyzing customer feedback** to improve products, services, and delivery experience.  

This project solves these issues by creating a **clean, structured dataset** integrated into a **relational database** and a **Power BI dashboard**, enabling actionable business insights.

---

## 📝 Project Overview

The **Fecom Inc BI Report** is a **data-driven analytical tool** that consolidates multiple datasets and visualizes key business metrics interactively.  

Key highlights include:

- **Data Wrangling:**  
  Cleaning, transforming, and enhancing datasets by removing irrelevant columns and adding analytical fields such as `Age Group`, `Total Item Cost`, `Installment Flag`, and `Rating Category`.

- **Database Design & ER Diagram:**  
  A relational model connecting **customers, orders, products, sellers, payments, and reviews** to ensure data integrity and support comprehensive analytics.

- **Dashboards & Insights:**  
  Power BI dashboards provide insights across several domains:

  - **Overview:** Total Orders, Revenue, Customers, Sellers, Average Rating, On-Time Delivery %.  
  - **Products:** Product catalog performance, shipping costs, delivery times, top and bottom performers.  
  - **Vendors:** Seller revenue, top sellers, quantity sold, geographic distribution, category-wise performance.  
  - **Customers:** Active customers, demographic insights, top revenue-generating customers, city-wise distribution.  
  - **Revenue:** Total revenue, revenue per order, payment method analysis, installment tracking.  
  - **Feedback:** Customer ratings, review count, positive/negative feedback analysis, category-wise sentiment.

- **Geospatial Analysis:**  
  Linking customers and sellers with geographic coordinates to visualize regional performance and market penetration.

---

## 🎯 Project Objectives

1. **Clean & Prepare Data:**  
   Ensure datasets are accurate, consistent, and ready for analysis by removing duplicates and irrelevant fields.

2. **Integrate Multiple Tables:**  
   Build a relational database connecting `Customers`, `Orders`, `Order_Items`, `Products`, `Sellers`, `Payments`, and `Reviews`.

3. **Deliver Actionable Insights:**  
   Track KPIs, trends, and patterns to monitor business performance and operational efficiency.

4. **Improve Customer Understanding:**  
   Analyze behavior, demographics, and feedback to enhance customer satisfaction and retention.

5. **Evaluate Products & Sellers:**  
   Identify top-performing products and sellers, underperforming items, and potential growth opportunities.

6. **Visualize Data Professionally:**  
   Create interactive dashboards for **easy, professional, and insightful visualization** of all key metrics.

7. **Support Strategic Decision-Making:**  
   Enable forecasting, trend analysis, and operational planning to optimize marketplace growth.


---
---

## 🗄️ Project Data Tables

This section provides a detailed overview of all the data tables used in the project, along with column names and their purpose.  


### 1. Di_Customer_List

| Sr. No | Column Name         | Purpose / Description                     |
|--------|-------------------|------------------------------------------|
| 1      | Customer_Trx_ID    | Unique customer transaction              |
| 2      | Subscriber_ID      | Unique subscriber ID                     |
| 3      | Subscribe_Date     | Customer subscription date               |
| 4      | First_Order_Date   | Date of first order                       |
| 5      | Customer_Postal_Code | Postal code of customer                  |
| 6      | Customer_City      | Customer city                             |
| 7      | Customer_Country   | Customer country                          |
| 8      | Customer_Country_Code | Country ISO code                        |
| 9      | Age                | Customer age                              |
| 10     | Gender             | Customer gender                           |

**Description:** This table contains detailed information about each customer, including demographics, location, and subscription details. It is mainly used for customer-level analysis and segmentation.  


### 2. Di_Geolocations

| Sr. No | Column Name       | Purpose / Description                                 |
|--------|-----------------|-------------------------------------------------------|
| 1      | Geo_Postal_Code  | Postal/ZIP code, useful for mapping or grouping areas|
| 2      | Geo_Lat          | Latitude for geographic visualization                 |
| 3      | Geo_Lon          | Longitude for geographic visualization                |
| 4      | Geolocation_City | City corresponding to postal code                     |
| 5      | Geo_Country      | Country name for comparison and filtering            |

**Description:** Contains geographic coordinates and location information used for mapping, regional analysis, and visualizing customer/seller distribution.  


### 3. Order_Items

| Sr. No | Column Name           | Purpose / Description                                       |
|--------|----------------------|-------------------------------------------------------------|
| 1      | Order_ID             | Unique ID for each order, links with other tables          |
| 2      | Order_Item_ID        | Item number within an order                                  |
| 3      | Product_ID           | Unique product identifier                                    |
| 4      | Seller_ID            | Unique seller ID, used for seller analysis                  |
| 5      | Shipping_Limit_Date  | Latest shipping date allowed                                 |
| 6      | Price                | Selling price of the product                                  |
| 7      | Freight_Value        | Shipping cost                                                |

**Description:** Contains item-level details of all orders, linking products to sellers and tracking pricing and shipping costs.  


### 4. Order_Payments

| Sr. No | Column Name          | Purpose / Description                                         |
|--------|--------------------|---------------------------------------------------------------|
| 1      | Order_ID            | Links payment to order                                       |
| 2      | Payment_Sequential  | Payment attempt number (1 = first attempt)                  |
| 3      | Payment_Type        | Payment method (credit card, voucher, etc.)                 |
| 4      | Payment_Installments | Number of installments selected                               |
| 5      | Payment_Value       | Total payment made                                           |

**Description:** Tracks payment details for each order, including method, installments, and payment amounts, used for revenue analysis.  


### 5. Order_Reviews

| Sr. No | Column Name                   | Purpose / Description                                     |
|--------|-------------------------------|-----------------------------------------------------------|
| 1      | Review_ID                     | Unique ID of the review                                   |
| 2      | Order_ID                      | Linked order for the review                               |
| 3      | Review_Score                  | Rating given by customer (1–5)                            |
| 4      | Review_Comment_Title_En       | Short title of review                                     |
| 5      | Review_Comment_Message_En     | Full review message                                       |
| 6      | Review_Creation_Date          | Date of review submission                                  |
| 7      | Review_Answer_Timestamp       | Timestamp of seller response                                |

**Description:** Stores customer feedback and ratings for orders. Used to analyze satisfaction, trends, and seller response times.  


### 6. Orders

| Sr. No | Column Name                   | Purpose / Description                                     |
|--------|-------------------------------|-----------------------------------------------------------|
| 1      | Order_ID                      | Unique order ID                                           |
| 2      | Customer_Trx_ID               | Customer who placed the order                             |
| 3      | Order_Status                  | Current order state (delivered, shipped, etc.)            |
| 4      | Order_Purchase_Timestamp      | Exact date & time of purchase                             |
| 5      | Order_Approved_At             | Date & time payment was approved                          |
| 6      | Order_Delivered_Carrier_Date  | Date & time seller dispatched                              |
| 7      | Order_Delivered_Customer_Date | Date & time customer received the product                  |
| 8      | Order_Estimated_Delivery_Date | Expected delivery date                                      |

**Description:** Contains general order-level information for tracking the lifecycle, status, and timestamps of each order.  


### 7. Di_Products

| Sr. No | Column Name            | Purpose / Description                                       |
|--------|-----------------------|-------------------------------------------------------------|
| 1      | Product_ID            | Unique product identifier                                   |
| 2      | Product_Category_Name | Category of the product                                     |
| 3      | Product_Weight_Gr     | Weight in grams                                            |
| 4      | Product_Length_Cm     | Length in centimeters                                      |
| 5      | Product_Height_Cm     | Height in centimeters                                      |
| 6      | Product_Width_Cm      | Width in centimeters                                       |

**Description:** Stores product information including category, weight, and dimensions, used for product-level analysis and logistics calculations.  


### 8. Di_Sellers_List

| Sr. No | Column Name       | Purpose / Description                                       |
|--------|-----------------|-------------------------------------------------------------|
| 1      | Seller_ID        | Unique seller identifier                                    |
| 2      | Seller_Name      | Name of the seller                                         |
| 3      | Seller_Postal_Code | Postal code of seller                                     |
| 4      | Seller_City      | City of seller                                             |
| 5      | Country_Code     | ISO code of seller country                                  |
| 6      | Seller_Country   | Full name of seller country                                 |

**Description:** Contains seller details including location and country information, used for seller-level analysis and mapping.

---
---

## 🚀 Power BI Report Planning

This table summarizes all pages of the Power BI dashboard along with their purpose.  

| Page No | Page Name         | Purpose                                                                 |
|--------|------------------|-------------------------------------------------------------------------|
| 1      | 🏠 Home             | Serves as the entry page with project name, logo, and navigation buttons|
| 2      | 📈 Overview         | Provides high-level metrics and trends: Total Orders, Revenue, Avg. Rating|
| 3      | 📦 Products         | Analyzes product performance: top products and category-wise sales      |
| 4      | 🧾 Sellers / Vendors| Evaluates seller performance: revenue, sales trends, top sellers        |
| 5      | 👥 Customers        | Understands customer behavior: location, avg order value, demographics  |
| 6      | 💳 Revenue          | Tracks revenue, payment methods, refunds, and monthly financial trends  |
| 7      | ⭐ Feedback         | Analyzes customer ratings and feedback, including average rating and sentiment|

---

## 🧹 Data Cleaning Steps

This section documents the **data cleaning process** applied to the project tables.  
Each table lists the steps applied, their effect on rows and columns, and the purpose of each transformation to ensure **accurate, consistent, and analysis-ready data**.




### 1. Customer_List Table

The **Customer_List** table contains detailed information about each customer, including demographics, location, and subscription data.  
The cleaning process ensures duplicates, errors, and unnecessary columns are handled, with added segmentation via `Age Group`.

| Sr. No | Applied Step           | Target Column          | Rows Before | Rows After | Effect (Rows) | Columns Before | Columns After | Effect (Columns) |
|--------|----------------------|----------------------|------------|-----------|---------------|----------------|---------------|-----------------|
| 0      | Load CSV File         | -                    | 102727     | 102727    | 0             | 10             | 10            | 0               |
| 1      | Remove Errors         | -                    | 102727     | 102727    | 0             | 10             | 10            | 0               |
| 2      | Remove Blank Rows     | -                    | 102727     | 102727    | 0             | 10             | 10            | 0               |
| 3      | Remove Duplicates     | -                    | 102727     | 102727    | 0             | 10             | 10            | 0               |
| 4      | Remove Duplicates     | Customer_Trx_ID      | 102727     | 99442     | 3285          | 10             | 10            | 0               |
| 5      | Remove Blank Rows     | Customer_Trx_ID      | 99442      | 99441     | 1             | 10             | 10            | 0               |
| 6      | Remove Column         | Subscriber_ID        | 99441      | 99441     | 0             | 10             | 9             | 1               |
| 7      | Remove Column         | Customer_Country_Code| 99441      | 99441     | 0             | 9              | 8             | 1               |
| 8      | Add Column            | Age Group            | 99441      | 99441     | 0             | 8              | 9             | 1               |

**Summary:**  
The table was cleaned by removing duplicates, blank rows, and unnecessary columns, while adding the `Age Group` column for segmentation.  
The final dataset is **clean, consistent, and ready for analysis**.

---

### 2. Geolocations Table

The **Geolocations** table contains geographic information (postal codes, latitude, longitude, city, country) for mapping and regional analysis.  
Cleaning ensures the dataset contains only **unique, valid, and usable geographic records**.

| Sr. No | Applied Step       | Target Column   | Rows Before | Rows After | Effect (Rows) | Columns Before | Columns After | Effect (Columns) |
|--------|------------------|----------------|------------|-----------|---------------|----------------|---------------|-----------------|
| 0      | Load CSV File     | -              | 1,000,163  | 1,000,163 | 0             | 5              | 5             | 0               |
| 1      | Remove Errors     | -              | 1,000,163  | 1,000,163 | 0             | 5              | 5             | 0               |
| 2      | Remove Blank Rows | -              | 1,000,163  | 1,000,163 | 0             | 5              | 5             | 0               |
| 3      | Remove Duplicates | -              | 1,000,163  | 1,686     | 998,477       | 5              | 5             | 0               |
| 4      | Remove Top Row    | -              | 1,686      | 1,685     | 1             | 5              | 5             | 0               |

**Summary:**  
This table was cleaned by removing duplicates and the top row to ensure **unique, high-quality geographic data** suitable for mapping, linking to customers/sellers, and regional analysis.

---

### 3. Order_Items Table

The **Order_Items** table contains item-level details of customer orders, including products, sellers, and pricing.  
Cleaning ensures duplicates are removed and relevant columns are retained, with calculated fields added for analysis.

| Sr. No | Applied Step       | Target Column     | Rows Before | Rows After | Effect (Rows) | Columns Before | Columns After | Effect (Columns) |
|--------|------------------|-----------------|------------|-----------|---------------|----------------|---------------|-----------------|
| 0      | Load CSV File     | -               | 112650     | 112650    | 0             | 7              | 7             | 0               |
| 1      | Remove Errors     | -               | 112650     | 112650    | 0             | 7              | 7             | 0               |
| 2      | Remove Blank Rows | -               | 112650     | 112650    | 0             | 7              | 7             | 0               |
| 3      | Remove Duplicates | -               | 112650     | 112650    | 0             | 7              | 7             | 0               |
| 4      | Remove Duplicates | Order_ID        | 112650     | 98666     | 13984         | 7              | 7             | 0               |
| 5      | Remove Column     | Order_Item_ID   | 98666      | 98666     | 0             | 7              | 6             | 1               |
| 6      | Add Column        | Total Item Cost | 98666      | 98666     | 0             | 6              | 7             | 1               |

**Summary:**  
Duplicates were removed, unnecessary columns were dropped, and a **Total Item Cost** column was added.  
The table is now clean and ready for **product-level revenue and performance analysis**.

---

### 4. Order_Payments Table

The **Order_Payments** table contains payment-related details for orders, including payment type, value, and installments.  
Cleaning ensures the table is accurate and includes flags for analysis.

| Sr. No | Applied Step       | Target Column        | Rows Before | Rows After | Effect (Rows) | Columns Before | Columns After | Effect (Columns) |
|--------|------------------|-------------------|------------|-----------|---------------|----------------|---------------|-----------------|
| 0      | Load CSV File     | -                 | 103886     | 103886    | 0             | 5              | 5             | 0               |
| 1      | Remove Errors     | -                 | 103886     | 103886    | 0             | 5              | 5             | 0               |
| 2      | Remove Blank Rows | -                 | 103886     | 103886    | 0             | 5              | 5             | 0               |
| 3      | Remove Duplicates | -                 | 103886     | 103886    | 0             | 5              | 5             | 0               |
| 4      | Remove Column     | Payment_Sequential | 103886     | 103886    | 0             | 5              | 4             | 1               |
| 5      | Add Column        | Installment Flag  | 103886     | 103886    | 0             | 4              | 5             | 1               |

**Summary:**  
Unnecessary columns were removed and a **Installment Flag** column was added to facilitate **financial and payment pattern analysis**.

---

### 5. Order_Reviews Table

The **Order_Reviews** table stores customer feedback, ratings, and comments for orders.  
Cleaning removes invalid or empty entries, drops irrelevant columns, and adds a classification column for analysis.

| Sr. No | Applied Step               | Target Column               | Rows Before | Rows After | Effect (Rows) | Columns Before | Columns After | Effect (Columns) |
|--------|---------------------------|----------------------------|------------|-----------|---------------|----------------|---------------|-----------------|
| 0      | Load CSV File             | -                          | 99329      | 99329     | 0             | 7              | 7             | 0               |
| 1      | Remove Errors             | -                          | 99329      | 99327     | 2             | 7              | 7             | 0               |
| 2      | Remove Blank Rows         | -                          | 99327      | 99268     | 59            | 7              | 7             | 0               |
| 3      | Remove Duplicates         | -                          | 99268      | 99268     | 0             | 7              | 7             | 0               |
| 4      | Remove Empty String       | Order_ID                   | 99268      | 99223     | 45            | 7              | 7             | 0               |
| 5      | Remove Empty String       | Review_Creation_Date       | 99223      | 99221     | 2             | 7              | 7             | 0               |
| 6      | Remove Column             | Review_Comment_Message_En  | 99221      | 99221     | 0             | 7              | 6             | 1               |
| 7      | Remove Column             | Review_Comment_Title_En    | 99221      | 99221     | 0             | 6              | 5             | 1               |
| 8      | Remove Column             | Review_Answer_Timestamp    | 99221      | 99221     | 0             | 5              | 4             | 1               |
| 9      | Add Column                | Rating Category            | 99221      | 99221     | 0             | 4              | 5             | 1               |

**Summary:**  
The table was cleaned by removing errors, blank rows, duplicates, and unnecessary columns.  
The **Rating Category** column was added to facilitate **customer sentiment and feedback analysis**.

---

### 6. Orders Table

The **Orders** table contains order-level details, including customer, order status, timestamps, and delivery information.  
Cleaning removes unnecessary columns, handles errors, and calculates delivery time for analysis.

| Sr. No | Applied Step                        | Target Column                  | Rows Before | Rows After | Effect (Rows) | Columns Before | Columns After | Effect (Columns) |
|--------|-----------------------------------|-------------------------------|------------|-----------|---------------|----------------|---------------|-----------------|
| 0      | Load CSV File                       | -                             | 99441      | 99441     | 0             | 8              | 8             | 0               |
| 1      | Remove Errors                       | -                             | 99441      | 99441     | 0             | 8              | 8             | 0               |
| 2      | Remove Blank Rows                    | -                             | 99441      | 99441     | 0             | 8              | 8             | 0               |
| 3      | Remove Duplicates                    | -                             | 99441      | 99441     | 0             | 8              | 8             | 0               |
| 4      | Remove Column                        | Order_Approved_At             | 99441      | 99441     | 0             | 8              | 7             | 1               |
| 5      | Remove Column                        | Order_Delivered_Carrier_Date  | 99441      | 99441     | 0             | 7              | 6             | 1               |
| 6      | Add Column                           | Delivery Time (Days)          | 99441      | 99441     | 0             | 6              | 7             | 1               |
| 7      | Remove Errors                        | Delivery Date After Plot       | 99441      | 96476     | 2965          | 7              | 7             | 0               |

**Summary:**  
The Orders table was cleaned by removing irrelevant columns and errors, and a **Delivery Time (Days)** column was added for **order fulfillment and delivery analysis**.

---

### 7. Products Table

The **Products** table contains product-level details such as category, dimensions, and weight.  
Cleaning ensures invalid or zero-value entries are removed, and a **Volume** column is added for analysis.

| Sr. No | Applied Step                     | Target Column         | Rows Before | Rows After | Effect (Rows) | Columns Before | Columns After | Effect (Columns) |
|--------|--------------------------------|---------------------|------------|-----------|---------------|----------------|---------------|-----------------|
| 0      | Load CSV File                    | -                   | 32951      | 32951     | 0             | 6              | 6             | 0               |
| 1      | Remove Errors                    | -                   | 32951      | 32951     | 0             | 6              | 6             | 0               |
| 2      | Remove Blank Rows                 | -                   | 32951      | 32951     | 0             | 6              | 6             | 0               |
| 3      | Remove Duplicates                 | -                   | 32951      | 32951     | 0             | 6              | 6             | 0               |
| 4      | Remove Empty String               | Product_Weight_Gr   | 32951      | 32949     | 2             | 6              | 6             | 0               |
| 5      | Remove Top 4 Zero Rows            | Product_Weight_Gr   | 32949      | 32945     | 4             | 6              | 6             | 0               |
| 6      | Add Column                        | Volume (cm³)        | 32945      | 32945     | 0             | 6              | 7             | 1               |

**Summary:**  
The table was cleaned by removing errors, blank rows, duplicates, and invalid weight entries.  
A **Volume (cm³)** column was added for **logistics, shipping, and dimensional analysis**.

---

### 8. Sellers_List Table

The **Sellers_List** table contains seller information such as location and country.  
Cleaning removes unnecessary columns to ensure a concise and accurate dataset.

| Sr. No | Applied Step       | Target Column   | Rows Before | Rows After | Effect (Rows) | Columns Before | Columns After | Effect (Columns) |
|--------|------------------|----------------|------------|-----------|---------------|----------------|---------------|-----------------|
| 0      | Load CSV File     | -              | 3095       | 3095      | 0             | 6              | 6             | 0               |
| 1      | Remove Errors     | -              | 3095       | 3095      | 0             | 6              | 6             | 0               |
| 2      | Remove Blank Rows | -              | 3095       | 3095      | 0             | 6              | 6             | 0               |
| 3      | Remove Duplicates | -              | 3095       | 3095      | 0             | 6              | 6             | 0               |
| 4      | Remove Column     | Country_Code   | 3095       | 3095      | 0             | 6              | 5             | 1               |

**Summary:**  
The Sellers_List table was cleaned by removing unnecessary columns for **concise seller-level analysis** and accurate reporting.

---
---

## 🗂 Finalized Columns – Project Tables

This section lists the **final columns** in each table after data cleaning, transformation, and addition of calculated fields.  
These columns are used for reporting, analysis, and visualization in the project.

---

### 1. Di_Customer_List
The `Di_Customer_List` table contains customer-related information including demographics, location, and subscription details.  
**Final Columns:**
- Customer ID  
- Subscription Date  
- First Order Date  
- City  
- Country  
- Postal Code  
- Age  
- Gender  
- Age Group  

---

### 2. Di_Geolocations
The `Di_Geolocations` table stores geographic information for mapping and regional analysis.  
**Final Columns:**
- Postal Code  
- Latitude  
- Longitude  
- City  
- Country  

---

### 3. Order_Items
The `Order_Items` table contains item-level details for each order, including pricing and logistics.  
**Final Columns:**
- Order ID  
- Product ID  
- Seller ID  
- Item Price  
- Shipping Cost  
- Shipping Deadline  
- Total Item Cost  

---

### 4. Order_Payments
The `Order_Payments` table captures payment information for orders.  
**Final Columns:**
- Order ID  
- Payment Method  
- Installments  
- Payment Amount  
- Installment Flag  

---

### 5. Order_Reviews
The `Order_Reviews` table stores customer feedback and ratings for each order.  
**Final Columns:**
- Review ID  
- Order ID  
- Rating  
- Review Date  
- Rating Category  

---

### 6. Orders
The `Orders` table contains order-level information for tracking order status and delivery.  
**Final Columns:**
- Order ID  
- Customer ID  
- Status  
- Order Date  
- Delivery Date  
- Estimated Delivery Date  

---

### 7. Di_Products
The `Di_Products` table stores product-specific information for analysis of category, weight, and dimensions.  
**Final Columns:**
- Product ID  
- Category  
- Weight (g)  
- Length (cm)  
- Height (cm)  
- Width (cm)
- Volume (cm²)

---

### 8. Di_Sellers_List
The `Di_Sellers_List` table contains information about sellers including location details for geographic analysis.  
**Final Columns:**
- Seller ID  
- Seller Name  
- City  
- Country  
- Postal Code  

---
---

## 🗺 ER Diagram – Project Database Structure

The **Entity-Relationship (ER) Diagram** provides a visual representation of the database design for the project.  
It shows how different tables are related to each other and defines the **structure, relationships, and data flow** across the system.

**Diagram:**
<img width="1637" height="842" alt="Data Modeling" src="https://github.com/user-attachments/assets/202be2a6-0f0a-4e9c-9c51-e63331ced69a" />

### Key Highlights:

- **Customer-Centric Design:**  
  The `Di_Customer_List` table is linked to the `Orders` table via `Customer ID`, enabling tracking of all orders placed by a customer.

- **Order and Item Relationship:**  
  The `Orders` table connects to `Order_Items`, capturing item-level details for each order. This allows analysis of individual products within an order.

- **Payment Tracking:**  
  The `Order_Payments` table is linked to `Orders` via `Order ID` to monitor payment method, installments, and payment amounts for each order.

- **Feedback Management:**  
  The `Order_Reviews` table is associated with `Orders` through `Order ID` and stores customer ratings and reviews, enabling sentiment and satisfaction analysis.

- **Product and Seller Analysis:**  
  The `Order_Items` table links to `Di_Products` (via `Product ID`) and `Di_Sellers_List` (via `Seller ID`), providing insights on product performance and seller behavior.

- **Geographic Mapping:**  
  `Di_Customer_List` and `Di_Sellers_List` link to `Di_Geolocations` via `Postal Code` for geographic visualization and regional analysis.

- **Normalization and Efficiency:**  
  The ER diagram ensures **minimal redundancy** by separating entities into dedicated tables while maintaining **clear foreign key relationships** for analytical queries.

### Purpose:
The ER diagram helps developers, analysts, and stakeholders **understand the database structure**, relationships between entities, and enables **efficient querying, reporting, and dashboard creation** in Power BI.

---
---

## 🧰 Data Wrangling

The Data Wrangling phase focused on **cleaning**, **transforming**, and **enhancing** the datasets to ensure accuracy, consistency, and analytical usefulness.  
Unnecessary fields were removed, and meaningful calculated columns were added to support deeper insights and reporting.

---

## 🔥 1. Columns Removed

To reduce noise and keep only meaningful information, the following columns were removed from each table:

### **🗂 Customer_List**
- Subscriber_ID  
- Customer_Country_Code  

### **📦 Order_Items**
- Order_Item_ID  

### **💳 Order_Payments**
- Payment_Sequential  

### **⭐ Order_Reviews**
- Review_Comment_Message_En  
- Review_Comment_Title_En  
- Review_Answer_Timestamp  

### **📜 Orders**
- Order_Approved_At  
- Order_Delivered_Carrier_Date  

### **🏪 Sellers_List**
- Country_Code  

These fields were removed because they were **irrelevant**, **duplicate**, or **not required** for business analysis.

---

## 🌱 2. Columns Added

New calculated fields were created to improve segmentation, cost calculation, and rating analysis.

### **🗂 Customer_List**
- **Age Group** → Categorizes customers into ranges (18–25, 26–35, 36–45, etc.) for demographic insights.

### **📦 Order_Items**
- **Total Item Cost** → Calculated as *(Item Price + Shipping Cost)* to determine final cost per item.

### **💳 Order_Payments**
- **Installment Flag** → Indicates whether the payment was made in **installments** or **full**.

### **⭐ Order_Reviews**
- **Rating Category** → Converts numeric rating into descriptive categories:
  - Poor  
  - Average  
  - Good  
  - Excellent  

---

## 🎯 Summary

The Data Wrangling process helped in:

- Removing irrelevant or duplicate fields  
- Improving dataset clarity and usability  
- Creating powerful analytical columns  
- Preparing the data for modeling, dashboards, and insights  

This ensures the final dataset is **clean**, **optimized**, and **analysis-ready**.

---
---


## 🏠 Home Page – Overview & Navigation

The **Home Page** serves as the **introductory interface** for the project.  
It provides users with a **quick overview of the platform**, brand identity, and access to all other sections through clear navigation.

**Screenshot:**  
<img width="1409" height="794" alt="Home" src="https://github.com/user-attachments/assets/ae2cd59f-747f-4c40-983d-492555517f90" />


### 🔑 Key Features

- **Project Branding:**  
  Displays the project **name and logo**, reinforcing brand identity and professional appearance.

- **Navigation Buttons:**  
  Provides **easy access** to all key pages such as Overview, Product, Vendor, Customer, Revenue, Feedback, and Reports.  

- **User-Friendly Interface:**  
  Designed for **intuitive interaction**, ensuring users can quickly find desired sections without confusion.


### 🎯 Summary

The **Home Page** acts as the **central hub** for the dashboard, helping users:  

- Recognize the project visually through logo and branding  
- Navigate seamlessly to all pages and modules  
- Understand the purpose and scope of the platform at a glance  

This ensures the first impression is **professional, clean, and easy to use**.

---

## 📊 Overview – KPI & Chart Insights

The **Overview Page** provides a **high-level summary of the platform's performance**, combining KPIs and visualizations to enable quick insights into orders, revenue, customers, sellers, and operational efficiency.

**Screenshot:**  
<img width="1407" height="789" alt="Overview" src="https://github.com/user-attachments/assets/7c364c6f-662b-4bf0-8190-06bdc4fdca4d" />


### 🔑 Key KPIs

| Sr. No | KPI Name                | Insight |
|--------|------------------------|---------|
| 1      | Total Orders Completed  | Shows how many orders were successfully delivered. A higher number reflects strong customer demand and good overall marketplace activity. |
| 2      | Total Revenue           | Indicates the total money earned from all orders. Helps measure business growth, profitability, and monthly/seasonal performance. |
| 3      | Total Customers         | Represents how many unique customers purchased from the platform. An increasing count shows successful customer acquisition and market expansion. |
| 4      | Total Sellers           | Shows the number of active sellers. More sellers indicate a wider product range and a healthier marketplace ecosystem. |
| 5      | Average Rating          | Reflects overall customer satisfaction based on product and delivery reviews. A higher rating indicates better product quality and service experience. |
| 6      | On-Time Delivery %      | Shows the percentage of orders delivered on or before the estimated delivery date. Higher values indicate efficient logistics and improved customer experience. |


### 📈 Charts & Visual Insights

| Sr. No | Chart Name                        | Columns / Measures                         | Insight |
|--------|----------------------------------|-------------------------------------------|---------|
| 1      | Monthly Completed Orders Trend    | Order Date, Total Orders Completed (KPI) | Shows monthly variation of successfully delivered orders to identify high-demand and low-demand periods. |
| 2      | Top 10 Products by Revenue        | Category, Total Revenue                    | Highlights highest revenue-generating product categories and identifies top-selling items. |
| 3      | Total Customers by Gender         | Gender, Total Customers                    | Displays customer distribution based on gender, providing insight into the dominant customer segment. |
| 4      | Total Revenue by Quarter          | Order Date, Total Revenue                  | Shows quarterly revenue performance to identify seasonal patterns, growth cycles, and overall business health. |


### 🎯 Summary

The **Overview Page** allows stakeholders to:

- Quickly monitor **business performance** through KPIs  
- Identify **trends** in orders, revenue, and customer activity  
- Evaluate **customer satisfaction** and **delivery efficiency**  
- Highlight **top-performing products and categories**  

It serves as the **primary dashboard for strategic decisions and operational monitoring**.

---

## 🛒 Products – KPI & Chart Insights

The **Products Page** provides a **detailed view of product performance**, combining KPIs and visualizations to understand inventory, product popularity, shipping efficiency, and revenue generation.

**Screenshot:**  
<img width="1408" height="791" alt="Products" src="https://github.com/user-attachments/assets/c3b0f98a-31a1-41ef-9a64-15b58942abab" />


### 🔑 Key KPIs

| Sr. No | KPI Name             | Insight |
|--------|--------------------|---------|
| 1      | Total Products       | Shows the total number of products in the catalog. Helps track catalog growth and overall marketplace inventory. |
| 2      | Active Products      | Indicates how many products have been ordered at least once. Helps identify products that are engaging customers. |
| 3      | Avg Shipping Cost    | Shows the average shipping cost per product. Helps monitor logistics expenses and manage delivery costs. |
| 4      | Avg Delivery Time    | Displays the average delivery time per product. Helps evaluate delivery efficiency and customer satisfaction. |

  

### 📈 Charts & Visual Insights

| Sr. No | Chart Name                              | Columns / Measures                     | Insight |
|--------|----------------------------------------|---------------------------------------|---------|
| 1      | Monthly Order Trend (Line Chart)       | Order Date, COUNT(Orders[OrderID])    | Displays overall order volume trend, helping identify monthly spikes or drops in customer purchasing activity. |
| 2      | Top 5 Products by Volume (Bar Chart)   | Category, Volume (cm²)                | Highlights the largest products by physical size or dimensions. Useful for inventory and logistics planning. |
| 3      | Top 5 Products by Quantity Sold (Bar)  | Category, COUNT(Orders[OrderID])      | Shows the most popular products based on the number of orders. Helps identify high-demand products. |
| 4      | Bottom 5 Products by Revenue (Bar)     | Category, Total Revenue                | Identifies underperforming products generating the least revenue. Helps make decisions on discounts, marketing, or discontinuation. |
| 5      | Total Orders by Status (Area Chart)    | Status, COUNT(Orders[OrderID])        | Shows the distribution of orders by status (Delivered, Pending, Canceled). Helps monitor fulfillment performance. |



### 🎯 Summary

The **Products Page** helps stakeholders:

- Track **overall product catalog** and active items  
- Evaluate **logistics efficiency** via shipping cost and delivery time  
- Identify **popular and underperforming products**  
- Make informed decisions for **inventory management, marketing, and promotions**  

This page ensures **product-level insights** to optimize marketplace operations and customer satisfaction.


---

## 🏪 Vendor / Sellers – KPI & Chart Insights

The **Vendor Page** provides insights into **seller performance**, revenue generation, and geographical presence, helping stakeholders understand which sellers contribute most to the marketplace.

**Screenshot:**  
<img width="1407" height="792" alt="Vendor" src="https://github.com/user-attachments/assets/9c201acf-5daa-4c61-b36c-64a1669e4385" />


### 🔑 Key KPIs

| Sr. No | KPI Name          | Insight |
|--------|-----------------|---------|
| 1      | Top Seller        | Highlights the seller generating the highest total revenue, identifying the strongest performer. |
| 2      | Total Sellers     | Shows how many sellers are registered on the platform. |
| 3      | Active Sellers    | Shows the number of sellers who made at least one sale during the selected period. |
| 4      | Seller Revenue    | Displays total revenue generated by all sellers combined. |


### 📈 Charts & Visual Insights

| Sr. No | Chart Name                       | Columns / Measures                       | Insight |
|--------|---------------------------------|-----------------------------------------|---------|
| 1      | Monthly Seller Revenue Trend     | Order Date, Seller Revenue (KPI)        | Tracks total seller revenue month-wise to identify growth patterns and high-performing periods. |
| 2      | Top 5 Sellers by Revenue         | Seller ID, Seller Revenue                | Shows which sellers generate the highest revenue, helping identify top contributors. |
| 3      | Top 5 Sellers by Sold Quantity   | Seller ID, COUNT(Order ID)               | Identifies sellers with the highest order count, highlighting high-volume sellers. |
| 4      | Geo Distribution of Sellers      | Country, COUNT(Seller ID)                | Shows seller presence by geography, useful for understanding market penetration. |
| 5      | Seller Category Performance      | Seller → Product Category → Revenue      | Shows revenue breakdown by seller and product category, helping analyze which categories perform best for each seller. |


### 🎯 Summary

The **Vendor Page** helps stakeholders:

- Identify **top-performing sellers** by revenue and order volume  
- Monitor **seller activity and engagement**  
- Analyze **geographical distribution** for strategic expansion  
- Evaluate **product category performance** per seller  

This page ensures **comprehensive seller analytics** to improve marketplace efficiency and support business growth.

---

## 👥 Customer – KPI & Chart Insights

The **Customer Page** provides detailed insights into **customer behavior, engagement, and demographics**.  
It helps stakeholders understand **active customers, retention trends, and revenue contribution**.

**Screenshot:**  
<img width="1408" height="788" alt="Customers" src="https://github.com/user-attachments/assets/987153f1-4128-46b3-b3cd-6aec5ae9a4eb" />


### 🔑 Key KPIs

| Sr. No | KPI Name                  | Insight |
|--------|--------------------------|---------|
| 1      | Active Customers (Last 30 Days) | Shows how many unique customers placed at least one order in the past 30 days. Measures engagement, activity level, and short-term retention. |
| 2      | Total Customers           | Represents the overall number of unique registered customers, reflecting the size of the customer base and long-term acquisition success. |
| 3      | Avg Age of Customers      | Displays the average age of all customers, helping identify the dominant age group and support customer segmentation analysis. |
| 4      | Avg Customer Rating       | Shows the average product/service rating given by customers. A higher rating indicates better service quality and satisfaction. |


### 📈 Charts & Visual Insights

| Sr. No | Chart Name                        | Columns / Measures                    | Insight |
|--------|----------------------------------|--------------------------------------|---------|
| 1      | Monthly Active Customers (Line Chart) | Order Date, Active Customer (30 Days) KPI | Shows how customer engagement changes month by month by tracking customers who placed orders recently. Identifies growth, seasonal trends, and high-activity months. |
| 2      | Age Group Distribution (Column Chart) | Age Group, COUNT(Customer ID)        | Displays the number of customers in each age group, helping understand demographics and dominant segments. |
| 3      | Top 5 Customers by Revenue (Bar Chart) | Customer ID, Total Revenue           | Highlights the top revenue-generating customers, useful for identifying high-value customers and planning retention strategies. |
| 4      | Top 10 Cities by Customers (Bar Chart) | City, COUNT(Customer ID)             | Shows which cities have the highest customer count, helping target regional campaigns. |
| 5      | Total Orders by Subscription Month (Line Chart) | Subscription Month, COUNT(Order ID) | Displays order activity by customers based on subscription month, helping identify whether early or recent subscribers are more active. |


### 🎯 Summary

The **Customer Page** helps stakeholders:

- Track **recently active customers** and engagement trends  
- Understand **customer demographics** and age group distribution  
- Identify **high-value customers** for targeted retention efforts  
- Analyze **geographical customer presence** for marketing strategies  

This ensures a comprehensive understanding of customer behavior, supporting **growth, engagement, and retention initiatives**.

---

## 💰 Revenue – KPI & Chart Insights

The **Revenue Page** provides a clear view of **financial performance, payment behavior, and revenue trends**.  
It helps stakeholders monitor **earnings, average revenue per order, and installment payment patterns**.

**Screenshot:**  
<img width="1406" height="786" alt="Revenue" src="https://github.com/user-attachments/assets/bb1ed935-6d01-483f-ba9c-e8b0dc6f0076" />


### 🔑 Key KPIs

| Sr. No | KPI Name                 | Insight |
|--------|--------------------------|---------|
| 1      | Total Revenue            | Represents the total earnings generated from all customer payments, indicating the overall financial performance of the business. |
| 2      | Avg Revenue Per Order    | Shows the average revenue earned for each order, helping measure how much value each customer order contributes. |
| 3      | Avg Payment Amount       | Reflects the average value of individual payment transactions, useful when customers make multiple or installment-based payments. |
| 4      | Installment Payment %    | Measures the percentage of orders paid through installments, helping understand payment behavior and cash-flow patterns. |


### 📈 Charts & Visual Insights

| Sr. No | Chart Name                         | Columns / Measures                | Insight |
|--------|-----------------------------------|----------------------------------|---------|
| 1      | Monthly Total Revenue (Line Chart) | Order Date, Total Revenue (KPI) | Tracks monthly revenue trends to identify growth, seasonal patterns, or drops in sales. |
| 2      | Installments vs Non-installments (Donut Chart) | Installment Flag, Total Revenue | Shows how much revenue comes from installment vs non-installment payments. |
| 3      | Payment Method Split (Bar Chart)   | Payment Method, Total Revenue    | Highlights which payment methods contribute the most revenue. |
| 4      | Avg Revenue Per Order by Quarter   | Order Date, Avg Revenue Per Order (KPI) | Reveals how average earnings per order change across quarters. |



### 🎯 Summary

The **Revenue Page** helps stakeholders:

- Monitor **total earnings and revenue trends**  
- Understand **average revenue per order** and payment patterns  
- Analyze **installment-based transactions** and cash-flow impact  
- Evaluate **payment method contribution** for strategic decision-making  

This ensures financial performance is **transparent, actionable, and ready for analysis and reporting**.

---

## 📝 Feedback – KPI & Chart Insights

The **Feedback Page** provides insights into **customer satisfaction, review trends, and engagement levels**.  
It helps stakeholders understand **overall satisfaction, positive/negative feedback ratios, and product/service performance from the customer’s perspective**.

**Screenshot:**  
<img width="1406" height="788" alt="Feedback" src="https://github.com/user-attachments/assets/b9ab1edd-6995-4e05-96cb-bb4fbd35696e" />


### 🔑 Key KPIs

| Sr. No | KPI Name                     | Insight |
|--------|------------------------------|---------|
| 1      | Average Rating               | Indicates overall customer satisfaction based on the average review scores received. |
| 2      | Total Reviews                | Shows the total number of customer reviews submitted, helping understand engagement and feedback volume. |
| 3      | % Positive Reviews (Rating 4–5) | Represents the percentage of highly satisfied customers who rated the product or service positively. |
| 4      | % Negative Reviews (Rating 1–2) | Highlights the percentage of unhappy customers, helping identify issues in product quality, delivery, or service. |


### 📈 Charts & Visual Insights

| Sr. No | Chart Name                       | Columns / Measures                 | Insight |
|--------|---------------------------------|----------------------------------|---------|
| 1      | Monthly Avg Rating (Line Chart) | Review Date, Average Rating (KPI) | Shows how customer satisfaction changes month-by-month by tracking average rating trends over time. |
| 2      | Rating Distribution (Donut Chart) | Rating Category, COUNT(Review ID) | Displays how ratings are spread across categories (1–5), helping identify whether customers are mostly happy or unhappy. |
| 3      | Top 10 Categories by Rating      | Category, COUNT(Review ID)        | Highlights which product categories receive the most reviews, helping identify customers' most discussed items. |
| 4      | Feedback in Detail (Matrix/Table)| Customer ID, Category, Volume (cm³), Avg Rating, Revenue, Status | Provides a detailed view of each customer’s feedback along with product category, size, rating, and revenue data. |

### 🎯 Summary

The **Feedback Page** allows stakeholders to:

- Monitor **average ratings** and customer satisfaction trends  
- Analyze **positive vs negative feedback** to detect pain points  
- Identify **top product categories based on reviews**  
- Access **detailed customer feedback** for deeper insights into product and service performance  

This ensures customer experience is **transparent, measurable, and actionable for business improvements**.


---
---

## 🛠️ Tools Used

- **Microsoft Power BI Desktop** – for building reports and interactive dashboards  
- **Power Query Editor** – for data cleaning and transformation  
- **DAX (Data Analysis Expressions)** – for calculating KPIs, percentages, trends  
- **Excel / CSV Dataset** – source of Amazon sales data

---
---

## 🙏 Acknowledgement  

Special thanks to the **Retail Sales Sharing Dataset (Open Data)** for providing an excellent real-world dataset.  
This project was created as part of a **Data Analytics learning journey** using **Power BI**.  

---
---

## 📎 Author  

**👤 Name:** Prafull Wahatule  
**📧 Email:** [prafullwahatule@gmail.com](mailto:prafullwahatule@gmail.com)  
**💻 GitHub:** [https://github.com/prafullwahatule](https://github.com/prafullwahatule)  
**🔗 LinkedIn:** [https://www.linkedin.com/in/prafullwahatule/](https://www.linkedin.com/in/prafullwahatule/)  
**🌐 Portfolio:** [https://prafullwahatule.github.io/portfolio/](https://prafullwahatule.github.io/portfolio/)

---

⭐ *If you found this project helpful, don’t forget to star the repository!* ⭐


