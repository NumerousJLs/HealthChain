# HealthChain

HealthChain is a voice-based nutrition assistant built at Cal Hacks 11.0 and later selected for the Hume AI Startup Program. It turns meal conversations into structured nutrition records, tracks calorie and protein goals, and provides meal-history views through a Next.js frontend and Flask backend.

![HealthChain preview](preview.png)

## Core Flow

1. A user discusses a meal through Hume's empathic voice interface.
2. The backend uses Gemini to parse meals and nutrition targets into structured data.
3. Flask and SQLite persist meal records, goals, and history.
4. The Next.js interface displays progress and prior meals.

The repository also includes exploratory ChromaDB and Gemini work for healthier-meal recommendations. That prototype is separate from the primary meal-tracking flow.

## Technology

- Next.js, React, TypeScript, and Tailwind CSS
- Hume EVI for voice interaction
- Flask, SQLAlchemy, and SQLite
- Gemini for meal and target parsing

## Run Locally

Copy `.env.example` to `.env` and provide the required Hume and Gemini credentials.

```bash
cp .env.example .env
```

### Frontend

```bash
corepack enable
pnpm install
pnpm dev
```

### Backend

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r backend/src/requirements.txt
cd backend/src
python main.py
```

## Team

HealthChain was created by [Addy](https://github.com/addychen2), [Derek](https://github.com/dwstan), [Joshua](https://github.com/NumerousJLs), and [Steven](https://github.com/sanityl0st).

## Project Status

HealthChain is a hackathon prototype. The repository documents local setup and experimentation, not a production deployment or clinical nutrition service.
