# 🛰️ NAKSHTRA – Orbital Guard AI
### AI-Powered Space Debris Collision Prediction & Avoidance System

[![Python](https://img.shields.io/badge/Python-3.11-blue.svg)](https://www.python.org/)
[![React](https://img.shields.io/badge/React-18-61dafb.svg)](https://reactjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.0-3178c6.svg)](https://www.typescriptlang.org/)
[![Docker](https://img.shields.io/badge/Docker-Ready-2496ed.svg)](https://www.docker.com/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

**NAKSHTRA (Orbital Guard AI)** is an AI-driven **space traffic monitoring and collision avoidance system** designed to analyze satellite orbits, detect potential conjunction events, and generate optimal avoidance strategies using orbital mechanics and machine learning.

The platform simulates next-generation **space situational awareness systems** used by aerospace organizations to monitor satellites and space debris.

*Originally developed during the **Hyperspace Innovation Hackathon**, this project was later refined and documented for demonstration and portfolio purposes.*

---

# 🌍 Live Demo

### Frontend Deployment (Vercel)

🔗 https://frontend-rose-beta-63.vercel.app/

⚠️ **Note**

The current deployment contains **only the frontend visualization layer**.

Backend services such as:

- Satellite data ingestion
- Orbital propagation
- Machine learning prediction
- Collision probability calculation

require **local or cloud deployment using Docker**.

---

# 🌟 Key Features

## 🛰️ Real-Time Satellite Monitoring

- Tracks **23,000+ satellites and debris objects**
- Live **Two-Line Element (TLE)** data from **Celestrak API**
- Automatic orbital updates
- Real-time event notifications using **WebSockets**

---

## 🤖 Multi-Layer AI Collision Prediction

NAKSHTRA uses a **four-layer analytical architecture**:

1️⃣ **SGP4 Orbital Propagation**  
Industry-standard orbital mechanics model used by NASA.

2️⃣ **Foster 3D Probability of Collision (PoC)**  
Analytical model for calculating collision likelihood.

3️⃣ **Machine Learning Risk Model**  
Neural network (PyTorch) estimating collision probability.

4️⃣ **Maneuver Optimization Engine**  
Computes optimal **ΔV adjustments** for satellite avoidance.

---

## 🎬 Interactive Visualization

- 🌍 3D Earth visualization using **Three.js**
- 🛰️ Satellite orbit rendering
- ⏱️ Conjunction event playback timeline
- 📊 Risk analytics dashboard
- 🔔 Real-time alert notifications

---

# 🚀 Quick Start

## Prerequisites

- Docker Desktop or Docker Engine
- Docker Compose
- Minimum **2GB RAM**
- **5GB disk space**

---

## Run the Entire System

```bash
git clone https://github.com/imsohail07/Nakshatra_SpaceDebris.git

cd Nakshatra_SpaceDebris

docker-compose up -d
```

## Access the Application

### Frontend
```
http://localhost:3000
```

### Backend API
```
http://localhost:8000/docs
```

Swagger documentation will be available for testing endpoints.

---

# 💻 Development Setup

## Backend

```bash
cd backend
pip install -r requirements.txt
python -m uvicorn api_server:app --reload --port 8000
```

## Frontend

```bash
cd frontend
npm install
npm run dev
```

---

# 🏗 System Architecture

```
User Browser
     │
     ▼
React + Three.js Frontend
     │
     ▼
nginx Reverse Proxy
     │
     ▼
FastAPI Backend Server
     │
 ┌───┴──────────────┐
 │                  │
 ▼                  ▼
Machine Learning   Orbital Mechanics
(PyTorch)          (SGP4 + Foster PoC)
 │
 ▼
Celestrak Satellite Data API
```

---

# 🧠 Technology Stack

## Backend

- FastAPI
- PyTorch
- NumPy
- SciPy
- SGP4 Orbital Propagation
- WebSockets

## Frontend

- React 18
- TypeScript
- Three.js (WebGL)
- Tailwind CSS
- Vite Build System

## DevOps

- Docker
- Docker Compose
- nginx Reverse Proxy
- Containerized Microservices Architecture

---

# 📁 Project Structure

```
Nakshatra_SpaceDebris

backend
 ├ api_server.py
 ├ collision_ml_model.py
 ├ live_tle_fetcher.py
 ├ websocket_manager.py
 ├ synthetic_conjunctions.py
 └ requirements.txt

frontend
 ├ src
 │ ├ components
 │ │ ├ SimulationScene3D.tsx
 │ │ ├ AdvancedAnalyticsPanel.tsx
 │ │ ├ ConjunctionPlayback.tsx
 │ │ └ RiskTrendsChart.tsx
 │
 ├ package.json
 └ nginx.conf

docker-compose.yml
README.md
```

---

# 📡 API Endpoints

## REST API

```
GET /api/satellites
GET /api/conjunctions
POST /api/predict
GET /api/health
```

## WebSocket

```
ws://localhost:3000/ws/conjunctions
```

Streams real-time conjunction alerts.

---

# 📊 Performance Metrics

| Metric | Value |
|------|------|
| API Response | <200ms |
| WebSocket Latency | <50ms |
| 3D Rendering | 60 FPS |
| Memory Usage | ~500MB |
| System Startup | ~30 seconds |

---

# 🔐 Security Features

- Configured CORS policies
- nginx security headers
- Container isolation
- Environment variable configuration
- Health monitoring endpoints

---

# 🎓 Educational Value

This project demonstrates:

- Full-stack AI system design
- Real-time WebSocket architecture
- 3D satellite visualization using WebGL
- Aerospace orbital mechanics algorithms
- Machine learning integration
- Docker containerization
- Microservices architecture

---

# 🚀 Future Enhancements

- Historical conjunction database
- Automated maneuver simulation
- Satellite telemetry integration
- PDF risk reports
- CI/CD pipeline with GitHub Actions
- Cloud deployment with Kubernetes

---

# 📄 License

MIT License

---

# 👥 Team & Acknowledgment

This project was originally developed during the **Hyperspace Innovation Hackathon** by **Team Alchemist**.

### Team Members

- **Sohail Shirazi**
- **G Varun**
- **Aditi Singh**
- **Simran Hati**
- **Siddhi G**

---

*Note:* This repository contains the version maintained and documented by **Sohail Shirazi** as part of his project portfolio.

⭐ If you find this project useful, please consider giving it a star.
