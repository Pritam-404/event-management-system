# 🎓 EventHub — College Event Management System

A full-featured web application for managing college events with QR-based entry and real-time attendance tracking.

## ✨ Features

### Student Side
- Browse all upcoming events
- Register with name, email, phone, college ID
- Receive a unique QR code after registration
- Download QR code for event entry

### Admin Side
- Secure login (default: `admin` / `admin123`)
- Create, edit, delete events
- View all registrations per event
- Real-time QR code check-in scanner (camera-based)
- Manual QR data entry for testing
- Live attendance dashboard
- Export attendance as **CSV** or **PDF**

## 🚀 Quick Start

### 1. Install dependencies
```bash
pip install -r requirements.txt
```

### 2. Run the app
```bash
python app.py
```

### 3. Open in browser
```
http://localhost:5000
```

## 🗂️ Project Structure
```
college-event-system/
├── app.py                  # Flask backend + all routes
├── database.db             # SQLite DB (auto-created)
├── requirements.txt
├── qr_codes/               # Generated QR images
├── templates/
│   ├── base.html           # Shared layout
│   ├── index.html          # Event listing page
│   ├── register.html       # Student registration
│   ├── confirmation.html   # Post-registration + QR display
│   ├── admin_login.html    # Admin auth
│   ├── admin.html          # Admin dashboard
│   ├── event_form.html     # Create/edit event form
│   ├── registrations.html  # Per-event registrations list
│   ├── checkin.html        # QR scanner page
│   └── attendance.html     # Attendance log
└── static/
    ├── style.css
    └── script.js
```

## 🔐 Admin Credentials
| Field | Value |
|---|---|
| Username | `admin` |
| Password | `admin123` |

## 📦 Tech Stack
- **Backend**: Python / Flask
- **Database**: SQLite
- **QR Generation**: `qrcode[pil]`
- **PDF Export**: `reportlab`
- **QR Scanning**: `html5-qrcode` (browser camera)
- **Frontend**: HTML5 + CSS3 + Vanilla JS

## 🔄 Workflow
1. Admin creates event via Admin Panel
2. Students register on the public events page
3. Each student gets a unique QR code
4. At the event, admin opens Check-in page and scans QRs
5. System marks attendance in real-time
6. Admin exports attendance report as CSV or PDF
