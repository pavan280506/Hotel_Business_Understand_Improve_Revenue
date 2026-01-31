# Milestone 3 – Forecasting and Cancellation Analysis  
**Project:** HotelRevAI – AI Driven Revenue Analysis for Hotels  

---

## Overview
Milestone 3 focuses on extending the hotel revenue analytics solution with **forecasting**, **cancellation analysis**, and **booking behavior insights** using Power BI. The objective is to analyze historical booking patterns and translate them into **forward-looking insights** that support demand planning, occupancy management, and revenue optimization.

The final dashboard titled **“Forecasting and Cancellation Analysis”** consolidates key performance indicators, trend analysis, and predictive visuals into a single interactive view for business decision-making.

---

## Data Model Structure
The Power BI report is built using a star schema to ensure accurate filtering and aggregation:

- **Fact_Bookings**
  - Total bookings, new bookings
  - Cancellations and no-shows
  - Occupancy-related measures

- **Dim_Date**
  - Date, month, year
  - Used for trend analysis, slicers, and forecasting

- **Dim_Hotel_Branches**
  - Hotel branch / location attributes

- **Dim_Customer**
  - Guest type (Business, Leisure)

- **Dim_Room**
  - Room and accommodation details

This structure supports time-series forecasting and multi-dimensional analysis.

---

## Forecasting Approach
Forecasting is implemented using **Power BI’s built-in Analytics Forecast feature** on line charts.

- **Forecasted Metrics:**
  - Total Bookings by Day
  - Average Occupancy by Day

- **Forecast Configuration:**
  - Units: Points  
  - Forecast Length: 10 future points  
  - Seasonality: Auto (system-detected patterns)  
  - Confidence Interval: 95%  

The dashboard clearly distinguishes **actual historical values** from **forecasted values**, with shaded confidence intervals to represent prediction uncertainty.

---

## Cancellation & No-Show Analysis Logic
Cancellation and no-show behavior is analyzed using derived KPIs and trend visuals.

### Key Measures:
- **Cancellation Rate** = Total Cancellations / Total Bookings  
- **No-Show Rate** = Total No-Shows / Total Bookings  
- **Average Occupancy** = Average Occupancy Rate  

### Visual Analysis:
- Cancellation rate trends by year and by day
- No-show rate trends over time
- Percentage-based cancellation fluctuations to identify volatile periods

These visuals help identify revenue leakage and operational risk periods.

---

## Booking Behavior & Lead-Time Insights
The dataset does not contain an explicit booking lead-time field. Therefore, booking behavior is **inferred** through:
- **New Bookings by Month**
- Daily booking trends
- Seasonal demand patterns

This approach highlights how booking volume varies across months and seasons and is clearly stated as an analytical assumption.

---

## Dashboard Components
The final dashboard includes:

### KPI Cards
- Total Bookings  
- Average Occupancy  
- Cancellation Rate  
- No-Show Rate  

### Trend & Forecast Visuals
- Total Bookings by Day (Actual vs Forecast)
- Average Occupancy by Day (Actual vs Forecast)
- Cancellation Rate by Year
- No-Show Rate by Day

### Behavioral Analysis
- New Bookings by Month
- Daily cancellation rate fluctuations

### Interactive Filters
- **Season** (Spring, Summer, Winter)
- **Guest Type** (Business, Leisure)
- **Date Range** slicer

All visuals are fully interactive and respond dynamically to slicer selections.

---

## Key Insights
- Booking demand shows **clear temporal patterns**, making it suitable for short-term forecasting.
- Forecasted bookings indicate potential stabilization after recent fluctuations.
- Cancellation rates remain relatively low overall but show **day-level volatility**.
- No-show rates are consistent but represent a measurable source of revenue loss.
- Monthly booking distribution highlights demand concentration in specific periods.

---

## Business Implications
- Forecasting supports **proactive demand and occupancy planning**.
- Cancellation and no-show analysis helps refine **overbooking and refund strategies**.
- Seasonal and guest-type filters enable **targeted revenue strategies**.
- The dashboard provides a concise, decision-ready view for hotel management.

---

## 📁 Repository Structure

Hotel_Business_Understand_Improve_Revenue/
└── Milestone 3/
├── Milestone3_PowerBI.pbix
├── screenshots/
│ └── Report.png
└── README.md

---

## Conclusion
Milestone 3 successfully extends descriptive analytics into **predictive and strategic insights**. By integrating forecasting, cancellation analysis, and interactive exploration, the dashboard enables data-driven decision-making for hotel revenue and operations management.