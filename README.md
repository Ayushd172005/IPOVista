# IPOVista 🇮🇳
### Indian IPO Analytics Dashboard

> Search any IPO from 2010–2022 and instantly see subscription data, listing gains, investor sentiment scores, peer comparisons, and market-wide trends — all in one dark-mode dashboard.

[![Live Demo](https://img.shields.io/badge/Live%20Demo-ipo--vista--deployment.vercel.app-black?style=for-the-badge&logo=vercel)](https://ipo-vista-deployment.vercel.app/)
[![Dataset](https://img.shields.io/badge/Dataset-319%20IPOs-c8f03c?style=for-the-badge&logoColor=black)](https://github.com/Ayushd172005/IPOVista)
[![Deployment Repo](https://img.shields.io/badge/Deployment%20Repo-IPOVista__Deployment-6c5ce7?style=for-the-badge&logo=github)](https://github.com/Ayushd172005/IPOVista_Deployment)

---

## Screenshots

**Search View**
<img width="1280" height="800" alt="Search View" src="https://github.com/user-attachments/assets/7241d254-75fd-45f7-bd70-8f09ecc2215d" />

**Company Analysis — Zomato**
<img width="1280" height="800" alt="Zomato Analysis" src="https://github.com/user-attachments/assets/75150dee-380d-4430-9020-513b25df0463" />
<img width="1280" height="800" alt="Zomato Analysis 2" src="https://github.com/user-attachments/assets/4b4b71fa-8f0a-40fe-9373-0a2b653e3083" />

**Market Overview**
<img width="1280" height="800" alt="Market Overview" src="https://github.com/user-attachments/assets/d889a5af-8140-4c2f-94db-3d6ac4a94fd2" />

**Leaderboard**
<img width="1280" height="800" alt="Leaderboard" src="https://github.com/user-attachments/assets/8af4cce0-3bf7-4576-ab52-49c1aed32ddb" />

---

## Features

- **Company Search** — Type any company name for a full IPO breakdown with autocomplete suggestions
- **Subscription Analysis** — QIB, HNI, and RII subscription charts visualised side by side
- **Listing Gain Benchmark** — Compare a stock's listing gain vs. its year's average and the all-time average
- **Investor Sentiment Score** — Composite 0–100 score derived from subscription strength and listing performance
- **Peer IPOs** — Other companies that listed within 90 days, clickable for instant comparison
- **Analyst Summary** — Auto-generated narrative verdict (Buy / Hold / Avoid) for each IPO
- **Market Overview** — Year-by-year average gains, IPO count per year, and gain distribution histogram
- **Leaderboard** — Top 50 IPOs ranked by best gainers, worst performers, most subscribed, or largest issue size

---

## Dataset

- **319 Indian IPOs** spanning 2010–2022
- Source: `Indian_IPO_Market_Data.csv` compiled into `data.js` for zero-latency browser access
- Fields: IPO name · listing date · issue size (₹ Cr) · QIB / HNI / RII subscription multiples · total subscription · issue price · listing day gain %

---

## Repository Structure

This project uses a two-repo setup — source here, deployment separate:

| Repo | Purpose |
|---|---|
| [`IPOVista`](https://github.com/Ayushd172005/IPOVista) | Source code — develop and edit here |
| [`IPOVista_Deployment`](https://github.com/Ayushd172005/IPOVista_Deployment) | Production build — Vercel watches this |

---

## File Structure for Deployment

```
IPOVista/
├── index.html       # Main HTML — Search, Market, and Leaderboard views
├── style.css        # Dark theme — lime accent, Syne + DM Mono + Inter fonts
├── app.js           # All logic — search, Chart.js rendering, sentiment scoring
├── data.js          # 319 IPO records compiled from CSV
├── vercel.json      # Vercel static deployment config
└── README.md
```

---

## Tech Stack

- **Vanilla HTML / CSS / JS** — zero frameworks, zero build step
- **[Chart.js 4](https://www.chartjs.org/)** — bar charts, histograms, benchmark comparisons
- **Google Fonts** — Syne · DM Mono · Inter
- **Vercel** — static hosting via `IPOVista_Deployment`

---

## Local Development

```bash
git clone https://github.com/Ayushd172005/IPOVista.git
cd IPOVista

# Open directly in browser
open index.html

# Or use a local server
npx serve .
# or
python3 -m http.server 8080
```

---

## Deployment Workflow

```
Edit in IPOVista  →  Test locally  →  Push to IPOVista_Deployment  →  Vercel auto-deploys
```

```bash
# Copy updated files to deployment repo
cp index.html style.css app.js data.js vercel.json ../IPOVista_Deployment/

cd ../IPOVista_Deployment
git add . && git commit -m "deploy: sync from source" && git push
```

---

## Author

**Ayush D** — [@Ayushd172005](https://github.com/Ayushd172005)

---
