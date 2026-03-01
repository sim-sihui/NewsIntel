# 📈 NewsIntel — Financial Intelligence Dashboard

[![Live Demo](https://img.shields.io/badge/demo-live-brightgreen?style=for-the-badge&logo=vercel)](https://newsintel-mu.vercel.app/)
![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/javascript-%23F7DF1E.svg?style=for-the-badge&logo=javascript&logoColor=black)
![Leaflet](https://img.shields.io/badge/Leaflet-199918?style=for-the-badge&logo=Leaflet&logoColor=white)
![Vercel](https://img.shields.io/badge/vercel-%23000000.svg?style=for-the-badge&logo=vercel&logoColor=white)

**A high-performance, framework-free intelligence suite for modern investors.**

NewsIntel bridges the gap between **Global Geopolitics**, **Market Sentiment**, and **Equity Analysis**. Built from the ground up to be lightweight and dependency-free, it provides a "single pane of glass" view into the forces moving US and Singapore markets.

---

## 🚀 The "Vanilla" Philosophy

In a world of bloated frameworks, NewsIntel is built on the belief that the modern browser is already powerful enough.
* **Zero Frameworks:** No React, Vue, or Angular.
* **Zero Build Tools:** No Webpack, Vite, or NPM dependencies.
* **Pure Performance:** Instant load times using native Web APIs.

---

## 🛠️ Tech Stack & Architecture

| Layer | Technology | Implementation Detail |
| :--- | :--- | :--- |
| **Logic** | `Vanilla JS (ES6+)` | Custom state management and DOM reconciliation. |
| **Visuals** | `HTML5 Canvas` | High-fidelity sparklines & price projections drawn pixel-by-pixel. |
| **Mapping** | `Leaflet.js` | Interactive geopolitical risk overlays with custom pulse animations. |
| **Design** | `CSS3 + Variables` | A unified design system using CSS tokens for dark-mode consistency. |
| **Connectivity** | `CORS Proxies` | Real-time news fetching via Allorigins and Corsproxy.io. |

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
* **Triple-Threat Input:** Support for direct text paste, `.pdf`/`.txt` uploads, or URL fetching.
* **Sentiment Engine:** Rule-based NLP identifying Bullish/Bearish shifts in specific sectors.
* **Transmission Logic:** Maps macro events (e.g., "Rate Hikes") to specific sector pressure (e.g., "Tech").
* **Stale Detection:** Automatically flags news >7 days old as "already priced in."

### 3. Global Conflict Tracker
*Visualizing geopolitical risk in real-time.*
* **Interactive Map:** 28+ active conflict zones with pulsing status indicators.
* **Risk Categorization:** Filter by "Interstate," "Civil War," or "Political Instability."
* **The Singapore Connection:** Specialized links for conflicts impacting local trade (Red Sea, South China Sea).
* **Fly-to Interaction:** Click a conflict to automatically zoom the viewport to the epicenter.



---

## 🧠 What I Learned

### Financial Intelligence
* **Macro-Transmission:** How the Federal Reserve's discount rate reprices growth equities.
* **Sector Rotation:** Tracking the flight to quality during geopolitical volatility.
* **Singapore Nuance:** Analyzing the unique impact of Taiwan Strait or Red Sea stability on SG port throughput.

### Technical Engineering
* **From-Scratch Charting:** Building a charting engine using the Canvas API instead of a library.
* **CORS Mastery:** Navigating cross-origin restrictions to aggregate news data.
* **Design Systems:** Implementing unified themes using CSS Custom Properties (`--accent`, `--bg-dark`).

---

## 🔮 Future Roadmap

- [ ] **Live API Integration:** Transition from static data to Alpha Vantage/Polygon.io.
- [ ] **LLM Integration:** Connect Claude/GPT-4 API for deep semantic news analysis.
- [ ] **Portfolio Stress Testing:** Simulate how a specific conflict would impact user holdings.
- [ ] **Persistent Watchlists:** `localStorage` integration for user-saved tickers.

---

## 📂 Project Structure

* `stock intelligence` — Equity dashboard & signal engine.
* `news market analyzer` — Sentiment analysis & news processing tool.
* `conflict tracker` — Geopolitical map (Requires internet for CartoDB tiles). Specifically on how the world conflict will impact US and SG.

---

Built with ☕ and Vanilla JavaScript.
