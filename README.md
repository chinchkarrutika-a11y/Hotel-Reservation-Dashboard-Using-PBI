# 🏨 Hotel Reservation Analysis Dashboard

## 📊 Microsoft Power BI Project

An interactive **Hotel Reservation Analysis Dashboard** developed using **Microsoft Power BI** to analyze hotel bookings, revenue, customers, room performance, occupancy, and cancellations.

The project demonstrates the complete **Business Intelligence workflow**, from raw data cleaning and transformation to data modeling, DAX calculations, interactive visualization, and business insights.

---

## 🎯 Project Objective

The main objective of this project is to transform raw hotel reservation data into an interactive dashboard that helps hotel management understand:

* Revenue performance
* Booking volume
* Customer behavior
* Hotel performance
* Room performance
* Occupancy
* Booking cancellations
* New vs. repeat customers

The dashboard provides a centralized view of important KPIs and allows users to explore the data using interactive filters.

---

## 🛠️ Tools & Technologies

| Tool / Technology              | Purpose                                    |
| ------------------------------ | ------------------------------------------ |
| **Microsoft Power BI Desktop** | Dashboard development and visualization    |
| **Power Query**                | Data cleaning and transformation           |
| **DAX**                        | Measures, calculations, and business logic |
| **CSV**                        | Source datasets                            |
| **Star Schema**                | Data modeling                              |
| **Power BI Data Model**        | Relationships and analytical model         |

---

## 📁 Dataset

The project uses five main CSV datasets:

### 1. `reservations_large`

The main **Fact Table** containing reservation-level information.

Important fields include:

* Reservation ID
* Customer ID
* Hotel ID
* Room ID
* Booking Date
* Check-in Date
* Check-out Date
* Total Price

### 2. `customers_large`

Contains customer-related information:

* Customer ID
* Customer Name
* Email
* Phone
* Country

### 3. `hotels_large`

Contains hotel information:

* Hotel ID
* Hotel Name
* City
* Total Rooms

### 4. `rooms_large`

Contains room information:

* Room ID
* Room Type
* Capacity
* Base Price

### 5. `booking_history_large`

Contains booking status history.

A reservation can have multiple status records, such as:

* Confirmed
* Completed
* Cancelled

To handle this correctly, a separate **`Booking_Latest_Status`** table was created to identify the latest status for each reservation.

---

## 🧹 Data Cleaning

Data preparation was performed using **Power Query Editor**.

The major cleaning steps included:

* Checking and correcting data types
* Reviewing duplicate records
* Handling null values
* Removing unnecessary columns
* Standardizing column names
* Maintaining consistent data formatting
* Preparing the datasets for data modeling

The cleaned datasets were then loaded into the Power BI data model.

---

## 🏗️ Data Modeling

The project uses a **Star Schema** to organize the data.

### Fact Table

`reservations_large`

### Dimension Tables

* `customers_large`
* `hotels_large`
* `rooms_large`
* `Date`

### Supporting Table

* `Booking_Latest_Status`

A dedicated **Measures Table** was also created to keep DAX measures organized.

The model uses relationships based on relevant keys such as:

* `customer_id`
* `hotel_id`
* `room_id`
* `reservation_id`

This structure makes the model easier to maintain and supports efficient analytical calculations.

---

## 📐 DAX & KPIs

Several DAX measures were created to analyze hotel performance.

### Key KPIs

* **Total Revenue**
* **Total Bookings**
* **Total Customers**
* **Cancelled Bookings**
* **Cancellation Rate**
* **ADR**
* **Average Booking Value**
* **Occupancy Rate**

Additional logic was created to classify customers as:

* **New Customer**
* **Repeat Customer**

The `Booking_Latest_Status` logic ensures that status-based calculations use the latest available booking status.

---

## 📊 Dashboard Pages

The Power BI report contains multiple analytical pages.

### 🏠 Executive Dashboard

Provides an overall view of the hotel's performance through KPIs and interactive visuals.

Key metrics include:

* Total Revenue
* Total Bookings
* Total Customers
* ADR
* Occupancy Rate
* Cancellation Rate
* Cancelled Bookings

### 🏨 Hotel Performance

Used to compare hotel-level performance and analyze revenue and booking patterns.

### 👤 Customer Analysis

Provides insights into:

