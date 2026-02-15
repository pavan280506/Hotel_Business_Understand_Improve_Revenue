# 📊 Revenue Strategy Dashboard (Power BI)

## 📌 Overview
An interactive Power BI dashboard built to analyze hotel booking performance and optimize revenue strategy using pricing tiers, seasonal trends, upsell insights, and country-wise performance analysis.

---

## 🏗️ Phase 1: Data Preparation & DAX

### 🔹 Calculated Column

```DAX
Pricing Tier = 
SWITCH(TRUE(), 
    'Fact_Bookings'[ADR] < 120, "Budget", 
    'Fact_Bookings'[ADR] <= 130, "Standard", 
    "Premium"
)
```

### 🔹 Core Measures

```DAX
Total Revenue = SUM('Fact_Bookings'[Revenue])

Room Revenue = SUM('Fact_Bookings'[Room_Revenue])

Upsell Revenue = [Total Revenue] - [Room Revenue]

Upsell Potential % = DIVIDE([Upsell Revenue], [Total Revenue], 0)

Avg ADR = AVERAGE('Fact_Bookings'[ADR])

Avg RevPAR = AVERAGE('Fact_Bookings'[RevPAR])
```

---

## 📊 Phase 2: Dashboard Design

### 1️⃣ Executive KPI Cards
- Avg ADR  
- Avg RevPAR  
- Total Revenue  
- Upsell Potential %  
- Average Review Score  

Provides a high-level performance snapshot.

---

### 2️⃣ Pricing Tier Effectiveness
- X-Axis: Pricing Tier  
- Y-Axis: Avg RevPAR & Occupancy %  

Shows which pricing tier generates the best return per available room.

---

### 3️⃣ Upsell Opportunity (Treemap)
- Category: Guest_Type  
- Details: Booking_Channel  
- Values: Upsell Revenue  

Identifies high-value upsell segments.

---

### 4️⃣ Seasonal Performance (Combo Chart)
- Column: Total Revenue  
- Line: Occupancy %  
- Legend: Season  

Analyzes revenue trends and seasonal demand.

---

### 5️⃣ High RevPAR Segments (Scatter Plot)
- X-Axis: Avg ADR  
- Y-Axis: Avg RevPAR  
- Bubble Size: Total Revenue  
- Details: Guest_Country  
- Trend Line Added  

Highlights high-value markets and pricing correlation.

---

## 🎛️ Phase 3: Interactivity

Slicers Added:
- Month  
- Guest Country  
- Booking Channel  
- Guest Type  
- Season  

Enables dynamic filtering and segment-level analysis.

---

## 📌 Key Insights

- Premium tier generates highest RevPAR.  
- Revenue peaks in early-year months.  
- Direct bookings improve upsell opportunities.  
- Positive correlation between ADR and RevPAR.  
- Spain and Germany represent strong high-value markets.

---

## 🛠 Tools Used
- Microsoft Power BI  
- DAX  
- Data Modeling & Visualization  

---

## 🎯 Business Impact
Helps revenue managers optimize pricing strategy, identify profitable segments, analyze seasonal demand, and improve upsell targeting through data-driven insights.