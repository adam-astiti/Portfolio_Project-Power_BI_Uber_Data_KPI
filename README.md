# 📊 Uber NYC Data and KPI Dashboard (Power BI)

<table>
  <tr>
    <td width="33%"><img src="https://github.com/user-attachments/assets/5a3c5bbe-b1d4-46b2-9a03-e61c163d88ab" alt="KPI Summary Page"></td>
    <td width="33%"><img src="https://github.com/user-attachments/assets/0b88db98-164c-410b-80f8-158dc530a051" alt="Financials by Location Page"></td>
    <td width="33%"><img src="https://github.com/user-attachments/assets/aab2947a-09de-4c06-9a47-33a7bf2d63f1" alt="Operational by Location Page"></td>
  </tr>
</table>
</table>

*A snapshot of each page, showcasing key metrics and interactive elements.*

## 📌 Project Overview

This project provides a comprehensive, interactive performance dashboard for Uber's New York City operations for June 2024. The dashboard was developed to solve the critical business problem of fragmented and delayed data, enabling leadership to shift from reactive problem-solving to a proactive, data-driven strategy.

Designed specifically for an **NYC Operations Manager**, this tool provides a centralized source of truth to monitor and improve the health of the Uber marketplace. It is built to directly inform high-impact business decisions, including:

* **Optimizing Driver Allocation:** By identifying peak demand periods and specific high-traffic hotspots, managers can strategically deploy driver incentives to reduce wait times and maximize ride capture.
* **Informing Growth Strategy:** The dashboard reveals nuanced financial insights, such as identifying underserved but highly profitable outer boroughs (like Staten Island and Queens), guiding targeted campaigns for driver recruitment.
* **Improving Operational Efficiency:** By analyzing trip durations and average speeds by location, the dashboard helps diagnose operational bottlenecks like traffic, allowing for more accurate ETA predictions and better service quality management.

At its core, the dashboard tells a key strategic story: while Manhattan is the engine for ride **volume**, the outer boroughs represent a significant and untapped opportunity for high-**value**, profitable trips.

## 💡 Key Insights & Findings

The dashboard surfaces several critical insights into Uber's NYC operations for June 2024:

1.  **High-Level Performance:** In June 2024, operations generated **$1.54M in revenue** from **103.6K trips**, with an average booking value of **$14.90**.
2.  **Predictable Demand Patterns:** Demand follows a clear weekly rhythm, culminating in a significant surge on **Saturday and Sunday**. Daily operations are driven by a dual-peak model with spikes during the **8 AM morning commute** and a sustained **4 PM - 8 PM evening peak**.
3.  **Manhattan as the Volume Engine:** **Manhattan** is the core driver of business, overwhelmingly leading in both the total number of trips and overall revenue generated. The top 7 busiest pickup hotspots are all located there.
4.  **The Outer Borough Profitability Insight:** A key strategic finding is the untapped value of the outer boroughs. Trips in **Queens and Staten Island**, while less frequent, are **individually more profitable**, showing higher average surge fees and indicating significant unmet rider demand.
5.  **The Efficiency Paradox:** Despite being the volume engine, Manhattan is one of the **least efficient boroughs**, with the **second-slowest on-road speeds** due to traffic, just slightly faster than the Bronx. This highlights a major operational challenge in the city's primary market.

## 🛠️ Technical Skills & Tools Used

This project was developed end-to-end using **Microsoft Power BI**.

### 1. Data Transformation (Power Query)

<table>
  <tr>
    <td width="33%" valign="top">
      <img src="https://github.com/user-attachments/assets/7f633141-559a-468b-a44e-f311475eb580" alt="Power Query Editor" width="100%">
      <p align="center">Power Query Editor</p>
    </td>
    <td width="33%" valign="top">
      <img src="https://github.com/user-attachments/assets/78bf7fb2-25f6-4a9f-9805-5a0f69fcdb40" alt="Outlier Detection with DAX" width="100%">
      <p align="center">Outlier Detection with DAX</p>
    </td>
    <td width="33%" valign="top">
      <img src="https://github.com/user-attachments/assets/5c3fa33d-3448-4215-afcd-fe1ac2371f1c" alt="DAX for Date Table" width="100%">
      <p align="center">DAX for Date Table</p>
    </td>
  </tr>
