# Logistics Analysis Report

## Table of Contents
- [Introduction](#introduction)
- [Project Objectives](#project-objectives)
- [Data Cleaning and Transformation (Power Query)](#data-cleaning-and-transformation-power-query)
- [Data Normalization and Modelling](#data-normalization-and-modelling)
- [Analysis and Calculations using DAX](#analysis-and-calculations-using-dax)
- [Data Visualization Dashboard Preview](#data-visualization-dashboard-preview)
- [Insights](#insights)
- [Conclusion](#conclusion)
- [Recommendations](#recommendations)
- [About Me](#about-me)

---

## Introduction
Logistics forms the foundation of many businesses, yet delays, inefficiencies, and poor customer satisfaction can quietly erode overall performance. This report delivers a structured analysis of shipment data, forecasting, and customer experience, equipping stakeholders with clear insights to drive smarter decisions.

---

## Project Objectives
- Provide a clear picture of shipment performance across all modes.  
- Identify priority issues in delivery timelines and customer satisfaction.  
- Recommend actionable strategies to improve logistics efficiency.  
- Support decision‑making with data‑driven insights.  

---

## Data Cleaning and Transformation (Power Query)
- Applied steps: promoted headers, changed data types, added custom/conditional columns, split columns, removed duplicates, added index, reordered columns.  
- Merged queries with dimension tables (DimCarrier, DimCustomer, DimLocation, DimPayment, DimShipment, DimShippingMode, etc.) to enrich the fact table.  
- Outcome: a clean, consistent dataset ready for modeling.  

---
## Entity Relationship Diagram (ERD)
![ERD Diagram](images/Erddiagram.png)

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

![Dashboard Page 1](images/page1.png)

- **Page 1: Overview of Shipment Status**  
  - Completed shipments: 16.74K (+25% YoY), $11.32M value.  
  - In progress shipments: 47.46K (+25% YoY).  
  - Average delivery time: 9.7 days.  

![Dashboard Page 2](images/page2.png)

- **Page 2: Shipment Forecasting by Mode**  
  - Jets: 11,775 shipments (4,002 high priority).  
  - Bus: 10,861 shipments (3,602 medium priority).  
  - Lorry: 12,604 shipments (4,430 low priority).  
  - Motorbike: 12,224 shipments (4,443 medium priority).  
  - Regional breakdown highlights Lagos, Abuja, Port Harcourt, Accra.  

![Dashboard Page 3](images/page3.png)

- **Page 3: Customer Experience & Delivery Metrics**  
  - Business customers: 35.99%, Retail: 32.85%, International: 31.16%.  
  - Satisfaction tracked (Very Satisfied, Neutral, Unsatisfied).  
  - Payment status linked to satisfaction (Paid, Pending, Overdue).  

---

## Insights
- More than half of completed shipments are **late**, showing efficiency gaps.  
- **Motorbike and Lorry** shipments have weaker performance and satisfaction scores.  
- Regional disparities: Lagos and Abuja strong, Port Harcourt and Accra weaker.  
- Only **32% of shipment value is paid**; overdue payments hurt satisfaction.  

---

## Conclusion
This comprehensive Logistics Analysis Report gives stakeholders a clear view of shipment performance, highlights priority issues, and provides actionable insights to improve efficiency.  

---

## Recommendations
- Improve delivery times for **Motorbike and Lorry shipments**.  
- Prioritize **high‑value and high‑priority shipments** for faster delivery.  
- Use **regional insights** to optimize shipment routes and carrier performance.  
- Strengthen payment processes to reduce overdue balances.  
- Enhance customer communication during delays to improve satisfaction.  

---

## About Me
Prepared by **Akitoye Michael Oluwaseyi**  
Passionate about data analysis, logistics optimization, and building actionable dashboards.  

