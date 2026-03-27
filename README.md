# Logistics Analysis Report

## Table of Contents
- [Introduction](#introduction)
- [Project Objectives](#project-objectives)
- [Data Cleaning and Transformation (Power Query)](#data-cleaning-and-transformation-power-query)
- [Entity Relationship Diagram (ERD)](#entity-relationship-diagram-erd)
- [Data Normalization and Modelling](#data-normalization-and-modelling)
- [Analysis and Calculations using DAX](#analysis-and-calculations-using-dax)
- [Data Visualization Dashboard Preview and Key Insights](#data-visualization-dashboard-preview)
  - [Page 1 - Executive Logistics Dashboard](#page-1---executive-logistics-dashboard)
  - [Page 2 - Shipment Analysis by Transport Mode](#page-2---shipment-analysis-by-transport-mode)
  - [Page 3 - Customer Experience & Delivery Metrics](#page-3-customer-experience--delivery-metrics)
- [Conclusion](#conclusion)
- [Key Recommendations](#key-recommendations)
- [About Me](#about-me)


---

## Introduction
Logistics forms the foundation of many businesses, yet delays, inefficiencies, and poor customer satisfaction can quietly erode overall performance. This report delivers a structured analysis of shipment data, forecasting, and customer experience, equipping stakeholders with clear insights to drive smarter decisions.

---

## Project Objectives
-	Quantify completed and in-progress shipments across multiple transport modes (Jet, Bus, Lorry, Motorbike).
-	Evaluate shipment value trends and the financial performance of logistics services.
-	Analyze shipment efficiency and delivery performance across key regions (Lagos, Abuja, Port Harcourt, etc.).
-	Measure customer satisfaction levels, identify drivers of positive or negative experiences, and examine the impact of shipment delays or payment status on ratings.
-	Recommend improvements to enhance shipment delivery timelines, optimize transport mode deployment, and increase overall satisfaction.

---

## Data Cleaning and Transformation (Power Query)
- Applied steps: promoted headers, changed data types, added custom/conditional columns, split columns, removed duplicates, added index, reordered columns.  
- Merged queries with dimension tables (DimCarrier, DimCustomer, DimLocation, DimPayment, DimShipment, DimShippingMode, etc.) to enrich the fact table.  
- Outcome: a clean, consistent dataset ready for modeling.  

---
## Entity Relationship Diagram (ERD)
![ERD Diagram](images/Erd%20diagram.png)

---

## Data Normalization and Modelling
- Built a star schema with **FactLogistics** as the central fact table.  
- Linked dimension tables for carriers, customers, shipment modes, payment status, and satisfaction categories.  
- Ensured relationships support accurate filtering, slicing, and aggregation.  

---

## Analysis and Calculations using DAX
- Created measures for shipment status (% Completed, % In Transit, % Early, % Late).  
- Built financial metrics (% Paid, % Pending, % Overdue).  
- Mode and priority analysis (Bus, Jets, Lorry, Motorbike by High/Medium/Low priority).  
- Trend analysis (MoM and YoY changes in shipments and value).  
- Customer satisfaction averages and correlations with payment status.  

---

## Data Visualization Dashboard Preview

![Dashboard Page 1](images/Page%201.png)
## Page 1 - Executive Logistics Dashboard

### Purpose
Provide executives with a high-level snapshot of logistics performance.

### KPIs & Measures Used
- **Shipment Status:** % Completed, % In Transit, % Not Completed, % Ready for Pickup
- **Performance Metrics:** Shipment Value, Average Delivery Day, Average Satisfaction Score
- **Trend Measures:** Month-over-Month (MoM) and Year-over-Year (YoY) for Completed, In Progress, and Shipment Value

### Visuals
- KPI cards showing shipment status percentages
- Line chart illustrating shipment trends over time
- Bar chart comparing carrier performance ratings
- Trend indicators (▲ ▼) for MoM and YoY changes

### Key Insights
- **Completed Shipments**
  - Total completed shipments: **16.74K**, a **25% increase YoY**.
  - Value of completed shipments: **$11.32M**, also a **25% increase YoY**.
  - Average shipment time: **9.7 days**. Jets are fastest (**10.1 days**), Motorbikes slowest (**9.9 days**).
- **In Progress Shipments**
  - **47.46K** shipments still in progress, a **25% increase YoY**.
  - High‑priority shipments account for the largest share of in‑progress deliveries.
- **Shipment Trend Analysis**
  - Monthly and yearly trends highlight growth patterns and delivery challenges.

---

![Dashboard Page 2](images/Page%202.png)

## Page 2 - Shipment Analysis by Transport Mode

### Purpose
Break down shipment volumes and performance by transport mode.

### KPIs & Measures Used
- **Mode Measures:** `Mode_Bus`, `Mode_Jets`, `Mode_Lorry`, `Mode_Motorbike`
- **Priority Measures:** `P_High`, `P_Medium`, `P_Low` for each mode
- **Location Measures:** `Location_Title` for dynamic city-level analysis

### Visuals
- Stacked bar charts showing completed vs in-progress shipments by mode
- Tables showing shipment counts by city and mode
- Priority distribution visuals (High, Medium, Low)

### Key Insights
- **Jets:** 11,775 shipments forecasted, with **4,002 high‑priority** deliveries.
- **Bus:** 10,861 shipments forecasted, with **3,602 medium‑priority** deliveries.
- **Lorry:** 12,604 shipments forecasted, with **4,430 low‑priority** deliveries.
- **Motorbike:** 12,224 shipments forecasted, with **4,443 medium‑priority** deliveries.
- **Regional Breakdown:** Shipments distributed across Lagos, Abuja, Port Harcourt, and other regions, revealing regional disparities in performance.

---

![Dashboard Page 3](images/Page%203.png)

### Page 3: Customer Experience & Delivery Metrics 
### Purpose
Track satisfaction level (Very Satisfied, Neutral, Unsatisfied, Dissatisfied).  
### Key Insights
- **Customer Type Breakdown**
  - Business customers: **35.99%** of completed shipments.
  - Retail customers: **32.85%**.
  - International customers: **31.16%**.
- **Shipment Status**
  - Metrics track statuses such as In Transit, Ready for Pickup, Completed, etc.
  - Priority levels highlight shipments needing immediate attention.
- **Satisfaction Level**
  - Customer satisfaction tracked by categories: Very Satisfied, Neutral, Unsatisfied.
  - Shipment Value and Delivery Time strongly influence satisfaction.
- **Payment and Rating**
  - Payment status (Paid vs Pending) and delivery ratings correlate with satisfaction levels. 

---

### Conclusion
This comprehensive Logistics Analysis Report provides stakeholders with a clear view of shipment performance, highlights priority issues, and guides actions to improve logistics efficiency. The insights support better decision‑making in delivery timelines, transport mode optimization, and customer satisfaction.

### Key Recommendations
- Improve delivery times for **Motorbike and Lorry shipments**.
- Prioritize **high‑value and high‑priority shipments** for prompt delivery.
- Leverage **regional insights** to optimize shipment routes and carrier performance. 

---

## About Me
Prepared by **Akitoye Michael Oluwaseyi**  
Passionate about data analysis, logistics optimization, and building actionable dashboards.  

