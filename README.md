# car-rental-powerbi-dashboard
An enterprise-grade Power BI dashboard analyzing fleet utilization, revenue KPIs (RPD/LOR), and demand forecasting using Google BigQuery and Inforiver.
# Enterprise Mobility & Fleet Revenue Analytics Dashboard

## 📌 Project Overview
This project is an enterprise-grade 15-page Power BI dashboard designed for the Car Rental and Mobility domain. It connects to Google BigQuery to analyze massive datasets, track fleet utilization, and optimize Revenue Per Day (RPD). It features advanced demand forecasting and calendar heatmaps using Inforiver to minimize no-shows and optimize vehicle allocation.

## 🛠️ Tech Stack
* **Data Source:** Google BigQuery
* **BI Tool:** Power BI
* **Custom Visuals:** Inforiver (for Variance tracking & Demand Forecast Heatmaps)
* **Languages:** DAX (Time Intelligence, KPI Engineering), SQL

## 🗄️ Data Architecture & Modeling
The data model follows a Star Schema architecture connecting three primary fact and dimension tables:
1. **Booking Insight Table:** Tracks `Bookingadvdays`, `Cancel count`, `LOR` (Length of Rent), `Revenue`, `Customer ID`, and `Shop date`.
2. **Utilization Table:** Tracks `Capacity count`, `Pace`, `Reserved`, and `Car class code`.
3. **Customer Dimension:** Maps `Customer ID`, `Customer Name`, and `Currency`.
*(Note: A centralized custom Date Table was engineered for complex Time Intelligence calculations).*

## 📊 Key Business Impact & Visualizations
* **Executive Performance (Pages 1-3):** YoY comparison matrix for Net Bookings and Revenue, tracking metrics like Total Booking LY/TY and RPD trends.
* **Operational Behavior (Pages 4-10):** * 30-Day Rolling Booking & Revenue Curves.
  * Lead Time (Days Out) bucket analysis to track last-minute booking percentages.
  * Day-of-Week patterns for No-shows and Cancellations.
* **Forecasting & Variance (Pages 12-13):** Dynamic Inforiver Calendar Heatmaps tracking Actual Utilization vs. Demand Forecast, highlighting positive/negative variance.

## 💻 Sample DAX Implementations
Check the `DAX_Measures` folder in this repo for the code behind:
* Dynamic Lead Time (Days Out) categorization.
* YoY % Variance calculations using `SAMEPERIODLASTYEAR`.
* Custom Rolling 30-Days revenue logic.

---
*If you'd like an interactive walkthrough of this dashboard, please feel free to reach out!*
