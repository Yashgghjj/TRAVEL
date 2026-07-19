# AI Smart Travel Planner

A modern, full-stack travel planning platform with AI-powered itinerary generation, budget forecasting, route optimization, saved trips, auth, chatbot support, voice input, and a premium glassmorphism dashboard UI.

## Stack

- Frontend: React + Vite + Framer Motion
- Backend: FastAPI + Scikit-learn + Pandas
- Database: MongoDB
- APIs: OpenWeatherMap + Google Distance Matrix hooks

## Features

- Personalized recommendations by destination, budget, days, and interests
- ML budget prediction (hotel, food, transport) with breakdown
- Route optimization using nearest total path estimation
- Day-wise timeline with attractions and cost
- Weather/map integration points (real keys supported through env)
- Login/signup, save trips, chatbot, voice destination input
- Safety alert logic for scam/fraud awareness
- Responsive premium UI, dark/light mode, animated cards

## Project Structure

```text
travel/
  backend/
    app/
      routers/
      services/
    data/
  frontend/
    src/
```

## Local Setup

### 1) Backend

```bash
cd backend
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
copy .env.example .env
uvicorn app.main:app --reload
```

### 2) Frontend

```bash
cd frontend
npm install
npm run dev
```

Open `http://localhost:5173`.

## Environment Variables

Set in `backend/.env`:

- `MONGO_URI`
- `MONGO_DB_NAME`
- `JWT_SECRET`
- `OPENWEATHER_API_KEY`
- `GOOGLE_MAPS_API_KEY`

## Deployment-Ready Targets

- Frontend: Vercel
- Backend: Render / Railway
- MongoDB: MongoDB Atlas

Use the same env variables in deployment dashboard secrets.

## Docker Compose

```bash
docker compose up --build
```

- Frontend: `http://localhost:5173`
- Backend: `http://localhost:8000`
- MongoDB: `mongodb://localhost:27017`
