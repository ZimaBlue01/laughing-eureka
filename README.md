# ✈️ Airline Booking System  
*A Database Design & Normalisation Project by Muhammed Uwais Adam*

## 📌 Overview  
This project presents the full database design, entity-relationship modelling, and normalisation process for an **online flight booking system** for a South African Airline Booking Agency. The system allows customers to:

- View flights by **date, time, class, capacity, price, departure and arrival points**
- Register as a customer
- Make bookings if registered  
- View availability based on capacity and ticket status  
- Process payments using various payment methods  

The project includes the **initial ERD**, **full 1NF → 2NF → 3NF normalisation**, the **final ERD**, and **mapping to relational tables**.  
All documentation, diagrams, and entity explanations are contained in the accompanying PDF.  
  
## 🎯 Project Purpose  
The goal of this system is to design a clean, normalised, and efficient database capable of handling:

- Flight information  
- Seat and ticket availability  
- Customer registration  
- Bookings and booking details  
- Passengers per booking  
- Payment options and transactions  
- Session tracking (registered & unregistered users)

The project ensures **data integrity**, **eliminates redundancy**, and demonstrates full understanding of structured database design.  

---

## 🧩 Key Entities & Their Roles

### 🛫 **Flight Details**
Central entity storing:
- Flight ID, date, time  
- Departure & arrival points  
- Class & price  
- Availability  



---

### 📊 **Flight Availability & Ticket Availability**
Two-step availability logic:

1. **Flight Availability**  
   - Ensures capacity is not exceeded.

2. **Ticket Availability Status**  
   - Double-checks final availability at ticket level.  


---

### 🎟️ **Ticket & Passenger Ticket**
- Tickets include flight number, customer name, and travel date.
- Passenger Ticket acts as an **intersection entity**:
  - Linking tickets to passengers  
  - Assigning a boarding gate  


---

### 🧍‍♂️ **Passengers**
Stores passenger names and ages.  
A single booking may include multiple passengers.  
:contentReference[oaicite:5]{index=5}

---

### 📘 **Flight Booking**
A key entity that ties together:
- Flight details  
- Ticket ID  
- Booking ID  
This creates a complete view of a customer's booking.  


---

### 🧾 **Booking & Booking Detail**
- Booking stores flight name, customer name, and discount eligibility.
- Booking Detail connects the booking to the registered customer's ID.  


---

### 👤 **Registered & Unregistered Customers**
- Registered customers have:  
  - ID number, passport number, email, phone  
  - Postal addresses (via intersection entity **Customer Postal**)  
- Unregistered customers receive a **visitor ID** and can only view flights, not book.  


---

### 💳 **Payment & Payment Options**
- Payments store:
  - Payment date  
  - Customer ID  
  - Payment method  
- Payment Options include: VISA, EFT, etc.  


---

### 🧭 **Session**
Tracks:
- Visitor or customer interaction  
- Flight viewed  
- Whether user is registered or not  
This allows the agency to analyse user behaviour.  


---

## 🧮 Normalisation  
The project includes full normalisation to **Third Normal Form (3NF)**:

### ✔ **1NF:**  
All repeating groups removed.  
Fields atomic and clearly defined.

### ✔ **2NF:**  
All partial dependencies removed.  
Composite keys resolved where necessary.

### ✔ **3NF:**  
All transitive dependencies removed.  
Clean, dependency-free schema produced.

This ensures a stable, scalable database with no redundancy.  


---

## 🗂️ Final ERD & Mapping to Tables  
The final ERD is fully normalised and includes:

- Primary keys for each entity  
- Foreign keys for relationships  
- Support for many-to-many links through intersection entities  
- Accurate modelling of business logic  

All relational tables are mapped with:

- Column names  
- Key types  
- Null constraints  
- Sample data  
- Entity relationships  

