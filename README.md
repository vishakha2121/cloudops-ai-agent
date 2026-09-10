<h1 align="center">☁️ CloudOps AI Agent</h1>

<h3 align="center">Autonomous Multi-Cloud Operations Platform</h3>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.11-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/FastAPI-0.109-009688?style=for-the-badge&logo=fastapi&logoColor=white" />
  <img src="https://img.shields.io/badge/React-18-61DAFB?style=for-the-badge&logo=react&logoColor=black" />
  <img src="https://img.shields.io/badge/Gemini-AI-4285F4?style=for-the-badge&logo=google&logoColor=white" />
  <img src="https://img.shields.io/badge/PostgreSQL-15-336791?style=for-the-badge&logo=postgresql&logoColor=white" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" />
  <img src="https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge" />
</p>

<p align="center">
  An AI-powered autonomous agent that monitors <b>AWS</b>, <b>Azure</b>, and <b>GCP</b> infrastructure —
  detects anomalies in real-time, predicts outages before they occur, optimizes cloud costs,
  and delivers intelligent recommendations through a beautiful unified dashboard.
</p>

---

## 📖 Table of Contents

- [About the Project](#-about-the-project)
- [Key Features](#-key-features)
- [System Architecture](#-system-architecture)
- [Tech Stack](#-tech-stack)
- [Project Structure](#-project-structure)
- [Getting Started](#-getting-started)
  - [Prerequisites](#prerequisites)
  - [Backend Setup](#backend-setup)
  - [Frontend Setup](#frontend-setup)
  - [Database Setup](#database-setup)
- [Environment Variables](#-environment-variables)
- [API Endpoints](#-api-endpoints)
- [Screenshots](#-screenshots)
- [How It Works](#-how-it-works)
- [Roadmap](#-roadmap)
- [Contributing](#-contributing)
- [License](#-license)
- [Contact](#-contact)

---

## 🎯 About the Project

**CloudOps AI Agent** is an intelligent infrastructure monitoring and optimization system that autonomously watches over multi-cloud environments. Unlike traditional monitoring tools, it uses **Google's Gemini AI** combined with **machine learning algorithms** to:

- 🔍 Detect anomalies in real-time before they escalate
- 🔮 Predict potential outages using time-series forecasting
- 💰 Identify cost-optimization opportunities automatically
- 🧠 Generate actionable infrastructure recommendations
- 💬 Provide a ChatGPT-style AI assistant for cloud operations

This project was built as a **learning-focused, practice-level implementation** demonstrating how modern AI can be combined with cloud operations (CloudOps) to create an autonomous agent.

---

## ✨ Key Features

| Feature | Description |
|---------|-------------|
| 🌐 **Multi-Cloud Monitoring** | Unified view of AWS, Azure, and GCP resources |
| 🤖 **AI Anomaly Detection** | Isolation Forest + Gemini AI for detecting outliers |
| 🔮 **Outage Prediction** | Time-series forecasting to predict failures |
| 💵 **Cost Optimization** | Automated recommendations to reduce cloud spend |
| 💬 **AI Chat Assistant** | Conversational interface for cloud queries |
| 📊 **Real-Time Dashboards** | Live metrics with interactive charts |
| 🔔 **Smart Alerts** | Context-aware notifications via email/Slack |
| 📈 **Prometheus + Grafana** | Industry-standard monitoring integration |
| 🛠️ **Terraform Suggestions** | AI-generated infrastructure-as-code recommendations |
| ☸️ **Kubernetes Native** | Deployable on any K8s cluster |
| 🔐 **JWT Authentication** | Secure login and role-based access |
| ⚡ **WebSocket Updates** | Real-time data streaming to the frontend |

---

## 🏗️ System Architecture



---

## 🧰 Tech Stack

### Backend
- **Python 3.11** — Core language
- **FastAPI** — Modern async web framework
- **SQLAlchemy** — ORM for database
- **Alembic** — Database migrations
- **Pydantic** — Data validation
- **JWT (python-jose)** — Authentication
- **APScheduler** — Background jobs
- **WebSockets** — Real-time communication

### AI / ML
- **Google Gemini API** — LLM for recommendations
- **scikit-learn** — Isolation Forest for anomalies
- **statsmodels** — ARIMA time-series forecasting
- **pandas / numpy** — Data processing

### Frontend
- **React 18** — UI library
- **Vite** — Fast build tool
- **Redux Toolkit** — State management
- **React Router v6** — Routing
- **TailwindCSS** — Styling
- **shadcn/ui** — Beautiful components
- **Recharts** — Charts and graphs
- **Axios** — HTTP client
- **Framer Motion** — Animations

### Database & Cache
- **PostgreSQL** — Primary database
- **SQLite** — Development fallback
- **Redis** — Caching & sessions

### DevOps & Monitoring
- **Docker & Docker Compose** — Containerization
- **Kubernetes** — Orchestration
- **Terraform** — Infrastructure as Code
- **Prometheus** — Metrics collection
- **Grafana** — Visualization
- **GitHub Actions** — CI/CD

---

## 📁 Project Structure



---

## 🚀 Getting Started

### Prerequisites

Make sure you have installed:

- **Python 3.11+** → [Download](https://www.python.org/downloads/)
- **Node.js 18+** → [Download](https://nodejs.org/)
- **PostgreSQL 15+** → [Download](https://www.postgresql.org/download/)
- **Git** → [Download](https://git-scm.com/)
- **Gemini API Key** → [Get Free Key](https://aistudio.google.com/app/apikey)
- *(Optional)* **Docker** → [Download](https://www.docker.com/)

---

### Backend Setup

```bash
# 1. Navigate to backend
cd backend

# 2. Create virtual environment
python -m venv venv

# 3. Activate it
# Windows:
venv\Scripts\activate
# Mac/Linux:
source venv/bin/activate

# 4. Install dependencies
pip install -r requirements.txt

# 5. Copy environment file
cp .env.example .env
# Edit .env and add your GEMINI_API_KEY and DATABASE_URL

# 6. Run migrations
alembic upgrade head

# 7. Seed sample data (optional)
python scripts/seed_data.py

# 8. Start the server
uvicorn app.main:app --reload --port 8000


# 1. Navigate to frontend
cd frontend

# 2. Install dependencies
npm install

# 3. Copy environment file
cp .env.example .env
# Edit .env and set VITE_API_URL=http://localhost:8000

# 4. Start dev server
npm run dev