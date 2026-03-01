# NewsIntel — Financial Intelligence Dashboard

A browser-based financial intelligence platform that brings together stock analysis, news impact assessment, and global conflict tracking into a single cohesive interface. Built entirely with vanilla HTML, CSS, and JavaScript — no frameworks, no build tools, no dependencies beyond a map library.

---

## Technologies Used

| Layer | Technology |
|---|---|
| Structure | HTML5 |
| Styling | CSS3 — Custom Properties, Flexbox, Grid, animations |
| Logic | Vanilla JavaScript (ES6+) |
| Maps | Leaflet.js 1.9.4 |
| Charts | HTML5 Canvas API |
| Fonts | Google Fonts — IBM Plex Mono, Syne, DM Sans, Bebas Neue, Manrope |
| URL fetching | CORS proxy APIs (allorigins, codetabs, corsproxy.io) |

---

## Features

### Stock Intelligence
A curated dashboard of US and Singapore equities with AI-style investment signals.

- **Stock cards** for 15+ tickers across US (NVDA, AAPL, MSFT, META, TSLA, XOM, JPM, AMZN) and Singapore markets (DBS, OCBC, ST Engineering, SIA, SATS, CICT)
- **BUY / WAIT / AVOID** signals with colour-coded badges
- **Mini sparkline charts** rendered on Canvas with simulated price history
- **Sector filters** — All, Tech, Finance, Energy — and a live search bar
- **Detail modal** on click, showing:
  - Full price chart with a 30-day projection overlay (dashed line)
  - Key metrics: P/E ratio, market cap, dividend yield, beta, 52-week range
  - Numbered reasons to invest
  - Key risks
  - Investment verdict with recommended entry price and holding period

### Market Impact Analyzer
Paste a news article and get an instant market impact assessment.

- **Three input methods** — paste text directly, upload a `.txt` / `.pdf` file, or fetch a URL (via CORS proxy)
- **Metadata tagging** — select news source (BBC, Reuters, CNBC, FT, CNA), publication date, and category (macro, earnings, geopolitical, commodities, crypto, regulation)
- **Keyword-based sentiment engine** produces a Bullish / Bearish / Neutral verdict with a confidence score
- **Affected securities** with projected short-term price moves per ticker
- **Sector impact bars** showing relative pressure on Financials, Energy, Technology, Consumer Discretionary, Healthcare, Utilities
- **Reasoning block** explaining the transmission mechanism from news to markets
- **Sample articles** to try the tool instantly
- Stale-article detection — flags news older than 7 days as already priced in

### Global Conflict Tracker
An interactive world map of 28 active conflicts, built for monitoring geopolitical risk.

- **Leaflet.js map** with dark CartoDB tile layer and pulsing markers (red = worsening, yellow = unchanging, green = improving)
- **Collapsible sidebar** with:
  - Search bar
  - Filter chips for conflict type (Interstate, Civil War, Territorial Dispute, Transnational Terrorism, Criminal Violence, Political Instability)
  - Impact filters for US and Singapore interests (Critical, Significant, Limited)
  - Status filter (Worsening, Unchanging, Improving)
- **Region-grouped conflict list** across Americas, Middle East & North Africa, Sub-Saharan Africa, Asia, Europe & Eurasia
- **Detail panel** per conflict — slides in from the right, showing region, type, status tags, countries affected with flags, and a direct link to the CFR analysis
- **Singapore-specific news links** for conflicts with direct relevance (South China Sea, Yemen/Red Sea, Myanmar, Taiwan)
- **Stats bar** at the bottom with live counts: total, worsening, unchanging, improving, critical
- Map **flies to the conflict location** when a marker or list item is clicked

---

## The Process of Building

The project grew page by page, each one teaching something new.

**1. Stock Intelligence (first)**
The starting point was a simple grid of stock cards. The main challenges were designing a readable dark theme for dense financial data, and drawing sparkline charts with Canvas. Once the card grid worked, a modal was added for the detailed breakdown — chart projection, metrics, investment reasoning — which required managing Canvas redraws and modal state cleanly.

**2. Market Impact Analyzer (second)**
After building stock cards with static data, the natural next question was: *how does news move these prices?* This page was built to explore that connection. The keyword-matching sentiment engine was the core challenge — mapping financial terminology to market outcomes (rate hike → TLT falls, oil spike → XOM rises). URL fetching required routing through public CORS proxies since browsers block cross-origin requests.

