*⚠️ Note: The core development of this project took place in a private repository to protect API keys and sensitive configuration. This public version represents the finalized production build.*

# 📈 NewsIntel — Financial Intelligence Dashboard

[![Live Demo](https://img.shields.io/badge/demo-live-brightgreen?style=for-the-badge&logo=vercel)](https://newsintel-mu.vercel.app/)
![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/javascript-%23F7DF1E.svg?style=for-the-badge&logo=javascript&logoColor=black)
![Leaflet](https://img.shields.io/badge/Leaflet-199918?style=for-the-badge&logo=Leaflet&logoColor=white)
![Vercel](https://img.shields.io/badge/vercel-%23000000.svg?style=for-the-badge&logo=vercel&logoColor=white)

A browser-based financial intelligence platform that brings together stock analysis, news impact assessment, and global conflict tracking into a single cohesive interface. **Built entirely with vanilla HTML, CSS, and JavaScript** — no frameworks, no build tools, and no dependencies beyond a map library.

---

## 🛠️ Technologies Used

| Layer | Technology |
|---|---|
| **Structure** | HTML5 |
| **Styling** | CSS3 — Custom Properties, Flexbox, Grid, animations |
| **Logic** | Vanilla JavaScript (ES6+) |
| **Maps** | Leaflet.js 1.9.4 |
| **Charts** | HTML5 Canvas API |
| **Fonts** | Google Fonts — IBM Plex Mono, Syne, DM Sans, Bebas Neue, Manrope |
| **Fetching** | CORS proxy APIs (allorigins, codetabs, corsproxy.io) |

---

## ✨ Core Features

### 1. Stock Intelligence
*Direct insights into 15+ blue-chip tickers across US & SG markets.*
* **Smart Signals:** Dynamic `BUY` / `WAIT` / `AVOID` badges based on valuation metrics.
* **Canvas Sparklines:** Custom-drawn 30-day price history and dashed projections.
* **Deep-Dive Modals:** Detailed risk assessment, P/E ratios, and dividend yields.
* **Market Coverage:** 🇺🇸 (NVDA, AAPL, TSLA) | 🇸🇬 (DBS, SIA, ST Engineering).

### 2. Market Impact Analyzer
*Quantifying the narrative: How news moves the needle.*
* **Triple-Threat Input:** Support for direct text paste, `.pdf`/`.txt` uploads, or URL fetching via CORS proxy.
* **Sentiment Engine:** Rule-based NLP identifying Bullish/Bearish shifts in specific sectors.
* **Transmission Logic:** Maps macro events (e.g., "Rate Hikes") to specific sector pressure.
* **Stale Detection:** Automatically flags news >7 days old as "already priced in."

### 3. Global Conflict Tracker
*Visualizing geopolitical risk in real-time.*
* **Interactive Map:** 28+ active conflict zones with pulsing status indicators.
* **Risk Categorization:** Filter by "Interstate," "Civil War," or "Political Instability."
* **The Singapore Connection:** Specialized links for conflicts impacting local trade (Red Sea, South China Sea).
* **Fly-to Interaction:** Click a conflict to automatically zoom the viewport to the epicenter.

---

## 🏗️ The Process of Building

The project grew page by page, each one teaching something new.

1.  **Stock Intelligence:** Started with a simple grid of stock cards. The challenge was designing a readable dark theme for dense data and drawing sparklines using the Canvas API directly.
2.  **Market Impact Analyzer:** Built to explore the "why" behind price movements. The core challenge was building a keyword-matching sentiment engine that maps financial terminology to market outcomes.
3.  **Conflict Tracker:** Introduced the first external library, Leaflet.js. Focused on customizing map tiles, creating `divIcon` markers with CSS animations, and managing complex layer visibility.

Throughout the build, a shared design system was maintained—using the same dark palette and monospace labels—to ensure the suite feels like a single, cohesive product.

---

## 🧠 Knowledge Gained

### Finance & Markets
* **Valuation Metrics:** Deep understanding of P/E ratios, dividend yields, and beta.
* **Rate Sensitivity:** How Fed decisions reprice equities through the discount rate.
* **Singapore Nuance:** Analyzing the unique impact of Taiwan Strait or Red Sea stability on SG port throughput.
* **Geopolitical Risk:** Translating conflict into oil price premiums and safe-haven flows.

### Technology
* **Canvas API:** Drawing polylines and dashed projections without a charting library.
* **CORS Proxies:** Navigating cross-origin restrictions to aggregate news data.
* **DOM Management:** Efficiently rendering and re-rendering lists and modals in plain JS.
* **CSS Design Tokens:** Using custom properties (`--accent`, `--bg-dark`) for theme consistency.

---

## 🔮 Future Roadmap

- [ ] **Live Market Data:** Replace static prices with a real financial API (Alpha Vantage/Polygon.io).
- [ ] **AI-Powered Analysis:** Integrate the Claude API for deep semantic news analysis.
- [ ] **Persistent Watchlist:** Save user-selected tickers using `localStorage`.
- [ ] **Portfolio Tracker:** Input holdings and see aggregate exposure to geopolitical risks.
- [ ] **Global Expansion:** Expand beyond US and Singapore to cover EU, Japan, and Hong Kong.

---

## 📂 Project Structure

| File | Page |
|---|---|
| `stockintelligence.html` | Stock Intelligence dashboard |
| `news-marketanalyzer.html` | Market Impact Analyzer |
| `conflict-tracker.html` | Global Conflict Tracker |

> **Note:** The Conflict Tracker requires an internet connection to load the CartoDB map tiles. Other pages are self-contained.
