# 🗑️ SmartWaste — City Waste Management System

A fully client-side, multi-page web app that lets citizens report overflowing garbage bins, track complaint status, and help keep their city clean. No backend or server required.

---

## 🚀 Features

- **Report Garbage Bins** — Upload a photo, pin the location, set severity level
- **GPS Auto-detect** — Automatically fetch current coordinates for the complaint
- **Live Dashboard** — View, filter, and manage all your complaints
- **Status Tracking** — Update complaints between Pending → In Progress → Completed
- **Severity Levels** — Low, Medium, High, Critical
- **User Auth** — Register/Login with localStorage-based accounts
- **Responsive Design** — Works on mobile and desktop

---

## 📁 File Structure

```
SmartWaste/
├── index.html       # Landing page (hero, features, how it works)
├── login.html       # Login page
├── register.html    # Registration page
├── report.html      # Report a garbage bin (form)
└── dashboard.html   # User dashboard (complaint list + stats)
```

> All files are standalone HTML — no build tools, no frameworks, no backend needed.

---

## 🖥️ How to Use

### 1. Open the App
Open `index.html` in any modern browser directly as a local file, or host on any static server (GitHub Pages, Netlify, etc.).

### 2. Create an Account
Click **Get Started** → fill in name, email, and password on `register.html`. Passwords must be at least 6 characters.

### 3. Report a Bin
After logging in, you land on `report.html`:
- Upload a photo of the overflowing bin
- Enter the area/street, city, and pincode (or click **Auto-detect** for GPS)
- Set the severity level and add a description
- Click **Submit Complaint**

### 4. Track on Dashboard
Go to `dashboard.html` to:
- See summary stats (Total / Pending / In Progress / Resolved)
- Filter complaints by status
- Update complaint status via the dropdown
- Delete complaints you no longer need

---

## 📊 Dashboard Stats

| Stat | Colour | Meaning |
|------|--------|---------|
| Total | Teal | All complaints filed by you |
| Pending | Yellow | Awaiting action |
| In Progress | Blue | Being addressed |
| Resolved | Green | Completed |

---

## 🔐 Auth & Data Storage

All data is stored in the browser's `localStorage` — no server calls are made.

| Key | Contents |
|-----|----------|
| `sw_users` | Array of all registered users |
| `sw_user` | Currently logged-in user object |
| `sw_complaints` | Array of all complaints (all users) |

> ⚠️ Data is browser-specific. Clearing browser data will remove all accounts and complaints.

---

## 🗺️ Complaint Object Structure

```json
{
  "id": 1712345678901,
  "userId": 1712345678000,
  "userName": "John Doe",
  "area": "MG Road, Koramangala",
  "city": "Bengaluru",
  "pincode": "560001",
  "severity": "high",
  "desc": "Bin near bus stop overflowing since 2 days",
  "image": "data:image/jpeg;base64,...",
  "status": "Pending",
  "date": "5 Apr 2026"
}
```

---

## ⚙️ Severity Levels

| Level | Icon | Description |
|-------|------|-------------|
| Low | 🟡 | Slightly overflowing |
| Medium | 🟠 | Very full |
| High | 🔴 | Garbage on street |
| Critical | 🚨 | Health hazard |

---

## 🎨 Design

- **Fonts:** Syne (headings) + DM Sans (body) via Google Fonts
- **Colours:** Dark green `#0a1a0f` background, `#00c853` green accent, `#1de9b6` teal gradient
- **Theme:** Dark-only UI with glassmorphism cards and gradient accents

---

## 🌐 Browser Compatibility

Works in all modern browsers. Recommended: **Chrome** or **Edge**.

GPS auto-detect requires the user to grant location permission when prompted.

---

## 📄 License

This project is for personal/educational use. Pure HTML, CSS, and vanilla JavaScript — no external libraries or frameworks.
