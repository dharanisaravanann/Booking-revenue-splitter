Booking Revenue Splitter

A Streamlit web app that converts reservation-level booking data into daily stay entries with revenue per night — built for property managers, hotels, serviced apartments, and operations teams who need to analyse revenue on a per-night basis, with no Python knowledge required.

Upload an Excel file → get back a clean Excel output with the original data plus a daily-level split, ready for reporting.

Features
Splits reservations into daily rows — for each booking, generates one row per stay date between Arrival and Departure − 1 day
Calculates revenue per night — divides Base Revenue and Total Revenue by number of nights for a consistent nightly value
Clean Excel output — downloaded file includes two sheets: Original Data and Daily Split Data
Consistent date formatting — all dates standardised to dd-mm-yyyy
How It Works
Upload a .xlsx reservation file
The app cleans column names, converts Arrival/Departure/Booking Date to proper date format, expands each booking into individual stay dates, and computes nightly revenue
Download the resulting Excel file with daily-level entries
Required Input Columns

Your file must include:

Reservation Number, Apartment, Guest Name, Channel, Arrival, Departure, Booking Date, Nights, Base Revenue, Total Revenue

Tech Stack

Python, Streamlit, Pandas

Built during my Data Science internship at OMNIYAT, where this tool was adopted by multiple business teams for self-service revenue reporting.
