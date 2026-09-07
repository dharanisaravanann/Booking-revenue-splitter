# Booking Revenue Splitter

A Streamlit web app that converts reservation-level booking data into daily stay entries with revenue and fees allocated per night.

---

## Introduction

**Booking Revenue Splitter** is a self-service reporting tool built for property managers, hotels, serviced apartments, and operations teams who need to analyse revenue on a per-night basis rather than per-booking. No Python knowledge is needed to use it — upload an Excel file, get a clean Excel file back.

**Note:** only `Reservation Number`, `Arrival`, `Departure`, and `Booking Date` are strictly required in your input file. Revenue and fee columns (see below) are optional — any of them present in your file will be split evenly across nights automatically.

---

## How It Works

1. Upload a `.xlsx` reservation file
2. The app:
   - Cleans column names and parses Arrival, Departure, and Booking Date (day-first format)
   - Expands each booking into one row per stay night (Arrival → Departure − 1 day)
   - Converts stay dates and booking dates into Excel DATEVALUE format for spreadsheet compatibility
   - Divides all revenue and fee columns present in the file evenly across the number of nights
   - Renames split columns to `<Column> per Night` and `Channel` to `Sub Channel`
3. Download the resulting Excel file, which includes two sheets: **Original Data** and **Reservations Daily Split**

---

## System Requirements

- **Python:** 3.9+
- **Dependencies:** streamlit, pandas, openpyxl

---

## Installation

**1. Clone the repository**

```
git clone https://github.com/dharanisaravanann/Booking-revenue-splitter.git
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

Your input file **must** contain:

- `Reservation Number`
- `Arrival`
- `Departure`
- `Booking Date`

Optional columns, split evenly per night if present:

- `Base Revenue`, `Total Revenue`, `Room Revenue`, `SC on Room Revenue`, `VAT on Room Rev`, `VAT on SC`, `Cleaning Fees Without VAT`, `VAT on Cleaning Fees`, `Tourism Dirham Fees`, `Cleaning Fees`

Also supported (passed through, not split): `Apartment`, `Guest Name`, `Channel`

---

*Built during my Data Science internship at OMNIYAT, where this tool was adopted by multiple business teams for self-service revenue reporting.*