* Customer behavior
* Customer distribution
* New vs. repeat customers
* Booking patterns

### 🛏️ Room Performance

Analyzes room-related performance including:

* Room types
* Booking patterns
* Room utilization
* Revenue performance

---

## 🎛️ Interactive Filters

The dashboard includes interactive slicers that allow users to filter the analysis by:

* Hotel
* City
* Room Type
* Booking Date

All connected visuals update dynamically according to the selected filters.

---

## 💡 Business Insights

The dashboard can help hotel management:

* Monitor revenue performance
* Compare hotel performance
* Track booking trends
* Analyze cancellation behavior
* Understand customer behavior
* Identify repeat customers
* Monitor room utilization
* Support data-driven decision-making

Instead of relying on manual analysis, users can interact with the dashboard and quickly explore different business scenarios.

---

## 🚧 Challenges Faced

One of the main challenges was handling multiple booking status records for the same reservation.

A single reservation could have different status records over time. Using the latest status was important because using all status records directly could result in incorrect cancellation or booking-status analysis.

This was addressed by creating the:

`Booking_Latest_Status`

table to retain the latest status for each reservation.

Other challenges included:

* Designing an appropriate Star Schema
* Creating relationships between multiple datasets
* Developing reusable DAX measures
* Handling data quality issues
* Organizing measures using a dedicated Measures Table

---

## 🚀 Future Enhancements

Possible future improvements include:

* Connecting the dashboard to a live SQL database
* Publishing the report to Power BI Service
* Implementing Row-Level Security
* Adding predictive booking analysis
* Adding revenue forecasting
* Adding RevPAR analysis
* Adding Customer Lifetime Value analysis
* Creating a mobile-friendly dashboard

---

## 📂 Project Structure

```text
Hotel-Reservation-Analysis/
│
├── README.md
│
├── Dataset/
│   ├── reservations_large.csv
│   ├── customers_large.csv
│   ├── hotels_large.csv
│   ├── rooms_large.csv
│   └── booking_history_large.csv
│
├── PowerBI/
│   └── Hotel_Reservation_Analysis.pbix
│
├── Screenshots/
│   ├── Executive_Dashboard.png
│   ├── Hotel_Performance.png
│   ├── Customer_Analysis.png
│   └── Room_Performance.png
│
└── Documentation/
    └── Project_Report.pdf
```

> **Note:** Update the file names and folders according to the actual files uploaded to this repository.

---

## 🔄 Project Workflow

```text
Raw CSV Data
     ↓
Power Query
     ↓
Data Cleaning & Transformation
     ↓
Data Modeling
     ↓
Star Schema
     ↓
DAX Measures
     ↓
Interactive Dashboard
     ↓
Business Insights
```

---

## 📸 Dashboard Preview

### Executive Dashboard

*Add your Power BI dashboard screenshot here.*

```text
![Executive Dashboard](Screenshots/Executive_Dashboard.png)
```

### Hotel Performance

```text
![Hotel Performance](Screenshots/Hotel_Performance.png)
```

### Customer Analysis

```text
![Customer Analysis](Screenshots/Customer_Analysis.png)
```

### Room Performance

```text
![Room Performance](Screenshots/Room_Performance.png)
```

---

## 🎓 Key Learning Outcomes

Through this project, I gained practical experience in:

* Data cleaning using Power Query
* Data transformation
* Star Schema data modeling
* Creating relationships between tables
* Writing DAX measures
* Creating calculated tables and columns
* KPI development
* Interactive dashboard design
* Business-oriented data analysis
* Presenting analytical insights

---

## 👩‍💻 Author

**Rutika Chinchkar**

**Data Analyst | Computer Science Postgraduate**

### Skills Demonstrated

`Power BI` · `Power Query` · `DAX` · `Data Cleaning` · `Data Modeling` · `Data Visualization` · `Business Intelligence`

---

## ⭐ Project Purpose

This project was developed as a practical **Business Intelligence and Data Analytics project** to demonstrate the ability to transform raw datasets into a structured analytical solution using Microsoft Power BI.


## Dashboard Preview

### Main Dashboard
![Main Dashboard](Screenshots/Dashboard.png)

### Detailed Analysis
![Detailed Analysis](Screenshots/Detailed-Analysis.png)

### Customer Analysis
![Customer Analysis](Screenshots/Customer-Analysis.png)
