# Logistics-Performance-Dashboard
Interactive Power BI dashboard analyzing logistics performance—track order status, delivery trends, client metrics, and carrier efficiency across South Africa and Botswana. 
Logistics-Performance-Dashboard -- End-to-End Power BI Bootcamp presented by Pro. Tarcisio from Exodus-Experts

Project Overview
This Logistics Dashboard provides an interactive and visual overview of transportation and order delivery performance. Built using Power BI, it enables data-driven decision-making for supply chain optimization by tracking key metrics across clients, carriers, timelines, and geographies.

Setup Instructions: git clone https://github.com/thobanizondi/Logistics-Performance-Dashboard
-Import CSV into Power BI Load dataset (Different files - one PDF, one CSV, one XLSX)
-Apply transformations
-Create insights-driven dashboards

Order Status Visualization
- Create a dynamic visual that categorizes orders by status: On Time, Late, and Not Delivered. This helps stakeholders quickly assess delivery performance and service reliability.
Top 5 Client Performance Analysis
-Identify your top five clients by volume or revenue, then evaluate their delivery success rates. This reveals how well your service aligns with high-value relationships.
Root Cause of Late Deliveries
-Drill into late orders to uncover patterns—by region, carrier, or product type. Use filters and slicers to empower users to explore the “why” behind delays.
Annual Order Distribution
-Visualize order trends across the year using line or area charts. This helps detect seasonality, peak periods, and potential forecasting opportunities.
Annual Carriers Distribution
-Visualize Carriers trends across the year using line or area charts. This helps detect seasonality, peak periods, and potential forecasting opportunities.

Dashboard Features
-Revenue
-Profit
-Volume
-Weight
-5 Top Models
-Orders
-Location Intelligencer
-Date Slicers*
-Country Filter (Slicer) - Switch between Botswana and South Africa views

Tools & Technologies
-Power BI Desktop
-DAX - for calculated measures
-Power Query (M Language) - for data transformation
-Bing Maps API - for geographic visuals
-CSV/Excel/PDF/XLSX  - for data input

Files Included
- LogisticsDashboard.pbix – Power BI file with all data models and visuals
- data/ – Sample anonymized datasets (optional)
- images/ – Screenshots of key dashboard visuals
- README.md – This documentation

Key Use Cases
- Identifying late delivery root causes
- Monitoring client satisfaction through delivery metrics
- Tracking carrier performance and service levels
- Analyzing order patterns by region and year

Potential Enhancements
- Add predictive analytics for delivery delays
- Integrate real-time data feeds
- Include anomaly detection for outliers (e.g., very late shipments)


<img width="397" alt="Logistics-Dashboard" src="https://github.com/user-attachments/assets/974ddf50-d821-49ce-a168-a72daa6c2f87" />

Data Model Overview: The Power BI dashboard is powered by a star schema consisting of one central fact table (factInvoices) and two related dimension tables (dimClients and dimCarrier), with measures that contain DAX calculations. This structure supports optimized reporting and slicing across various sales dimensions.

<img width="454" alt="Logistics-Data-Model-Relationship" src="https://github.com/user-attachments/assets/85bd803c-b456-4bd3-bc02-c3cb18b39f0b" />

Data Model Relationships
This project follows a classic star schema with fact and dimension tables to support high-performance analytics and intuitive dashboard visuals.
Relationships:
- dimCarriers (1) - factInvoices (*)
- Joined by Carrier Code
- Represents a one-to-many relationship: Each carrier can appear in multiple invoice records.
  
- dimClients (1) - factInvoices (*)
- Joined by ClientCode
- Represents a one-to-many relationship: A single client can be associated with multiple invoices.
  
Tables Overview:
factInvoices
-Central table capturing transactional data:
-Carrier Code, ClientCode, Invoice Number, Collection Date, Delivery Date, Event, Gross Weight (kg), etc.

dimCarriers
-Lookup table with carrier metadata:
-Carrier, Carrier Code, Warehouse

dimClients
-Contains client attributes:
-ClientName, ClientCode, City, Country

0-Measures
-Measures table used for centralizing DAX KPIs like Orders, Total Weight, etc.

This relational structure supports modular, scalable dashboards and enables efficient data filtering across dimensions like carrier, client, and region.











