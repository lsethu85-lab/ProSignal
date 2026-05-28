# Asset Intelligence Dashboard

<p align="center">
  <strong>A full-featured, browser-based equity research and portfolio intelligence workspace</strong><br>
  <sub>Powered by Sethu</sub>
</p>

<p align="center">
  <img alt="Platform" src="https://img.shields.io/badge/Platform-Web-0f172a?style=for-the-badge">
  <img alt="Stack" src="https://img.shields.io/badge/Stack-HTML%20%7C%20CSS%20%7C%20JavaScript-1d4ed8?style=for-the-badge">
  <img alt="Storage" src="https://img.shields.io/badge/Storage-LocalStorage-059669?style=for-the-badge">
  <img alt="Status" src="https://img.shields.io/badge/Status-Self--Contained-f59e0b?style=for-the-badge">
</p>

---

## Overview

**Asset Intelligence Dashboard** is a self-contained web application for stock analysis, watchlist discovery, and holdings management. It combines **technical signals**, **fundamental checks**, **news-aware scoring**, **quick-pick workflows**, and **portfolio planning tools** into a single HTML dashboard that runs directly in a browser.

It is designed for users who want a practical, fast, and highly visual interface for:

- analyzing stocks in a personalized workspace,
- reviewing curated picks,
- tracking holdings and risk,
- saving and restoring dashboard state locally,
- experimenting with scoring models without depending on a backend.

Because the application is packaged as a single page, it is easy to fork, customize, and host through GitHub Pages or run locally.

---

## Key Highlights

### Stocks Analytics
The **Stocks Analytics** tab is the main analysis workspace. It supports adding tickers, refreshing live analysis, and reviewing scoring outputs that bring together market data, technical indicators, trend structure, risk metrics, and simplified decision signals.

Highlights include:

- ticker-based stock analysis,
- signal classification such as **Buy**, **Hold**, **Trim**, and **Sell**,
- summary chips and market status display,
- technical breakdowns such as RSI, moving averages, MACD, volume context, and pattern labels,
- simplified fundamentals and risk positioning views,
- card-based visual layout for rapid review.

### Quick Picks
The **Quick Picks** section is optimized for exploration and speed. It presents curated stock ideas and lets you move candidates into your main analytics workflow with minimal friction.

Highlights include:

- quick-add cards for curated names,
- multiple grouped pick lists,
- verified/candidate style filtering behavior,
- NYSE and CAN SLIM-inspired scanning components,
- watchlist and alert concepts for idea development.

### My Holdings
The **My Holdings** module supports portfolio tracking and trade-planning logic.

Highlights include:

- save ticker, average cost, quantity, and cash balance,
- view unrealized P/L and portfolio totals,
- track technical, fundamental, sentiment, and AI-style outputs together,
- review targets, stops, allocation guidance, and alert stacks,
- maintain a more operational view of open positions.

### Save / Export / Import
The dashboard includes local persistence and backup workflow support.

Highlights include:

- **Save Dashboard** to persist state locally,
- **Export** to generate a JSON backup,
- **Import** to restore a prior saved state,
- browser-based persistence using `localStorage`.

---

## Feature Breakdown

## 1) Unified Multi-Tab Workflow
The dashboard organizes work into three major operating areas:

- **Stocks Analytics** – deep analysis and ticker review,
- **Quick Picks** – shortlist discovery and candidate onboarding,
- **My Holdings** – portfolio monitoring, allocation, and exit planning.

This structure makes the application useful for both idea generation and active position management.

## 2) Market and Signal Logic
The application includes a broad set of analysis helpers that support structured decision-making.

Examples include:

- market status checks,
- trend inspection,
- technical ratings,
- risk scoring,
- pattern labeling,
- rule-engine signal fallback,
- AI-style narrative signal support.

## 3) Holdings Intelligence
The holdings tab is more than a simple ledger. It brings together:

- current market price vs average cost,
- position-level targets and stops,
- sentiment and divergence-style awareness,
- action cues such as **Buy More**, **Hold**, or **Reduce**,
- cash-aware trade planning and allocation suggestions.

## 4) Self-Contained Operation
This project is intentionally lightweight from a deployment standpoint.

Benefits include:

- no required backend,
- easy local execution,
- simple GitHub hosting,
- direct modification through a single HTML file,
- portability for personal investing workflows and experimentation.

---

## Screens / Functional Areas

### Header and Utility Controls
The top bar can be branded for personal use and includes utility actions such as:

- save dashboard state,
- export backup,
- import backup,
- refresh the workspace.

### Stocks Analytics Cards
The card-based layout is built for quick scanning of multiple names while still exposing useful detail such as:

- price and daily change,
- signal badge,
- confidence or scoring context,
- technical panels,
- fundamentals panels,
- pattern observations,
- latest-news snippets,
- update timestamps.

### Quick Picks Board
Quick Picks is purpose-built for fast onboarding of names into the main workflow. It emphasizes:

