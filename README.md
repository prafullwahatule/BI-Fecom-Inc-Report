# 📊 BI Fecom Inc Report

This Power BI project provides a comprehensive **Business Intelligence Report** for **Fecom Inc**, covering **sales, customers, products, sellers, payments, reviews,** and **geographic insights**.  
It helps business users and decision-makers analyze performance trends, track revenue, monitor customer behavior, and evaluate product & seller efficiency.

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

## 🧠 Data Model Overview

**Dimension Tables:**  
`Products`, `Sellers_List`, `Customer_List_clean`  

**Fact Tables:**  
`Orders`, `Order_Items`, `Order_Payments`, `Order_Reviews`  

**Support Table:**  
`Geolocations`

---

## 🛠️ Technologies Used

- **Power BI Desktop**  
- **DAX** (for calculated measures and KPIs)  
- **Data Modeling & Relationships** (for unified insights)

---

## 🎯 Purpose

This report provides **actionable insights** to help Fecom Inc:  
- Improve sales & profitability  
- Monitor business and seller performance  
- Understand customer patterns  
- Enable **data-driven decision-making**

---

## 🧑‍💻 Author

**Prafull Wahatule**  
📧 [prafullwahatule@gmail.com](mailto:prafullwahatule@gmail.com)  
🔗 [GitHub Profile](https://github.com/prafullwahatule)  
🔗 [LinkedIn Profile](https://www.linkedin.com/in/prafullwahatule/)  

