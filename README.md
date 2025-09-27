# 🌍 Power BI Global Covid-19 & Vaccine Dashboard  

## 📖 Project Overview  
This project demonstrates how to build an **end-to-end Power BI analytics solution** using publicly available Covid-19 and vaccination data. The project covers:  
- Importing and preprocessing raw data from web APIs  
- Data modeling and creating DAX measures for KPIs  
- Designing effective dashboards for insights  
- Publishing reports to Power BI Service with automated refresh  

The final output consists of **two interactive dashboards**:  
- **Global Covid-19 Situation Dashboard**  
- **Global Vaccination Situation Dashboard**  

---

## 🛠️ Tech Stack  
- **Power BI Desktop**  
- **Power Query (M language)** for data transformation  
- **DAX (Data Analysis Expressions)** for measures & KPIs  
- **Power BI Service** for publishing & auto-refresh  

---

## 📂 Data Sources  
- **Covid-19 Data (Worldwide)** → Imported via Web API  
- **Vaccination Data (Worldwide)** → Imported via Web API  

Two tables are created in Power BI:  
- `Covid19` (cases & deaths)  
- `Vaccine` (doses administered)  

---

## 🔄 Data Preprocessing  
Performed in **Power Query Editor**:  
- Renamed tables (`Covid19`, `Vaccine`)  
- Ensured correct column data types  
- Applied **Unpivot** and **Extract** transformations to normalize data  
- Cleaned date fields for modeling  

---

## 📊 Data Model  
- Relationship between `Covid19` and `Vaccine` tables via **Date column**  
  - Type: **Many-to-Many (via Date dimension)** or **1-to-Many** if a proper Date table is introduced  
  - Reason: Both datasets share the Date field as a key for aggregation and comparison  

---

## 📐 DAX Measures  
A dedicated table `_Measures` was created to store all KPIs. Key measures include:  

- **Covid-19 Cases & Deaths**  
  - `Total Confirmed Cases`  
  - `Confirmed Cases Up to Today`  
  - `Confirmed Cases Up to Yesterday`  
  - `30-Day Avg Confirmed Cases`  
  - `60-Day Avg Confirmed Cases`  
  - `Deaths`  
  - `Deaths Up to Today`  
  - `Deaths Up to Yesterday`  
  - `Death Rate (%) = Deaths / Confirmed Cases`  

- **Vaccination**  
  - `Total Vaccine Doses Up to Today`  
  - `Most Recent Update Date`  

---

## 📈 Dashboards  

### 🦠 Global Covid-19 Dashboard  
- Trend line of daily confirmed cases with **30- & 60-day averages**  
- Top 10 countries with highest cumulative cases  
- World map of confirmed cases by country  
- KPI cards: total cases, deaths, new cases today  
- Global death rate (Deaths / Confirmed cases)  
- Slicers & bookmarks: 7 days, 30 days, 60 days, 1 year, all dates  

### 💉 Global Vaccination Dashboard  
- Table: country-level death rates  
- Table: vaccine doses by country  
- Line chart: daily death rate trend  
- Line chart: cumulative vaccine doses worldwide  
- World map: cumulative vaccine doses by country  
- KPI cards: most recent update date  

---

## 🚀 Deployment  
- Published dashboards to **Power BI Service**  
- Configured **daily auto-refresh** to keep reports up-to-date  

---

## 🔍 Insights (Sample)  
- Countries with higher vaccination rates show lower recent death rates.  
- Global case growth trends align with vaccine rollout phases.  
- Some regions with high cumulative cases lagged in vaccination coverage.  

---

## 📸 Screenshots  


---

## 📌 How to Use  
1. Clone this repo.  
2. Open the `.pbix` file in Power BI Desktop.  
3. Replace data source links with the provided API endpoints.  
4. Refresh to load the latest data.  

---

## 🎯 Key Skills Demonstrated  
- Data integration via API  
- Power Query transformations (Unpivot, Extract, Data Types)  
- Data modeling & relationships  
- DAX measures & time intelligence functions  
- Dashboard design best practices  
- Publishing & scheduling refresh in Power BI Service  

---

## 👤 Author  
**Trung Hieu Nguyen**  
- 📍 Sydney, Australia  
- 🎓 Business Analytics | Western Sydney University  
- 💼 Data Analyst  
