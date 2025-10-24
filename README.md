# OLA-Dashboard

A Power BI based dashboard built for visualising and analysing ride-booking data from OLA Cabs.  
This dashboard enables business users and analysts to monitor key metrics such as total rides, cancellations, sources of cancellation, ride trends over time, and more.

---

## 🚀 Key Features

- Interactive visuals in **Power BI** for exploring ride-level data and trends.  
- Metrics such as total bookings, cancelled bookings, and cancellation percentage.  
- Ability to filter by dates, ride status, ride type, and other dimensions.  
- Drill-down capabilities to explore cancellations by customer vs driver.  
- Clean, readable visuals suitable for business stakeholders.

---

## 📊 Data & Metrics

### Data Source  
- The dataset is expected to be a flat table (e.g., `July` table) containing ride-level records.  
- Key columns include: `Booking_Status`, `Cancel_By_Customer`, `Cancel_By_Driver`, timestamps, ride identifiers, and other ride attributes.

### Sample Metrics  
- **Total Bookings** = COUNTROWS( July )  
- **Cancelled Bookings** = CALCULATE( COUNTROWS( July ), July[Booking_Status] IN { "Canceled_Rides_by_Customer", "Canceled_Rides_by_Driver" } )  
- **Cancellation %** = DIVIDE( [CancelledBookings], [TotalBookings], 0 )

---

## 🛠 Setup & Installation

1. Clone or download this repository  
   ```bash
   git clone https://github.com/kunshbhatia/OLA-Dashboard.git
