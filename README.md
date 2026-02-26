# 🛡️ Women Safety AI App

A full-stack AI-powered women safety web application built with **HTML/CSS/JavaScript** (frontend) and **Node.js + Express + MySQL** (backend).

---

## 📁 Project Structure

```
women safety/
├── frontend/                  # Frontend (HTML + CSS + JS)
│   ├── css/
│   │   └── style.css          # Global design system
│   ├── js/
│   │   └── utils.js           # Shared utilities & API helpers
│   ├── login.html             # Login page
│   ├── register.html          # Registration page
│   ├── dashboard.html         # Main safety dashboard
│   ├── emergency.html         # Emergency center
│   ├── contacts.html          # Emergency contacts management
│   ├── history.html           # Alert history & analytics
│   └── fake-call.html         # Fake call escape tool
│
├── backend/                   # Backend (Node.js + Express)
│   ├── config/
│   │   └── database.js        # MySQL/Sequelize connection
│   ├── models/
│   │   ├── User.js            # User model
│   │   ├── EmergencyAlert.js  # Emergency alerts model
│   │   ├── EmergencyContact.js# Emergency contacts model
│   │   ├── LocationHistory.js # Location tracking model
│   │   └── SafeZone.js        # Safe zones model
│   ├── controllers/
│   │   ├── authController.js  # Auth logic
│   │   ├── emergencyController.js # Emergency + AI Risk
│   │   └── contactController.js   # Contacts CRUD
│   ├── middleware/
│   │   └── authMiddleware.js  # JWT auth middleware
│   ├── routes/
│   │   ├── authRoutes.js
│   │   ├── emergencyRoutes.js
│   │   └── contactRoutes.js
│   ├── .env                   # Environment variables
│   ├── server.js              # Main server entry
│   └── package.json
│
└── database/
    └── setup.sql              # MySQL Workbench setup script
```

---

## 🚀 Setup Instructions

### Step 1 — MySQL Database Setup

1. Open **MySQL Workbench**
2. Connect to your MySQL server
3. Open `database/setup.sql`
4. Run the entire script (Ctrl+Shift+Enter)
5. Database `women_safety_db` will be created with all tables ✅

### Step 2 — Backend Setup

```bash
cd backend
npm install
```

Edit `.env` and set your MySQL password:
```env
DB_HOST=localhost
DB_PORT=3306
DB_NAME=women_safety_db
DB_USER=root
DB_PASSWORD=YOUR_MYSQL_PASSWORD_HERE
JWT_SECRET=womenSafetyAIApp2024SecretKey!@#
PORT=5000
```

Start the backend server:
```bash
npm run dev    # Development (with auto-reload)
npm start      # Production
```

Server will run at: **http://localhost:5000**

### Step 3 — Frontend Setup

Simply open the frontend files in a browser or use Live Server (VS Code):

- **Login**: `frontend/login.html`
- **Dashboard**: `frontend/dashboard.html`

Or use a simple HTTP server:
```bash
cd frontend
npx serve .
```

---

## 🌐 API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/auth/register` | Register new user |
| POST | `/api/auth/login` | Login user |
| GET | `/api/auth/profile` | Get profile (protected) |
| POST | `/api/emergency/sos` | Trigger SOS alert |
| PUT | `/api/emergency/location` | Update live location |
| GET | `/api/emergency/history` | Get alert history |
| POST | `/api/emergency/risk-analysis` | AI risk analysis |
| GET | `/api/emergency/stats` | Dashboard stats |
| PUT | `/api/emergency/:id/resolve` | Resolve alert |
| GET | `/api/contacts` | Get emergency contacts |
| POST | `/api/contacts` | Add contact |
| PUT | `/api/contacts/:id` | Update contact |
| DELETE | `/api/contacts/:id` | Delete contact |

---

## 🗄️ Database Tables

| Table | Description |
|-------|-------------|
| `users` | User accounts |
| `emergency_alerts` | All SOS/Voice/Shake alerts |
| `emergency_contacts` | Trusted emergency contacts |
| `location_history` | GPS location audit trail |
| `safe_zones` | Police stations & safe areas |

---

## ✨ Key Features

- 🔴 **SOS Button** — One-tap emergency activation
- 🎙️ **Voice Trigger** — "HELP" voice command support
- 📳 **Shake Detection** — Phone shake emergency trigger
- 📍 **Live GPS Tracking** — Real-time location updates
- 🧠 **AI Risk Analysis** — Smart danger score calculation
- 👥 **Emergency Contacts** — Up to 5 trusted people
- 📞 **Fake Call Tool** — Realistic incoming call to escape danger
- 📊 **Alert History** — Complete audit log with filters
- 🔐 **JWT Authentication** — Secure user sessions
- ⚡ **Socket.IO** — Real-time emergency notifications
- 🗄️ **MySQL** — Reliable relational database (Sequelize ORM)

---

## 🛡️ Emergency Helplines

| Number | Service |
|--------|---------|
| **112** | All Emergency (Police, Fire, Medical) |
| **1091** | Women Safety Helpline |
| **100** | Police |
| **108** | Ambulance |
| **181** | Women Helpline (Domestic Violence) |

---

## 🏆 Hackathon Flow

```
User Trigger (SOS / Voice / Shake)
        ↓
Emergency Mode ON
        ↓
Location Tracking Start (GPS)
        ↓
Automatic Helpline Call (112)
        ↓
Emergency Contacts Alert (SMS)
        ↓
Audio Recording Start (Evidence)
        ↓
AI Risk Detection (Score + Tips)
        ↓
Safe Route + Police Help
        ↓
All Data Stored in MySQL Database
```

---

Built with ❤️ for women's safety | Hackathon 2024
