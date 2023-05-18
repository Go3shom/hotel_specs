# Hotel Reservation System Request

## Customer

- Can _create_ a new **Account**
- Can _search for_ **Available Rooms** based on desired **Dates** and **Location**.
- Can _view_ **Room Details**
  1. Amenities
  2. Prices
  3. Photos
- Can _select_ their preferred **Room Types**
- Can _make_ **Bookings**
- Can _modify_ their **Reservations**
- Can _cancel_ their **Reservations**
- Can _view_ their **Booking History**
- Should have **Online Booking** and **Payment Options**
  1. Pay Online
  2. Pay at Hotel

---  

## Hotel staff

### 1) Administrator/Manager

- Can _manage_ **User Accounts**
- Can _set up_ **Room Types** and **Rates**
- Can _configure_ **System Settings**
- Can _generate_ **Reports** on **System Performance**.

### 2) Front Desk Agent

- Can _handle_ guest **CheckIns**
- Can _handle_ guest **CheckOuts**
- Can _handle_ guest **Reservations**.
- Have _access_ to _view_ **Room Availability**
- Have _access_ to _manage_ **Room Availability**
- Have _access_ to _assign_ **Rooms** to guests
- Have _access_ to _handle_ **Booking Modifications**.
- Have _access_ to _handle_ **Booking Cancellations**.

### 3) Housekeeping Staff

- Can _view_ **Room** _Occupancy_
- Can _manage_ the _status_ of **Rooms**.
- Can _block_ **Rooms** for _Maintenance_ purposes.
- Can _view_ **Room** _Maintenance Schedules_
- Can _manage_ the _cleanliness_ of **Rooms**.
- Can _mark_ **Rooms** as _clean_ or _dirty_

### 4) Reservation Manager

- Can _supervise_ **Reservation Process**
- Have _access_ to _view_ **Bookings**
- Have _access_ to _manage_ **Bookings**
- Have _access_ to _assign_ **Rooms**
- Can _handle_ customer _inquiries_ or _issues_.
- Can _generate_ **Reports** on **Reservation Statistics**

### 5) Finance/Accounting Staff

- Can _handle_ **Financial Transactions** and **Revenue Management**
- Can _access_ **Financial Reports**
- Cam _view_ **Payment Details**
- Can _generate_ **Revenue Related reports**.

### 6) Reporting Analyst

- Can _analyze_ **Data**
- Can _generate_ various **Reports** for **Management** purposes.
- Have _access_ to **Detailed Reports** on **Occupancy Rates**, **Revenue**, **Customer Feedback**, and other relevant metrics.

---

## Room

- **Room Status**
  1. Available
  2. Occupied
  3. Reserved
  4. Under Maintenance
    a. Fixing plumbing issues
    b. Upgrading room amenities
  5. Out of Service
    a. Structural repairs that require a significant amount of time
  
- **Room Availability**
  1. Available **Room** on specific **Date**

- **Food** [I don't know about it, btw 😁]

---

## DB Tables

1. users [user_id, username, email, password, role_id]
2. roles [role_id, role_name]
3. rooms [room_id, room_number, room_type, description, price_per_night]
4. photos [photo_id, photo_path, room_id]
5. bookings [booking_id, user_id, room_id, check_in_date, check_out_date, total_price, payment_status]
6. payments [payment_id, booking_id, payment_date, amount]
7. room_status [status_id, status_name]
8. room_availability [room_id, status_id, date, available_quantity]