</table>

*A snapshot of data transformation*

* **Data Source:** The analysis is based on the public [Uber NYC Rides Dataset from Kaggle](https://www.kaggle.com/datasets/ahmedramadan74/uber-nyc).
* **Data Validation & Cleaning:** Ensured data integrity by correcting data types and checking for errors. The dataset was filtered to isolate rides within NYC boroughs for a simulated reporting period of **June 2024**.
* **Outlier Handling:** A validation process was created to identify and flag outliers (e.g., trips with unusually long durations for short distances). These flagged trips were then excluded from all report calculations using the **Filter Pane** to ensure analytical accuracy.
* **Date Table:** A dedicated calendar dimension table was created using DAX to support time intelligence analysis, a Power BI best practice.

### 2. Data Modeling

![image](https://github.com/user-attachments/assets/a1890467-5e3b-4880-8a8d-a6dbcae8794f)

*Data model of this project*

* **Star Schema:** A **Star Schema** data model was implemented to optimize performance. A central Fact Table (`Trips`) is connected via one-to-many relationships to several Dimension Tables (`Date`, and `Location`).

### 3. DAX (Data Analysis Expressions)
* **Calculated Columns:** Created new columns directly in the data model, such as `Trip Duration (Seconds)`, calculated from the pickup and drop-off timestamps.
* **Measures:** Developed all measures needed to power the visuals and KPIs, including `Total Revenue`, `Total Trips`, and `Average Booking Value`.

![image](https://github.com/user-attachments/assets/69ccf8fd-88d9-40a5-b26f-18501a2aee7c)

*Measures*

### 4. Report Visualization & Interactivity

![power bi uber project](https://github.com/user-attachments/assets/628c08c4-eb3e-4e8b-b487-209879137121)

* **User-Centric Design:** All visuals and fields were given clear, business-friendly titles to enhance readability for non-technical stakeholders.
* **Custom Theme:** A custom dark-mode theme was designed with a specific color palette that aligns with Uber's branding for a professional and polished look.
* **Dynamic Interactivity:** The dashboard is fully interactive, utilizing:
    * **Slicers** to filter the entire report by Borough.
    * **Page Navigation** buttons for a seamless multi-page experience.
    * **Bookmarks** and buttons to allow users to toggle between different views on a single page (e.g., switching from "Peak Demand by Day" to "Peak Demand by Hour").

## 📂 Project Structure

The report is designed with a clear, multi-page structure for targeted analysis:
* **KPI Summary:** A high-level overview of key performance indicators and demand patterns.
* **Financials by Location:** A deep-dive into revenue, trip value, and surge pricing by borough.
* **Operational by Location:** An analysis of on-the-ground metrics like trip hotspots, duration, and on-road efficiency.

## 🚀 How to Use

As Power BI Service requires a license to publish reports publicly, this project can be viewed by running the files locally. Press ctrl before click a button.

**Prerequisites:**
* You must have **Microsoft Power BI Desktop** installed.

**Instructions:**
1.  Clone this repository to your local machine or download the source files.
2.  The repository includes both the Power BI file (`Your_File_Name.pbix`) and the raw dataset.
3.  Open the `.pbix` file in Power BI Desktop to view and interact with the full report.

## 👤 Contact
* **Author:** Adam Astiti
* **LinkedIn:** [linkedin.com/in/adam-astiti-a3787312a/](https://www.linkedin.com/in/adam-astiti-a3787312a/)
* **GitHub:** [github.com/adam-astiti](https://github.com/adam-astiti)
