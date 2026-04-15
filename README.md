# SafeRoute AI 🛡️🗺️

**The Cybersecurity Dashboard for the Real World.**
SafeRoute AI is an intelligent navigation hackathon prototype that proves routing should prioritize *safety* instead of just *speed*. By cross-referencing real-time mapping data with dynamic hazard reports, SafeRoute vector-analyzes alternative route paths and provides you with the mathematically safest way home.

## ✨ Features
* **Safest Route Algorithm**: We don't just take Google's fastest route. SafeRoute fetches multiple alternative paths and runs interference checks against known hazards and "Safe Nodes" (hospitals, police stations) to serve you the absolute safest path.
* **Live Environmental Feed**: Simulates a live data connection using WebSockets and Google Gemini to inject real-time (mocked) hazard reports directly into your vicinity.
* **Premium Cyberpunk Dashboard**: A heavy dark-mode aesthetic utilizing Leaflet, custom styling, Map Vignettes, and glowing Neon Route highlighting.
* **Dynamic Risk UI**: Real-time evaluation dashboard grading your current route's safety score (A+ to D) dynamically as new reports arrive.
* **Emergency SOS Rerouting**: A high-visibility, pulsing SOS button that mathmatically calculates your proximity to the nearest verified Safe Node and instantly re-routes you in an emergency.

## 🛠️ Technology Stack
* **Frontend**: React, Vite, React-Leaflet, CartoDB Dark Matter, Vanilla CSS
* **Backend**: Python, FastAPI, WebSockets
* **APIs & AI**: Google Maps Directions & Places APIs, Google Gemini Flash 2.5 (Synthetic Hazard Generation)

## 🚀 Getting Started

### Prerequisites
You will need API keys for Google Maps and Google Gemini.
Create a `.env` file inside the `backend` directory:
```env
GOOGLE_MAPS_API_KEY=your_google_maps_key_here
GEMINI_API_KEY=your_gemini_key_here
```

### 1. Booting the Backend
Open a terminal and start the FastAPI server:
```bash
cd backend
pip install -r requirements.txt
uvicorn main:app --reload --port 8000
```

### 2. Booting the Frontend
Open a second terminal window for the React dashboard:
```bash
cd frontend
npm install
npm run dev
```

The application will now be running locally. Open your browser to the given Vite localhost address!

## 🌐 Deployment
SafeRoute is built securely to be deployed easily.
1. Deploy the `backend` directory as a Web Service on **Render** (using `uvicorn main:app --host 0.0.0.0 --port 10000`).
2. Update the `App.jsx` API/WS connection strings to point to your new Render URL.
3. Deploy the `frontend` directory as a Vite app on **Vercel**.
