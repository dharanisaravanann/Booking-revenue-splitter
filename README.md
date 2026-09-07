# Booking Revenue Splitter

A Streamlit web app that converts reservation-level booking data into daily stay entries with revenue calculated per night.

---

## Introduction

**Booking Revenue Splitter** is a self-service reporting tool built for property managers, hotels, serviced apartments, and operations teams who need to analyse revenue on a per-night basis rather than per-booking. No Python knowledge is needed to use it — upload an Excel file, get a clean Excel file back.

**Note:** the tool expects reservation-level data with defined Arrival, Departure, and Revenue columns (see Required Input Columns below) — it won't work on data that doesn't follow this structure.

---

## How It Works

1. Upload a `.xlsx` reservation file
2. The app:
   - Cleans column names
   - Converts Arrival / Departure / Booking Date to proper date format
   - Expands each booking into individual stay dates (Arrival → Departure − 1 day)
   - Computes nightly revenue by dividing Base Revenue and Total Revenue by number of nights
3. Download the resulting Excel file, which includes two sheets: **Original Data** and **Daily Split Data**

---

## System Requirements

- **Python:** 3.9 – 3.12
- **Dependencies:** Streamlit, Pandas, openpyxl

---

## Installation

**1. Clone the repository**

```
git clone https://github.com/dharanisaravanann/booking-revenue-splitter.git
```

**2. Install dependencies**

```
pip install -r requirements.txt
```

**3. Run the app**

```
streamlit run app.py
```

---

## Required Input Columns

Your input file must contain these columns:

- `Reservation Number`
- `Apartment`
- `Guest Name`
- `Channel`
- `Arrival`
- `Departure`
- `Booking Date`
- `Nights`
- `Base Revenue`
- `Total Revenue`

---

*Built during my Data Science internship at OMNIYAT, where this tool was adopted by multiple business teams for self-service revenue reporting.*
