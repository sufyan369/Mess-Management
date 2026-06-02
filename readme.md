# 🍽️ Mess Duty Register

A lightweight, browser-based **Mess Management & Meal Counting System** designed for hostels, colleges, mess committees, and student coordinators.

The application automatically parses WhatsApp meal-registration messages and generates meal-wise attendance reports for Breakfast, Lunch, Snack, and Dinner.

---

# 📌 Project Overview

Mess Duty Register helps mess coordinators avoid manual counting of meal requests.

Students usually send meal requirements through WhatsApp groups. Counting them manually is time-consuming and prone to mistakes.

This application allows the coordinator to:

* Paste WhatsApp chat messages
* Automatically identify students
* Detect meal selections
* Count meal totals
* Generate student-wise reports
* Print daily mess reports

Everything runs completely in the browser with no server required.

---

# 🎯 Objectives

The main objectives of this project are:

1. Automate meal counting.
2. Reduce manual errors.
3. Save time for mess duty staff.
4. Generate instant meal reports.
5. Maintain student-wise meal records.
6. Support custom meal keywords and abbreviations.

---

# 🚀 Features

## WhatsApp Chat Parsing

Supports common WhatsApp exported chat formats.

Example:

[11:03 AM, 02/06/2026] Afsal: B

[11:05 AM, 02/06/2026] Niyas: Lunch

[11:07 AM, 02/06/2026] Sameer: D

The system automatically extracts:

* Student Name
* Meal Selection

---

## Meal Categories

The application supports four meal types:

| Meal      | Description        |
| --------- | ------------------ |
| Breakfast | Morning meal       |
| Lunch     | Afternoon meal     |
| Snack     | Evening tea/snacks |
| Dinner    | Night meal         |

---

## Automatic Meal Counting

The system calculates:

* Total Breakfast Count
* Total Lunch Count
* Total Snack Count
* Total Dinner Count
* Total Students
* Total Meals

---

## Student-wise Breakdown

Each student receives a dedicated record showing:

* Breakfast Status
* Lunch Status
* Snack Status
* Dinner Status
* Total Meals Selected

Example:

| Student | B | L | S | D |
| ------- | - | - | - | - |
| Afsal   | ✓ | - | - | - |
| Niyas   | - | ✓ | - | ✓ |

---

## Duplicate Student Handling

If a student appears multiple times in the chat:

Afsal: B

Afsal: D

The system merges records and stores:

Afsal → Breakfast + Dinner

This prevents duplicate counting.

---

## Custom Meal Keywords

Administrators can define custom aliases.

Example:

Breakfast Aliases

* B
* Breakfast
* Brkfst
* Bfast
* BK

Lunch Aliases

* L
* Lunch
* LN

Snack Aliases

* S
* Snack
* Tea
* Evening

Dinner Aliases

* D
* Dinner
* Supper
* Night

New keywords can be added directly through the UI.

---

## Local Storage Support

Custom meal aliases are stored using browser Local Storage.

Benefits:

* No database required
* Settings persist after page refresh
* Offline support

---

## Unrecognized Keyword Detection

If students type unsupported keywords:

Example:

Afsal: Brekfst

The system displays:

⚠ Unrecognized Keyword

allowing administrators to add it as a valid alias.

---

## Print-Friendly Reports

The application includes a print mode.

Print reports include:

* Meal counts
* Student lists
* Daily summary

Buttons and editing controls are automatically hidden during printing.

---

# 🏗️ System Architecture

User
│
▼
Paste WhatsApp Chat
│
▼
Chat Parser
│
▼
Keyword Matching Engine
│
▼
Meal Classification
│
▼
Student Record Generation
│
▼
Count Calculation
│
▼
Report Generation
│
▼
Print / Export

---

# ⚙️ Technologies Used

## Frontend

* HTML5
* CSS3
* JavaScript (Vanilla JS)

## Browser APIs

* Local Storage API
* Print API

## Deployment

Can be hosted on:

* GitHub Pages
* Netlify
* Vercel
* Firebase Hosting
* Any static web server

---

# 📂 Project Structure

mess-duty-register/

├── index.html

├── styles.css (embedded)

├── script.js (embedded)

└── README.md

---

# 🧠 Core Functional Modules

## 1. Chat Parser

Responsible for:

* Reading pasted chat data
* Splitting lines
* Identifying names
* Identifying messages

---

## 2. Alias Management

Responsible for:

* Managing meal keywords
* Adding custom aliases
* Removing aliases
* Resetting aliases

---

## 3. Meal Matching Engine

Converts:

B → Breakfast

L → Lunch

S → Snack

D → Dinner

---

## 4. Student Record Manager

Stores:

Student Name

Selected Meals

Uses JavaScript Set() to avoid duplicate meals.

---

## 5. Report Generator

Creates:

* Meal Cards
* Summary Statistics
* Student Tables
* Unrecognized Keyword Reports

---

# 📊 Sample Workflow

Step 1

Paste WhatsApp chat.

Step 2

Click:

Parse & Count

Step 3

System processes messages.

Step 4

Meal counts are calculated.

Step 5

Student report is generated.

Step 6

Print or save report.

---

# 🔒 Data Privacy

The application is fully client-side.

No data is:

* Uploaded
* Shared
* Stored on a server

All processing happens inside the user's browser.

---

# ✅ Advantages

* Simple UI
* Fast processing
* No internet required after loading
* No database required
* Easy deployment
* Printable reports
* Customizable meal keywords
* Works on desktop and mobile browsers

---

# 🔮 Future Enhancements

Potential future improvements:

### Export Features

* PDF Export
* Excel Export
* CSV Export

### Database Support

* Student Database
* Meal History
* Attendance Records

### Authentication

* Admin Login
* Role Management

### Analytics

* Daily Trends
* Monthly Reports
* Consumption Statistics

### Cloud Integration

* Firebase
* MySQL
* PostgreSQL

### Notifications

* WhatsApp Integration
* Email Reports
* SMS Alerts

---

# 👨‍💻 Developed For

Hostel Mess Management

College Mess Committees

Student Duty Coordinators

Residential Institutions

Educational Hostels

---

# License

This project is open-source and can be modified, distributed, and used for educational or institutional purposes.

© Mess Duty Register Project