**3. Conflict Tracker (third, most recent)**
The conflict tracker brought in the first external library — Leaflet.js. Learning to customise map tiles, create `divIcon` markers with pulse animations, manage layer visibility on filter changes, and build the sliding detail panel were all new challenges. The Singapore-specific news links were added to tie geopolitical events back to local market relevance.

Throughout all three pages, a shared design system was maintained — the same dark palette, monospace labels, and accent colours — so navigating between pages feels like one product, not three separate tools.

---

## What I Learned

### Finance & Markets

| Concept | What I Learned |
|---|---|
| Stock signals | What drives BUY vs WAIT vs AVOID — valuation, momentum, macro environment |
| Valuation metrics | P/E ratio, market cap, dividend yield, beta, 52-week range and what each tells you |
| Sector rotation | Why money moves from growth to value in high-rate environments |
| Rate sensitivity | How Fed decisions reprice equities through the discount rate |
| News & markets | How to trace a news event through to its sector and ticker impact |
| Sentiment analysis | Why the same headline can be bullish for one sector and bearish for another |
| Singapore equities | STI structure, REITs, DBS/OCBC/OCBC dividend culture, MAS policy |
| Geopolitical risk | How conflicts translate to oil price premiums, defence sector bids, and safe-haven flows |
| Supply chain risk | How the Red Sea / Yemen conflict affected Singapore's port congestion |
| Taiwan Strait | Why a Taiwan conflict would be uniquely damaging to Singapore as a trade hub |

### Technology

| Concept | What I Learned |
|---|---|
| Canvas API | Drawing polylines, dashed projections, axes, and legend elements without a charting library |
| Leaflet.js | Tile layers, custom `divIcon` markers, tooltip styling, flyTo animations, layer management |
| CSS Custom Properties | Using design tokens (`--accent`, `--text-dim`) as a consistent design system across pages |
| CSS Grid & Flexbox | Combining both for responsive two-column layouts and filter chip rows |
| CORS proxies | Why browsers block cross-origin requests and how public proxies work around it |
| Keyword NLP | Building a lightweight rule-based sentiment engine using string matching |
| DOM management | Rendering and re-rendering lists, modals, and panels efficiently in plain JS |
| Responsive design | Making the layout usable on mobile with sticky buttons and panel scroll |
| CSS animations | Pulsing markers, blinking dots, spinner keyframes |
| File API | Reading user-uploaded `.txt` files with `FileReader` |

---

## Overall Growth

This project was built entirely from scratch without tutorials or starter templates, which forced every decision to be understood rather than copied. The biggest growth came from having to think about both domains simultaneously — *what does this data mean financially?* and *how do I display it cleanly?*

Learning to connect news events to market movements — and then building a tool that does that automatically — gave the financial concepts much more depth than just reading about them. Seeing that a Federal Reserve statement would compress P/E multiples, or that a Red Sea blockade would pressure Singapore's port throughput, made macroeconomics feel concrete rather than abstract.

On the technical side, the biggest shift was learning to work without frameworks. Every layout, every state update, every animation had to be solved from first principles, which built a much stronger understanding of how browsers actually work.

---

## How It Could Be Improved

- **Live market data** — replace static prices with a real financial API (Yahoo Finance, Alpha Vantage, or Polygon.io) for real-time quotes and actual historical charts
- **Real AI analysis** — integrate the Claude API into the Market Analyzer to replace keyword matching with genuine language understanding
- **Persistent watchlist** — let users save stocks to a personal list using `localStorage`
- **Portfolio tracker** — input holdings and see their aggregate exposure to geopolitical risks on the conflict map
- **More markets** — expand beyond US and Singapore to cover EU, Japan, Hong Kong, Australia
- **Live conflict data** — connect to the ACLED or GDELT API for automatically updated conflict events
- **Push alerts** — notify users when a tracked conflict status changes or a watched stock hits a target price
- **Dark/light theme toggle** — the design system already uses CSS custom properties, making a theme switch straightforward to add
- **PDF export** — let users download a stock card or market analysis as a PDF report


**Pages**

| File | Page |
|---|---|
| `stockintelligence.html` | Stock Intelligence dashboard |
| `news-marketanalyzer.html` | Market Impact Analyzer |
| `conflict-tracker.html` | Global Conflict Tracker |

> The Conflict Tracker requires an internet connection to load the CartoDB map tiles. The other two pages are fully self-contained.
