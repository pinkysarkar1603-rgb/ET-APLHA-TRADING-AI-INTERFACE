# ET Alpha

ET Alpha is an AI-powered market intelligence platform for Indian equities. It combines live market data, technical indicators, AI analysis, candlestick intelligence, factor attribution, natural-language screening, and deep visual research tools in one product.

The goal is to make market understanding faster and more accessible without reducing everything to a plain chatbot or a static dashboard.
## KINDLY OPEN ET-A78-COPY ZIP FILE AND DOWNLOAD RAW FILE, THEN FOLLOW THE INSTRUCTIONS BELOW.
By Developer- Akshat Sarkar

## What ET Alpha Includes

- Live market dashboard with real indicator-backed signal cards
- Candlestick chart intelligence with AI technical analysis
- Candle-click move blueprint for domestic, global, sector, and company drivers
- `DATA` page with a searchable indicator catalog and fullscreen chart overlays
- `Bharat Intelligence` page for natural-language India-first stock screening
- `Radar` workspace for compare, rotation, events, impact, alerts, watchlists, and explain flows
- `Intel` and `Info` views for headline context, factor mapping, and chart research
- Groq-powered analysis layers with graceful fallback behavior

## Main Product Areas

### Markets
The primary signal workspace. This page focuses on:
- live ticker snapshots
- conviction and trend scoring
- support and resistance
- technical setup context
- AI analysis on selected names

### Info
The chart-research layer. This includes:
- candlestick charts
- candle-click move explanation
- trade map framing
- sentiment and research modules

### Intel
The external-driver layer for:
- headline-linked market context
- domestic vs global factor mapping
- sector and company trigger summaries

### Radar
A multi-workflow workspace for:
- Signals
- Compare
- Rotation
- Events
- Impact
- Alerts
- Lab
- Watchlist
- Earnings
- Explain

### Bharat Intelligence
An accessibility-focused page for India-first workflows such as:
- natural-language stock screening
- Hinglish and simple search flows
- macro and report surfaces
- learning and trust-oriented explanations

### DATA
A dedicated analytics lab that includes:
- searchable technical indicator catalog
- indicator spotlight with AI explanation
- fullscreen candlestick mode
- indicator overlays applied directly on the central chart
- multiple data visuals for broader market exploration

## Tech Stack

### Frontend
- React
- TypeScript
- Vite
- Framer Motion
- Recharts

### Backend
- FastAPI
- Python
- indicator computation utilities
- market data aggregation routes

### AI
- Groq API for technical analysis, indicator narratives, and explanation layers

### Data Sources
- Yahoo Finance chart/search endpoints for live market context
- internal indicator engine for computed technical signals

## Repository Structure

```text
et78/
├─ backend/        # FastAPI backend, tools, APIs, signal engine
├─ frontend/       # React + TypeScript frontend
├─ data/           # local project data assets
├─ docs/           # supporting docs
├─ setup.bat       # Windows setup helper
├─ start.bat       # Windows run helper
└─ README.md
```

## Important Note Before Running

This repository does **not** include `frontend/node_modules` or `backend/.venv` in GitHub. They were intentionally removed to keep the repository size manageable.

That means after cloning or downloading the project, you must reinstall dependencies locally before running it.

## Requirements

- Node.js 18+
- npm
- Python 3.11 recommended for the backend

Python 3.11 is recommended because some backend dependencies may fail or compile badly on newer Python versions such as 3.13 or 3.14.

## Setup

### 1. Clone or download the project

Place the project anywhere on your machine, then open a terminal in the root folder.

### 2. Install frontend dependencies

```powershell
cd frontend
npm install
cd ..
```

### 3. Create a backend virtual environment

```powershell
cd backend
py -3.11 -m venv .venv
.venv\Scripts\activate
python --version
pip install --upgrade pip
pip install -r requirements.txt
cd ..
```

If you are using Command Prompt instead of PowerShell:

```cmd
cd backend
py -3.11 -m venv .venv
.venv\Scripts\activate.bat
python --version
pip install --upgrade pip
pip install -r requirements.txt
cd ..
```

## How To Run

Run the frontend and backend in two separate terminals.

### Terminal 1: Backend

```powershell
cd backend
.venv\Scripts\activate
uvicorn api.main:app --reload --port 8000
```

If you are in Command Prompt:

```cmd
cd backend
.venv\Scripts\activate.bat
uvicorn api.main:app --reload --port 8000
```

### Terminal 2: Frontend

```powershell
cd frontend
npm run dev
```

### Open In Browser

- Frontend: [http://localhost:5173](http://localhost:5173)
- Backend health check: [http://localhost:8000/api/health](http://localhost:8000/api/health)

## One-Click Windows Helpers

The repository also includes:

- `setup.bat`  
  Installs frontend dependencies, backend requirements, and Playwright Chromium.

- `start.bat`  
  Starts the frontend and backend in separate command windows.

These helpers are useful on Windows, but the manual steps above are the clearest and most reliable.

## How To Use ET Alpha

### Markets
Open `Markets` to view the live signal workspace. Select a stock to inspect:
- trend
- conviction
- support and resistance
- AI market summary

### Info
Open `Info` to explore candlesticks and click any candle to inspect:
- move blueprint
- possible price drivers
- supporting headlines
- trade map framing

### Intel
Open `Intel` to inspect:
- domestic factors
- global factors
- sector forces
- company triggers

### Radar
Open `Radar` when you want multi-stock workflows like:
- compare mode
- event mapping
- rotation
- alerts
- watchlists
- stock explanation tools

### Bharat Intelligence
Open `Bharat Intelligence` to use natural-language style screening. Example queries:
- `reliance`
- `railway stocks below 500`
- `bullish IT stocks near 52 week high`

### DATA
Open `DATA` for deep technical exploration:
- search any indicator from the catalog
- choose a stock
- click `Enlarge`
- use the left indicator sidebar
- watch the selected indicator affect the center candlestick chart directly

## Troubleshooting

### Frontend does not start

Run:

```powershell
cd frontend
npm install
npm run dev
```

### Backend dependency install fails

Make sure you are using Python 3.11:

```powershell
py -3.11 --version
```

Then recreate the environment:

```powershell
cd backend
py -3.11 -m venv .venv
.venv\Scripts\activate
pip install --upgrade pip
pip install -r requirements.txt
```

### Backend starts but imports fail

This usually means the environment is not active or requirements were not fully installed. Activate `.venv` first, then run the install command again.

### Pages load but feel incomplete

Check that:
- frontend is running on `5173`
- backend is running on `8000`
- the browser was refreshed after backend/frontend restarts

## Notes

- This project uses real fetched market context wherever available.
- AI outputs are intended as market intelligence, not regulated investment advice.
- Some features degrade gracefully if an AI request or external fetch is temporarily unavailable.

## Disclaimer

ET Alpha is a research and analytics platform. It is **not** a SEBI-registered investment advisor and should not be treated as a source of regulated investment advice.
