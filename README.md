# 🏨 Hotel Business: Understand and Improve Revenue  
## Power BI Analytics Project

## Project Overview
This project focuses on analyzing hotel booking data to understand occupancy patterns, revenue performance, and guest behavior. Using Power BI, the project builds an analytical solution to support data-driven decisions related to pricing, promotions, room optimization, and revenue strategy.  
The project is structured into multiple modules and is implemented incrementally through milestones.

## Project Objectives
- Track occupancy rates and booking trends
- Analyze pricing effectiveness using ADR and RevPAR
- Understand guest demographics and booking behavior
- Compare performance across booking channels and hotel branches
- Enable scalable analytics across hotels and locations.

---

## Module-wise Description

### Module 1: Data Modeling and Ingestion
This module focuses on preparing the analytical foundation for the project.
- Loaded booking, customer, room, and hotel branch data
- Designed a star schema with Date, Room, Customer, and Hotel dimensions
- Created derived attributes such as room category and stay-related fields
- Validated relationships and ensured clean data modeling.

---

### Module 2.1: Occupancy & Revenue Metrics
This module analyzes hotel performance using key revenue and occupancy KPIs.
- Calculated Occupancy %, Average Daily Rate (ADR), and Revenue per Available Room (RevPAR) using DAX
- Visualized revenue and occupancy trends over time
- Analyzed performance across months and seasons
- Compared Direct bookings and OTA bookings
- Enabled interactive filtering by room category, hotel branch, and booking source.

---

### Module 2.2: Guest Analysis
This planned module focuses on understanding guest behavior and demographics.
- Analysis of guest types and booking characteristics
- Visuals for nationality and booking source
- Guest segmentation into first-time guests, loyal guests, and high spenders.
  
---

### Module 3: Forecasting and Cancellation Trends
This module aims to extend analysis into predictive insights.
- Forecasting future occupancy using historical trends
- Cancellation rate and booking lead-time analysis
- No-show and refund trend visualization.

---

### Module 4: Revenue Strategy Dashboard
This final module focuses on decision support for hotel management.
- Identification of upsell opportunities
- Seasonal and room-type based pricing recommendations
- Strategic dashboard for general managers and revenue teams

---

## Architecture Overview
- **Data Sources:** Booking engines, hotel CRM, channel managers
- **Transformation Layer:** Power Query
- **Modeling Layer:** Guest, Booking, Room, Date
- **Visualization Layer:** Occupancy, Revenue, Guest Analysis dashboards

---

## Tools and Technologies
- Power BI
- DAX
- Power Query
- Star Schema Data Modeling

---

## Conclusion
This project demonstrates a structured, milestone-based approach to building a hotel revenue analytics solution in Power BI. The completed modules provide clear insights into occupancy and revenue performance, while future modules are designed to enhance guest understanding, forecasting capability, and revenue strategy planning.
