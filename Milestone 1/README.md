
# Milestone 1: Data Modeling and Ingestion – Hotel Revenue Project

## Project Overview
This project focuses on the data modeling and ingestion phase for a Hotel Business Intelligence solution. The goal was to transform a raw daily performance dataset into a functional Star Schema to enable professional-grade revenue and operational analysis.

## Data Ingestion & Transformation
Using Power Query, the following data cleaning and transformation steps were performed to ensure the dataset was analysis-ready:

- **Metric Correction:** Calculated missing RevPAR values using the formula:  
  RevPAR = Occupancy Rate × ADR

- **Profit Calculation:** Since the source Profit column was empty, a custom column was created:  
  Profit = Total Revenue − Total Costs

- **Data Cleaning:** Standardized date formats, removed null values, and ensured all financial columns were set to Currency data types.

## Data Modeling (Star Schema)
To meet the project requirements, a Star Schema was designed to separate numerical facts from descriptive dimensions, improving report performance and usability.

- **Fact Table:**  
  **Fact_Bookings** – Contains core quantitative metrics such as Revenue, Bookings, Costs, Profit, and Marketing Spend.

- **Dimension Tables:**  
  **Dim_Date** – Time-based analysis (Month, Weekday, Season)  
  **Dim_Customer** – Guest Country and Guest Type segmentation  
  **Dim_Room** – Room category analysis  
  **Dim_Hotel_Branches** – Organizational context for hotel branches

## Calculated Columns (DAX)
Three mandatory calculated columns were created in the Fact_Bookings table:

- **Booking Duration:** Set to 1 to represent the daily grain of the source data.  
- **Room Category:** Classified as "Deluxe" if ADR ≥ 125, otherwise "Standard".  
- **Stay Type:** Categorized as Short Stay, Medium Stay, or Long Stay based on checkout volumes.

## Key Observations
- **Marketing Impact:** A clear correlation exists between daily Marketing_Spend and New_Bookings, indicating marketing efforts are driving booking volume.  
- **Guest Performance:** The USA is the highest-contributing market in terms of both Revenue and Average Review Score.  
- **Profitability:** Deluxe room categories generate higher profit margins despite lower volume compared to Standard rooms.

## Conclusion
This milestone established a clean, well-structured Star Schema that forms a strong foundation for advanced BI reporting, dashboarding, and data-driven decision-making.
