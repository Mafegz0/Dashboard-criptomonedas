# Replit.md

## Overview

This is a real-time cryptocurrency price visualizer built as a single-page web application. It connects to the Binance WebSocket API to stream live prices for Bitcoin, Ethereum, Monero, and Litecoin, and displays them using D3.js for data visualization. The project is a simple front-end only application with no backend server — it consists of vanilla HTML, CSS, and JavaScript.

**Important note:** The project appears to be incomplete. The `script.js` file is cut off mid-function, meaning the core logic for processing incoming price data, updating the data model, and rendering the D3.js visualization is not yet implemented.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Front-End Architecture
- **Pure vanilla stack**: HTML + CSS + JavaScript with no build tools, frameworks, or bundlers. Files are served directly.
- **Entry point**: `index.html` loads `style.css` and `script.js`, plus D3.js from a CDN.
- **UI components**:
  - A dropdown (`<select>`) lets users pick which cryptocurrency to view (Bitcoin, Ethereum, Monero, Litecoin).
  - `#modulo1` contains two paragraph elements (`#contexto1`, `#contexto2`) intended for displaying textual price info (current price, high/low, etc.).
  - `#modulo2` is an empty div intended for the D3.js chart/visualization.
  - `#descripcion` provides static descriptive text about the dashboard.

### Data Flow
1. A WebSocket connection is opened to Binance's public streaming API (`wss://stream.binance.com:9443/stream?streams=...`) subscribing to mini ticker streams for BTCUSDT, ETHUSDT, XMRUSDT, and LTCUSDT.
2. Incoming messages are parsed from JSON. The symbol is mapped from Binance format (e.g., `BTCUSDT`) to a friendly name (e.g., `bitcoin`) using a lookup object.
3. A data model (`monedas` array) tracks for each coin: `precioActual`, `precioMasAlto`, `precioMasBajo`, and a `datos` array (intended to store historical price points for charting).
4. The processing function (`procesarNuevoMensaje`) is incomplete and needs to: update the data model, compute min/max prices, push to the `datos` array, and trigger D3.js re-renders.

### What Needs to Be Built
- Complete the `procesarNuevoMensaje` function to update the `monedas` data model with incoming prices.
- Build the D3.js visualization in `#modulo2` — likely a line chart showing price over time for the selected cryptocurrency.
- Wire up the dropdown menu so changing the selection updates the displayed chart and text info.
- Populate `#contexto1` and `#contexto2` with relevant price information (current price, high, low, percentage change, etc.).

### Design Decisions
- **No backend**: All data comes directly from Binance's public WebSocket API in the browser. This keeps the architecture simple but means no data persistence.
- **D3.js v7.3.0 via CDN**: Chosen for flexible, low-level control over data visualization. An alternative would be Chart.js for simpler charts, but D3 allows more customization.
- **Vanilla JS (no framework)**: Keeps the project lightweight and dependency-free, appropriate for a small single-purpose dashboard.

## External Dependencies

### Third-Party Libraries
- **D3.js v7.3.0** — loaded from `cdnjs.cloudflare.com` CDN. Used for data-driven DOM manipulation and charting.

### External APIs
- **Binance WebSocket API** — `wss://stream.binance.com:9443/stream?streams=...` — Public, free, no authentication required. Streams real-time mini ticker data for cryptocurrency pairs (BTCUSDT, ETHUSDT, XMRUSDT, LTCUSDT). Each message includes the current price in the `data.c` field and the symbol in `data.s`.

### No Backend or Database
- This project has no server-side code, no database, and no authentication. It is a purely client-side application. If a backend is ever needed (e.g., for price history persistence), it would need to be added from scratch.