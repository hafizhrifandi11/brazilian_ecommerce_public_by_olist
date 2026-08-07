# 📊 Brazilian E-Commerce Public Dataset Analysis & Dashboard

**Source Dataset :** [Dashboard Overview](brazilian.ecommerce.dashboard.pdf) 

An interactive and comprehensive Business Intelligence dashboard built to analyze Brazilian e-commerce public data (Olist). This project uncovers key insights regarding customer behavior, sales trends, geographic distribution, payment methods, and logistics performance.

---
## 📝 Overview Dashboard
![Dashboard Preview](https://github.com/hafizhrifandi11/brazilian_ecommerce_public_by_olist/blob/main/Overview.png)
---
## Problem Statement

Olist's management wants a clear, centralized view of marketplace performance across its multi-year operations to answer key business questions:

- How have order volume and revenue evolved over time (2017–2018)?
- Which payment methods do customers rely on most, and does this affect transaction value?
- Which Brazilian states drive the most orders and revenue?
- What proportion of orders reach "delivered" status vs. other outcomes (cancelled, processing, etc.)?

Without a consolidated dashboard, order, payment, customer, and seller data lived in separate tables — making it difficult to quickly assess overall marketplace health and regional performance.

## Data Understanding & Preparation

The dataset (`Olist_Dataset.xlsx`) consists of **4 related tables** covering nearly 100,000 transactions:

| Table | Description | Size |
|---|---|---|
| `Orders` | Order-level records including product category, order status, and full order timeline (purchase, approval, delivery, estimated delivery) | ~97,688 orders |
| `Order_Payments` | Payment details per order (payment type, installments, payment value, price, freight cost) | ~103,057 records |
| `Customers` | Customer identifiers with city, state, and geolocation | ~99,442 customers |
| `Sellers` | Seller identifiers with city, state, and geolocation | ~3,089 sellers |

**Data preparation steps performed:**
- Combined `Orders`, `Order_Payments`, `Customers`, and `Sellers` tables into a relational data model in Tableau.
- Standardized date fields (purchase, approval, delivery, estimated delivery) to enable accurate time-series analysis by month and year.
- Mapped `customer_state` / `seller_state` to Brazilian regions for geographic visualization.
- Created calculated fields for key metrics: **Average Order Value (AOV)**, **Total Customers**, and **Average Revenue per Customer**.

---

## Analysis Process

1. **Data Integration** — merged order, payment, customer, and seller data into a single analytical model.
2. **Metric Development** — built core measures (Total Orders, Total Revenue, AOV, Total Customers, Average Revenue per Customer).
3. **Trend Analysis** — tracked monthly sales trend and year-over-year transaction value (2017 vs. 2018).
4. **Segmentation Analysis** — broke down revenue by payment method and order status.
5. **Geographic Analysis** — mapped order and revenue contribution by Brazilian state to identify top-performing regions.
6. **Dashboard Design** — built an interactive Tableau dashboard with filters for Seller City, Payment Type, Order Status, and Year.
   
---

## 🚀  Dashboard Summary
The dashboard provides a high-level executive summary alongside deep-dive exploratory analytics into key performance indicators (KPIs):

* **Total Orders:** 97,688
* **Total Revenue:** 12,997,657
* **AOV (Average Order Value):** 133.1
* **Total Customers:** 96,096
* **Average Revenue per Customer:** 130.7

---

## 📈 Key Features & Visualizations

1. **Executive KPI Cards:** Instant visibility into core business metrics including total orders, total revenue, average order value (AOV), unique customers, and customer lifetime value approximation.
2. **Sales Trend Analysis:** Monthly time-series tracking order volume and price trends from 2017 through 2018, highlighting seasonal spikes and business growth.
3. **Transaction Value by Year:** Yearly comparison of transaction values showing strong scaling from 2017 to 2018.
4. **Payment Methods Proportion:** Donut chart breakdown showcasing customer preferences across payment types (`credit_card`, `boleto`, `voucher`, `debit_card`).
5. **Geographic Distribution & Top States:** 
   * Interactive map visualization (`Top States Contribution`) powered by Mapbox & OpenStreetMap.
   * `Top 5 States by Orders` bar chart identifying economic hubs, with **São Paulo (SP)** leading overwhelmingly at 71,715 orders, followed by Minas Gerais (MG), Paraná (PR), Rio de Janeiro (RJ), and Santa Catarina (SC).
6. **Order Status Breakdown:** Operational health tracking fulfillment rates, showing the vast majority of orders successfully `delivered` alongside canceled, shipped, and processing statuses.

---

## 🛠️ Tools & Technologies
* **Data Visualization & BI:** Tableau 
* **Data Processing & Analysis:** Python (Pandas, NumPy) / SQL
* **Dataset:** Olist Brazilian E-Commerce Public Dataset (Kaggle)

---

## 📂 Project Structure
```text
├── dataset/              # Raw and processed CSV data files
├── dashboard/            # Tableau (.twbx) or Power BI (.pbix) files
├── screenshots/          # Dashboard preview images
└── README.md             # Project documentation
```

---

## 🔍 Key Business Insights
* **Geographic Concentration:** Sales and order volume are heavily concentrated in the Southeast region of Brazil, with **São Paulo (SP)** acting as the primary revenue and fulfillment powerhouse.
* **Payment Preference:** Credit cards dominate transaction types, followed closely by boleto, indicating a strong preference for digital and installment-friendly payment methods.
* **Order Fulfillment Efficiency:** High delivery success rates reflect robust logistical tracking across participating marketplace sellers.

---

## 👤 Author
**Muhammad Hafizh Rifandi**
* [LinkedIn](https://www.linkedin.com/in/hafizhrifandi/)
* [GitHub](https://github.com/hafizhrifandi11)
