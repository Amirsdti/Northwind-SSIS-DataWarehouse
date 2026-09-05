# Northwind Data Warehouse - ETL Project

## 📌 Project Overview
This project demonstrates the design and implementation of a Data Warehouse based on the **Northwind** database. The ETL processes were developed using **SQL Server Integration Services (SSIS)** to extract transactional data, transform it into a dimensional model, and load it into the Data Warehouse.

## 🏗️ Architecture & Data Modeling
The Data Warehouse follows a **Snowflake Schema** design. This normalized dimensional approach optimizes data integrity and reduces redundancy.
*   **Fact Table:** Stores quantitative transaction data (FactOrders).
*   **Dimension Tables:** Store descriptive attributes. Dimensions like DimSuppliers and DimCustomers branch out to related dimensions like DimGeo, forming the snowflake structure.

## ⚙️ ETL Methodologies Applied
*   **Execute SQL Task (Truncation):** Applied exclusively to the `DimGeo` table to truncate old data prior to the Data Flow execution.
*   **Slowly Changing Dimensions (SCD Type 1):** Applied to the Fact table and all other Dimension tables using the **Changing attribute** configuration. This methodology overwrites existing records with new data, ensuring the warehouse reflects the most current state without maintaining historical rows.
*   **Lookups:** Utilized extensively in Data Flows to map Business Keys to Surrogate Keys, establishing logical relationships without physical database constraints.

## 🛠️ Technologies & Tools
*   **Microsoft SQL Server (SSMS):** Database management and schema design.
*   **SQL Server Integration Services (SSIS):** Data integration, automated SCD Type 1 workflows, and Execute SQL Tasks.
*   **Visual Studio:** IDE for SSIS package development.

## 🖼️ Snapshots

<img width="882" height="606" alt="DimEployees" src="https://github.com/user-attachments/assets/277ed941-1fe1-4763-bb32-24403dce35d5" />

<img width="851" height="627" alt="DimProducts" src="https://github.com/user-attachments/assets/ae7119ac-8c36-4a70-9ebc-b42e160bdf9c" />

<img width="658" height="702" alt="FactOrders01" src="https://github.com/user-attachments/assets/3d490021-1f67-4449-ab12-f58e70df541b" />

<img width="696" height="637" alt="FactOrders02" src="https://github.com/user-attachments/assets/e92287c6-ca43-40c9-8053-435ef9ec8444" />








