# 🚄 Vande Bharat Express – Train Passenger Performance Dashboard

<p align="center">
  <img src="https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?style=for-the-badge&logo=powerbi&logoColor=black" />
  <img src="https://img.shields.io/badge/Data%20Analytics-Project-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/DAX-Measures-purple?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Excel-Dataset-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white" />
</p>

<p align="center">
  An interactive Power BI dashboard for analyzing Vande Bharat Express passenger trends, revenue, occupancy, train performance, and operational efficiency.
</p>

<p align="center">
  **📊 <a href="ADD_YOUR_POWER_BI_LIVE_LINK_HERE">View Live Interactive Dashboard</a>**
</p>

---

## 📌 Project Overview

The **Vande Bharat Express Train Passenger Performance Dashboard** is an end-to-end data analytics project developed using Microsoft Power BI.

The project focuses on analyzing booking and operational data to uncover meaningful insights into passenger demand, revenue generation, occupancy rates, train speed, delays, and route performance.

It transforms raw Excel data into interactive visualizations and KPI reports to support data-driven analysis and performance monitoring.

## 🎯 Project Objectives

- Analyze overall passenger and booking trends.
- Monitor total revenue and route-wise revenue performance.
- Evaluate train occupancy and average speed.
- Track delays and on-time performance.
- Identify the busiest train and highest-revenue route.
- Compare passenger demand across travel classes.
- Explore performance across different states and routes.

## ✨ Dashboard Features

- **KPI Overview:** Total Passengers, Total Revenue, Average Occupancy, Average Speed, On-Time Percentage, and Average Delay.
- **Passenger Analysis:** Passenger trends and monthly booking patterns.
- **Revenue Analysis:** Revenue trends and highest-revenue route identification.
- **Train Performance:** Busiest train, train-wise passenger count, and operational metrics.
- **Route Analysis:** Route-wise passenger demand, revenue, and occupancy.
- **Class-wise Analysis:** Executive Class and Chair Car passenger distribution.
- **Operational Insights:** Delay analysis and on-time performance tracking.
- **Interactive Filters:** Explore the dashboard using available slicers for dates, states, routes, trains, and passenger categories.

## 📊 Key Performance Indicators

| KPI | Description |
|---|---|
| Total Passengers | Total passengers recorded |
| Total Revenue | Revenue generated from bookings |
| Average Occupancy | Average train occupancy percentage |
| Average Speed | Average train speed in km/h |
| On-Time Percentage | Percentage of on-time records |
| Average Delay | Average delay in minutes |
| Total Trains | Unique trains in the dataset |
| Total Bookings | Unique booking records |

## 🔍 Key Insights

- Overall passenger demand and revenue performance can be monitored through monthly trends.
- Route-wise analysis helps identify high-revenue corridors.
- Train-level analysis highlights the busiest train based on passenger volume.
- Class-wise analysis compares demand for Executive Class and Chair Car.
- On-time performance and average delay provide operational performance indicators.
- Occupancy analysis helps compare passenger demand across routes and trains.

## 🗂️ Dataset & Data Model

The project uses an Excel dataset containing three tables:

| Table | Purpose |
|---|---|
| Fact_Bookings | Booking, passenger, revenue, and operational details |
| Train_Master | Train-related information |
| State_Master | State-related information |

**Dataset coverage:** 100,000 booking records, 164 trains, and 23 states, covering January–May 2026.

### Data Model Relationships

- `Train_Master[Train_No]` → `Fact_Bookings[Train_No]`
- `State_Master[State]` → `Fact_Bookings[State]`

Both relationships use a one-to-many data model, with the master tables on the one side.

## 📐 DAX Measures

Some of the key DAX measures used in the dashboard:

```dax
Total Passengers =
SUM(Fact_Bookings[Passengers])

Total Revenue =
SUM(Fact_Bookings[Revenue])

Total Trains =
DISTINCTCOUNT(Fact_Bookings[Train_No])

Total Bookings =
DISTINCTCOUNT(Fact_Bookings[Booking_ID])

Average Occupancy =
AVERAGE(Fact_Bookings[Occupancy_%])

Average Speed =
AVERAGE(Fact_Bookings[Speed_kmph])

Average Delay =
AVERAGE(Fact_Bookings[Delay_Minutes])

On-Time Percentage =
DIVIDE(
    CALCULATE(
        COUNTROWS(Fact_Bookings),
        Fact_Bookings[On_Time] = TRUE()
    ),
    COUNTROWS(Fact_Bookings),
    0
)
```

## 🛠️ Tools & Technologies

| Technology | Usage |
|---|---|
| Microsoft Power BI | Dashboard development and visualization |
| Power Query | Data cleaning and transformation |
| DAX | Measures and KPI calculations |
| Microsoft Excel | Dataset and source data |
| Data Modeling | Table relationships and analytical structure |

## 🚀 How to Use This Project

1. Clone this repository:

```bash
git clone https://github.com/khilenderrajput/Vandhe-Bharat-Train-Passenger-Performance.git
```

2. Open the project folder.
3. Open the `.pbix` file using Power BI Desktop, if included in the repository.
4. If needed, connect the Excel dataset.
5. Check the relationships between the three tables.
6. Refresh the data and explore the interactive dashboard.

## 📊 Live Dashboard

**Explore the interactive Power BI dashboard:**

🔗 [Click Here – Live Dashboard](ADD_YOUR_POWER_BI_LIVE_LINK_HERE)

## 👨‍💻 Author

**Khilender Rajput**

Aspiring Data Analyst | Data Analytics Enthusiast

- GitHub: [@khilenderrajput](https://github.com/khilenderrajput)
- LinkedIn: [Khilender Rajput](https://www.linkedin.com/in/khilender-rajput-936519337/)
- LeetCode: [Khilender Rajput](https://leetcode.com/u/Khilender_rajput/)

---

## ⚠️ Dataset Disclaimer

This project uses synthetic/illustrative data for educational and portfolio purposes. The dataset does not represent official Indian Railways operational or financial records.

---

<p align="center">
  ⭐ If you find this project useful, consider giving this repository a star!
</p>
