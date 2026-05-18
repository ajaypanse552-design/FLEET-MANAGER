# 🚛 FleetPro — Vehicle Fleet Management System

A complete, single-file logistics fleet management web app with real-time status tracking, daily data entry, and Excel export. No server or database required — runs entirely in the browser.

---

## ✨ Features

- **Live Dashboard** — Running / Loading / Idle vehicle counts with live clock
- **Vehicle Management** — Add, delete, and track your entire fleet
- **Daily Entries** — Log date, destination, diesel, cash, PhonePe, extra expenses, and remarks per vehicle
- **Real-time Status** — Change vehicle status (Running / Loading / Idle) with one click
- **Monthly Reports** — View and filter data by month and year
- **Excel Export** — Download month-end reports as `.xlsx` with per-vehicle sheets + combined summary
- **Offline Ready** — All data stored in browser's localStorage (no internet needed after first load)

---

## 📁 Project Structure

```
fleet-manager/
├── index.html      ← The entire app (single file)
└── README.md       ← This file
```

---

## 🚀 Deployment Options

### Option 1 — Open Locally (Simplest)
Just double-click `index.html` to open in any browser. No installation needed.

> ⚠️ Data is stored per-browser. If you open it in a different browser or device, it starts fresh.

---

### Option 2 — Deploy on Netlify (Free, Recommended)

1. Go to [https://netlify.com](https://netlify.com) and sign up (free)
2. Click **"Add new site"** → **"Deploy manually"**
3. Drag and drop the `fleet-manager` folder onto the upload area
4. Netlify gives you a live URL like `https://your-site.netlify.app`
5. Share that URL with anyone in your team

---

### Option 3 — Deploy on GitHub Pages (Free)

1. Create a free account at [https://github.com](https://github.com)
2. Click **New Repository** → name it `fleet-manager` → set to **Public**
3. Upload `index.html` to the repository
4. Go to **Settings → Pages → Source → Deploy from branch → main → / (root)**
5. Your site will be live at `https://yourusername.github.io/fleet-manager`

---

### Option 4 — Deploy on Vercel (Free)

1. Go to [https://vercel.com](https://vercel.com) and sign up
2. Click **"Add New Project"** → **"Import"**
3. Upload or connect your GitHub repo containing `index.html`
4. Click **Deploy** — done in under 1 minute

---

### Option 5 — Host on Your Own Web Server / cPanel

1. Log in to your hosting control panel (cPanel, Plesk, etc.)
2. Open **File Manager** → navigate to `public_html`
3. Upload `index.html` → rename to `index.html` if needed
4. Visit `https://yourdomain.com` — the app is live

---

## 📱 How to Use

### Step 1 — Add Your Vehicles
- Go to **Vehicles** page
- Click **Add Vehicle**
- Enter vehicle number (e.g. `GJ01AB1234`), type, and initial status

### Step 2 — Add Daily Entries
- Click **New Entry** (from Dashboard or Daily Entries page)
- Fill in: Date, Vehicle, Destination, Status, Diesel, Cash, PhonePe, Extra, Remarks
- Click **Save Entry**

### Step 3 — Export Monthly Report
- Go to **Reports** page
- Select Month and Year
- Click **Download Excel**
- The `.xlsx` file will have:
  - One sheet per vehicle (named by vehicle number)
  - One combined "All Entries" sheet
  - Totals row at the bottom of each sheet

---

## 💾 Data Storage

- All data is saved automatically in your **browser's localStorage**
- Data stays even after closing the browser or restarting the computer
- Data is **per browser per device** — not synced across devices
- To back up your data: open browser DevTools (F12) → Console → type:
  ```js
  copy(localStorage.getItem('fleet_entries'))
  ```
  Then paste into a `.txt` file

---

## 🔧 Customization

The entire app is in one file (`index.html`). To customize:

- **Add more fields** — Search for `e-remarks` in the HTML and add more `form-group` divs
- **Change company name** — Search for `FleetPro` and replace with your company name
- **Change currency** — Search for `₹` and replace with your currency symbol
- **Add more vehicle types** — Find the `<select id="v-type">` and add more `<option>` tags

---

## 🌐 Browser Support

Works on all modern browsers:
- ✅ Google Chrome
- ✅ Microsoft Edge
- ✅ Mozilla Firefox
- ✅ Safari (Mac / iOS)
- ✅ Mobile browsers

---

## ❓ FAQ

**Q: Will I lose data if I clear browser history?**  
A: Yes — clearing "cookies and site data" will erase localStorage. Export your Excel before clearing.

**Q: Can multiple people use it at the same time?**  
A: Not with the current version — it stores data locally. For multi-user access, consider using it on a shared computer or contact a developer to add a backend database.

**Q: Can I use it on my phone?**  
A: Yes — the layout is responsive and works on mobile browsers.

**Q: How do I move data to a new computer?**  
A: Export Excel regularly as a backup. For full data migration, use the browser console method described in the Data Storage section above.

---

## 📞 Support

Built with ❤️ for logistics businesses. Single-file, zero dependencies (except SheetJS for Excel export via CDN).