- curated ideas,
- sector grouping,
- one-click add behavior,
- shortlist review,
- optional scanning extensions.

### Holdings Dashboard
The holdings screen shifts the focus from screening to management. It emphasizes:

- position accounting,
- tactical monitoring,
- planning targets,
- trailing stop concepts,
- portfolio-level summaries.

---

## Tech Stack

- **HTML5**
- **CSS3**
- **Vanilla JavaScript**
- **Browser Local Storage** for persistence

No build pipeline is required for basic usage.

---

## Repository Structure

```text
.
├── index.html        # Main application
├── README.md         # Project documentation
└── assets/           # Optional screenshots, icons, or supporting images
```

> If you keep everything in a single-file deployment model, `index.html` is the only runtime artifact required.

---

## Getting Started

## Option 1: Run Locally
1. Download or clone this repository.
2. Open `index.html` in a modern browser.
3. Start using the dashboard immediately.

## Option 2: Serve Locally for Development
If your browser restricts certain fetch behavior in local-file mode, use a lightweight local server.

### Python
```bash
python -m http.server 8080
```

Then open:

```text
http://localhost:8080
```

## Option 3: Host on GitHub Pages
1. Push the repository to GitHub.
2. Enable **GitHub Pages** in repository settings.
3. Serve from the root or `main` branch.
4. Open the published project URL.

---

## How to Use

### Analyze a Stock
1. Open **Stocks Analytics**.
2. Enter a ticker symbol.
3. Add the stock.
4. Refresh analysis if needed.
5. Review the generated cards, ratings, and technical/fundamental breakdown.

### Use Quick Picks
1. Open **Quick Picks**.
2. Browse the curated categories or scanner-derived listings.
3. Add a pick to the analytics workspace.
4. Review it in **Stocks Analytics** for deeper inspection.

### Track Holdings
1. Open **My Holdings**.
2. Add ticker, average price, quantity, and optional cash balance.
3. Refresh holdings analysis.
4. Review P/L, targets, stops, allocation guidance, and alerts.

### Save and Restore
1. Click **Save Dashboard** to persist the current dashboard state locally.
2. Click **Export** to download a backup as JSON.
3. Click **Import** to restore a previously exported backup.

---

## Data Persistence Model

The dashboard uses browser storage to maintain state between sessions.

Typical stored data includes:

- stock analytics state,
- holdings state,
- cash balance,
- quick-pick cache,
- scanner data,
- watchlist and alert data.

Because the storage is local to the browser profile, users should export backups if they want a portable copy.

---

## Customization Guide

This project is a strong base for extension. Common customization directions include:

### Branding
You can customize:

- application title,
- subtitle or author line,
- header actions,
- visual theme and accent colors.

### Strategy Logic
You can adapt:

- technical scoring thresholds,
- signal logic,
- risk calculations,
- allocation logic,
- quick-pick curation,
- holdings action rules.

### User Experience
You can enhance:

- auto-save indicators,
- toast notifications,
- mobile layout,
- charts and mini-visualizations,
- card density and table behavior.

---

## Suggested Enhancements

If you want to evolve the dashboard further, strong next steps include:

- **modularizing** the single HTML file into separate HTML/CSS/JS assets,
- adding **screenshot previews** to the repository,
- documenting **data-source behavior** more explicitly,
- improving the **mobile responsive layout**,
- introducing **versioned backup snapshots**,
- layering in **performance optimizations** for heavier scanning workflows.

---

## Screenshots

Create a folder such as `assets/` and add screenshots, then reference them here.

Example:

```md
## Screenshots

### Dashboard Overview
![Dashboard Overview](assets/dashboard-overview.png)

### Quick Picks
![Quick Picks](assets/quick-picks.png)

### Holdings View
![Holdings View](assets/holdings-view.png)
```

---

## Deployment Notes

This app is well-suited for:

- personal local use,
- static hosting,
- GitHub Pages,
- internal demos,
- rapid prototyping for investment analytics workflows.

If you plan to share the project publicly, consider documenting:

- data-source assumptions,
- browser compatibility,
- privacy considerations around local storage,
- limitations of any AI-style or rule-based outputs.

---

## Disclaimer

This project is intended for **educational, research, and personal productivity purposes only**.

It does **not** provide financial advice, investment recommendations, or guarantees of performance. Any scoring, signals, target ranges, or risk indicators should be treated as informational aids only.

Always perform your own due diligence before making investment decisions.

---

## Author

**Sethuraman Lakshminarayanan**
Malaysia (Remote)

If you fork this project, feel free to customize the branding and strategy logic for your own workflow.

---

## License

Add your preferred license here.

Examples:

- MIT License
- Apache 2.0
- Proprietary / Personal Use Only

---

## Contributing

If you want to evolve this into a more open community project, add contribution guidelines such as:

- issue templates,
- coding standards,
- feature request categories,
- pull request expectations.

---

## Star This Project

If this dashboard helps your workflow, consider starring the repository and keeping a changelog for your future enhancements.
