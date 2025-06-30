#  Revenue Insights in Hospitality Domain – Power BI Project

## Project Overview

**Project Title:** Revenue Insights in Hospitality Domain  
**Level:** Intermediate  
**Tool:** Microsoft Power BI  

This project showcases the use of Power BI to analyze and visualize key revenue metrics in the hospitality sector. It provides interactive dashboards to help stakeholders understand trends, track performance, and make data-driven decisions.

![Library_project](https://github.com/BijoyBytes/Power-Bi-Hospitality-Analysis/blob/main/wmremove-transformed.jpeg)


---

##  Objectives

1. Develop interactive dashboards to explore revenue and occupancy trends.
2. Enable dynamic filtering by time period, property, and customer segment.
3. Highlight key performance indicators (KPIs) such as ADR, RevPAR, and Occupancy Rate.
4. Identify revenue drivers and underperforming segments.
5. Share insights with management through an accessible Power BI report.

---

## 📂 Project Structure

### 1. Data Sources & Preparation
- Imported booking and property data.
- Applied Power Query transformations:
  - Removed duplicates.
  - Cleaned date formats.
  - Merged lookup tables.
- Created calculated columns and measures.

### 2. Data Model
- Defined relationships between fact and dimension tables.
- Built DAX measures to compute KPIs:
  ```dax
  Total Revenue = SUM(Bookings[Revenue])

  ADR = DIVIDE([Total Revenue], [Total Rooms Sold])

  Occupancy Rate = DIVIDE([Total Rooms Sold], [Available Rooms])

  RevPAR = [ADR] * [Occupancy Rate]
