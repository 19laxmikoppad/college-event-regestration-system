# 🏆 College Event Registration System
<img width="1200" height="1600" alt="WhatsApp Image 2026-07-22 at 4 13 00 PM" src="https://github.com/user-attachments/assets/cebfea15-05a4-4e92-9912-b4638c10f822" />

A full-stack, frosted-glass themed web application built with **Flask**, **SQLite**, **Tailwind CSS**, and **Bootstrap**. Designed specifically for college symposiums, hackathons, and inter-collegiate championships where teams of **exactly 12 students** from the same institution register across **4 sub-events**.

---

## 🌟 Key Features

* **Strict 12-Member Team Roster**: Enforces exact squad size (12 members) with mandatory fields (full name, phone, department, year of study, and sub-events) for each student.
* **Email Uniqueness & Validation**: Validates email formatting and checks against existing database records and current payload entries to prevent duplicate registrations.
* **Automatic Unique Team Naming**: Generates memorable team names using college abbreviations, random descriptors, and unique codes (e.g., `Imperial Thunder Hawks`, `ABC-2026-Team-8472`).
* **Interactive UI/UX**:
  * Real-time progress tracker and member completion indicators.
  * One-click **Auto-Fill Sample Data** button for fast testing.
  * Frosted glass aesthetic with backdrop blurring, glowing dark-mode ambient orbs, and custom scrollbars.
* **Organizer Admin Dashboard**:
  * Password-protected access (`admin123`).
  * Summary metrics: total teams, total student participants, and sub-event selection counts.
  * Live search and filtering across team names, college names, registration IDs, or leader emails.
  * One-click **CSV Data Export** (`college_event_registrations.csv`).
* **Printable Registration Receipts**: Detailed receipt view displaying squad cards, sub-event badges, and registration IDs.

---

## 📁 Project Structure

```text
├── app.py                  # Main Flask server & API route handlers
├── database.py             # SQLite schema initialization & database operations
├── requirements.txt        # Python dependency specifications
├── README.md               # Project documentation
├── templates/              # HTML Jinja layout & views
│   ├── base.html           # Master layout template (Frosted Glass theme)
│   ├── index.html          # Registration form (12-member squad)
│   ├── success.html        # Registration receipt & confirmation card
│   ├── admin.html          # Organizer management dashboard
│   └── admin_login.html    # Password login for organizer admin
├── static/                 # Static web assets
│   ├── css/
│   │   └── style.css       # Custom glassmorphism styles
│   └── js/
│       └── main.js         # Dynamic form validation & sample filler
└── src/                    # React / TypeScript implementation (optional frontend)
    ├── App.tsx             # React main application entry
    └── lib/
        └── db.ts           # LocalStorage database helper for client mode
