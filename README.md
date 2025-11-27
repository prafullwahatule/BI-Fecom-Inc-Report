# 📊 BI Fecom Inc Report

This Power BI project provides a comprehensive **Business Intelligence Report** for **Fecom Inc**, covering **sales, customers, products, sellers, payments, reviews,** and **geographic insights**.  
It helps business users and decision-makers analyze performance trends, track revenue, monitor customer behavior, and evaluate product & seller efficiency.

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

--

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

