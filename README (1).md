
# 🌫️ AirWatch India
<img width="1661" height="1033" alt="Screenshot 2026-03-22 140551" src="https://github.com/user-attachments/assets/50fab51a-60a6-42e4-8700-74d33351465f" />

> A real-time air quality monitoring dashboard for 10 major Indian cities — built as part of a 12-project weekend challenge aligned with the UN Sustainable Development Goals.

![HTML](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6%2B-F7DF1E?style=flat&logo=javascript&logoColor=black)
![Chart.js](https://img.shields.io/badge/Chart.js-FF6384?style=flat&logo=chartdotjs&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=flat)

**UN SDGs addressed:**
🟢 SDG 3 — Good Health and Well-Being &nbsp;|&nbsp; 🔵 SDG 11 — Sustainable Cities &nbsp;|&nbsp; 🟡 SDG 13 — Climate Action

---

## 🚀 Live Demo

👉 **[View Live on GitHub Pages](https://YOUR-USERNAME.github.io/airwatch-india)**

> Replace `YOUR-USERNAME` with your GitHub username after deploying.

---

## ✨ Features

- **Real-time AQI** for 10 Indian cities via the [WAQI API](https://waqi.info)
- **Animated gauge** — colour-coded arc from green (Good) to dark red (Hazardous)
- **Pollutant breakdown** — PM2.5, PM10, O₃, NO₂, SO₂, CO for each city
- **7-day trend chart** — powered by Chart.js with per-point colour coding
- **Smart alerts** — in-page banner + browser push notifications with adjustable threshold
- **30-minute cache** — localStorage to stay within free API limits
- **Fully responsive** — mobile, tablet, and desktop
- **Zero build step** — vanilla JS ES Modules, no npm, no webpack

---

## 🛠️ Tech Stack

| Layer | Tech |
|---|---|
| Frontend | HTML5, CSS3, Vanilla JS (ES Modules) |
| Charts | Chart.js 4 |
| Data | WAQI API (free tier) |
| Caching | Browser localStorage (30 min TTL) |
| Fonts | DM Sans + DM Mono (Google Fonts) |
| Hosting | GitHub Pages |

---

## ⚙️ Setup & Run Locally

### 1. Clone the repo
```bash
git clone https://github.com/YOUR-USERNAME/airwatch-india.git
cd airwatch-india
```

### 2. Get a free WAQI API key
Register at 👉 [aqicn.org/data-platform/token](https://aqicn.org/data-platform/token/) — just an email confirmation.

### 3. Add your key
Open `js/config.js` and replace the demo token:
```js
export const WAQI_TOKEN = "your-token-here";
```

### 4. Start a local server
```bash
# Python (built-in, no install)
python3 -m http.server 8080

# Node.js
npx serve .
```
Open [http://localhost:8080](http://localhost:8080)

> ⚠️ A local server is required — ES Modules don't work over the `file://` protocol.

---

## 🌐 Deploy to GitHub Pages (Free)

1. Push this repo to GitHub
2. Go to **Settings → Pages**
3. Source: **Deploy from a branch** → `main` → `/ (root)` → **Save**
4. Live in ~60 seconds at `https://YOUR-USERNAME.github.io/airwatch-india`

---

## 📁 Project Structure

```
airwatch-india/
├── index.html       ← App shell + layout
├── style.css        ← Dark theme, responsive grid
├── README.md
└── js/
    ├── config.js    ← API token, city list, AQI thresholds
    ├── fetcher.js   ← WAQI API + localStorage cache
    ├── classifier.js← AQI → category, colour, trend
    ├── alerts.js    ← Notifications + alert banner
    └── main.js      ← Entry point
```

---

## 🏙️ Supported Cities

Bengaluru · Delhi · Mumbai · Chennai · Hyderabad · Kolkata · Pune · Ahmedabad · Jaipur · Lucknow

To add more cities, extend the `CITIES` array in `js/config.js`.

---

## 🔮 Roadmap

- [ ] Map view with Leaflet.js
- [ ] PWA — offline support + install to home screen
- [ ] Hourly AQI breakdown
- [ ] Health tips by age group

---

## 🌱 Why I Built This

Air pollution causes over 1.6 million deaths in India annually. Most people don't check AQI before going outside because existing tools are cluttered and hard to read.

This dashboard makes air quality data accessible, beautiful, and actionable — giving anyone a 5-second answer to *"is it safe to go outside today?"*

Built as **Weekend Project #1 of 12** — each project tackles a real-world problem aligned with UN Sustainable Development Goals.

---

## 📄 License

MIT — free to use, modify, and distribute.

---

<p align="center">Made with 🫁 and genuine concern for clean air</p>
