# 🎟 Event Ticket Booking & QR Verification System

A complete **online event ticket booking system** that allows users to purchase tickets online using a payment gateway and receive a **unique ticket code and QR code** via email.
Event staff can verify tickets at the venue using **QR code scanning or manual code verification** to mark attendees.

This project demonstrates **real-world booking workflow, payment integration, QR verification, and role-based event management**.

---

# 📌 Project Overview

Event organizers often need a secure way to **sell tickets online and verify attendees during the event**.
This system solves that problem by providing:

* Online ticket booking
* Secure payment processing
* Unique ticket code generation
* QR code based ticket verification
* Event staff attendance management

The platform includes **three main roles**:

* Customer
* Admin
* Event Staff / Member

---

# 🎯 Key Features

## Customer Features

* Browse upcoming events
* View event details
* Purchase tickets online
* Secure payment gateway checkout
* Receive booking confirmation email
* Receive **unique ticket code**
* Receive **QR code ticket**
* Show QR code at event entrance

---

## Admin Features

* Admin dashboard
* Create and manage events
* View all ticket registrations
* Import unique ticket codes
* Manage bookings
* Assign event staff members
* Track ticket usage
* Monitor event attendance

---

## Event Staff Features

Each event can have **dedicated event members (staff)**.

Event members can:

* Login to event dashboard
* Scan ticket QR codes
* Verify ticket codes manually
* Mark attendee as **attended**
* Prevent duplicate entries

---

# 🎫 Unique Ticket Code System

Admin can upload or generate **unique ticket codes** for events.

Example:

```
EVT-98234
EVT-98235
EVT-98236
EVT-98237
```

When a ticket is purchased:

1. System assigns an **unused ticket code**
2. Code is linked to the order
3. Ticket status changes to **confirmed**
4. Code is emailed to the customer

---

# 📱 QR Code Ticket System

After payment confirmation, the system automatically generates a **QR code ticket**.

The QR code contains:

* Ticket ID
* Unique Ticket Code
* Event ID
* Customer Email

This QR code is sent to the customer via email and can be scanned during the event.

---

# ✅ Ticket Verification Process

## QR Code Scan

Event staff scans the QR code at the entrance.

System verifies:

* Ticket exists
* Ticket belongs to the correct event
* Ticket has not already been used

If valid:

```
Status: Valid Ticket
Attendance: Marked
```

---

## Manual Code Entry

Staff can also verify tickets manually by entering the unique ticket code.

Example:

```
Enter Code: EVT-98234
```

System verifies and marks the ticket as attended.

---

# 📊 Attendance Tracking

Ticket statuses include:

```
Available
Reserved
Confirmed
Attended
Invalid
```

Admin dashboard displays:

* Total tickets sold
* Total attendees checked-in
* Remaining tickets

---

# 🏗 System Architecture

```
Customer Browser
       │
Frontend Interface
(HTML, CSS, JavaScript)
       │
Laravel / PHP Backend
       │
Payment Gateway
(Stripe / Razorpay)
       │
MySQL Database
       │
QR Code Generator
       │
Email Notification System
       │
Event Staff Dashboard
```

---

# 🗄 Database Structure

## Users

```
id
name
email
password
role
created_at
```

---

## Events

```
id
title
description
date
location
price
total_tickets
created_at
```

---

## Orders

```
id
user_id
event_id
quantity
total_price
payment_status
payment_id
created_at
```

---

## Ticket Codes

```
id
event_id
unique_code
qr_code
status
order_id
attended_at
```

---

## Event Members

```
id
event_id
name
email
password
role
```

---

# 💻 Tech Stack

### Backend

* Laravel / PHP

### Frontend

* HTML5
* CSS3
* Bootstrap
* JavaScript
* AJAX

### Database

* MySQL

### Integrations

* Payment Gateway (Stripe / Razorpay)
* QR Code Generator
* Email SMTP

### Tools

* Git
* GitHub

---

# 📷 Screenshots

Add screenshots in the **/screenshots folder**

Examples:

```
screenshots/
homepage.png
event-details.png
checkout.png
payment-success.png
admin-dashboard.png
qr-ticket.png
qr-scan.png
```

---
