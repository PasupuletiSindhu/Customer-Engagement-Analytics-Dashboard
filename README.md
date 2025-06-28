# 📊 AI-Enhanced Engagement Dashboard

> *Uncover insights with intelligent anomaly detection and real-time metrics*

A unified analytics solution to track customer behavior and Reddit sentiment, equipped with real-time anomaly alerts and rich visualizations.

![Dashboard Preview](https://via.placeholder.com/800x400?text=Customer+Engagement+Dashboard)

## ✨ Highlights

- **🔍 Intelligent Anomaly Alerts** – Detects irregular activity using machine learning
- **🌐 Multi-Channel Metrics** – Aggregates data from customer sources and Reddit discussions
- **📊 Live Visual Analytics** – Interactive charts with data connections and anomaly cues
- **📧 Proactive Notifications** – Email alerts for data irregularities
- **📁 Easy Exports** – Downloadable CSV files for offline analysis
- **🌓 Theme-Aware UI** – Supports automatic light/dark mode switching

## 🧠 ML-Based Anomaly Monitoring

Utilizes Isolation Forest algorithms to detect spikes and dips in engagement data, providing timely alerts.

```
Spike detected on April 15
⚠️ Engagement exceeded typical levels by 30%
📧 Notification dispatched to team@company.com
```

## 🚀 System Overview

Three core components function in tandem:

```
┌─────────────────┐     ┌─────────────────┐     ┌─────────────────┐
│  React Frontend │────▶│  Express.js API │────▶│  FastAPI Engine │
└─────────────────┘     └─────────────────┘     └─────────────────┘
        ▲                       ▲                       ▲
        ▼                       ▼                       ▼
┌─────────────────┐     ┌─────────────────┐     ┌─────────────────┐
│   Interactive   │     │  Customer Data  │     │ ML Models and   │
│    UI/UX        │     │    Services     │     │ Data Processing │
└─────────────────┘     └─────────────────┘     └─────────────────┘
```

### Frontend (React + Vite)
- Responsive design using modular components
- Visuals powered by Chart.js and Recharts
- Detailed modals for deep data dives

### Backend (Node.js)
- API layer with Express.js
- Azure Anomaly Detector integration
- Automated reporting and notifications

### ML Engine (Python)
- FastAPI for lightweight inference
- Reddit data pulled via PRAW
- System metrics exposed via Prometheus

## 🛠️ Technologies Used

### UI/Frontend
- **React 19** – Functional, hook-based components
- **Vite** – Fast dev server and builds
- **Chart.js & Recharts** – Clean, interactive charts

### Server/API
- **Express.js** – Scalable REST services
- **Azure Anomaly Detector** – Cloud ML APIs
- **Node-cron & Nodemailer** – Scheduling + email alerts

### Anomaly Detection Layer
- **FastAPI** – Fast and efficient Python APIs
- **scikit-learn + Pandas** – ML logic and data wrangling
- **PRAW** – Reddit API client

## 🚀 Setup Instructions

### Requirements
- Node.js 18+
- Python 3.10+
- npm/yarn

### Installation

```bash
git clone https://github.com/yourusername/customer-engagement-dashboard.git
cd customer-engagement-dashboard

cd backend && npm install
cd ../frontend && npm install

cd ../anomaly-backend
python -m venv ../anomaly-env
source ../anomaly-env/bin/activate  # Windows: ..\anomaly-env\Scripts\activate
pip install -r requirements.txt
```

### Configuration

Create a `.env` file in `anomaly-backend` with the following:

```
DATA_DIR=data
SAMPLE_DATA_FILE=sampleData.json
ALLOWED_ORIGINS=http://localhost:5173
API_KEY=your_api_key
REDDIT_CLIENT_ID=your_reddit_client_id
REDDIT_CLIENT_SECRET=your_reddit_client_secret
```

### Run Services

```bash
# Node.js API
cd backend && node server.js

# FastAPI Anomaly Service
cd anomaly-backend && uvicorn main:app --reload

# React Frontend
cd frontend && npm run dev
```

Navigate to `http://localhost:5173` to explore the dashboard.

## 📈 Usage Scenarios

### Analyzing Customer Activity
- Choose a customer from the dropdown
- Observe metrics and AI-detected anomalies
- Set thresholds and receive alerts
- Export metrics via CSV

### Monitoring Reddit Sentiment
- Input subreddit and time range
- View community trends and flags
- Explore individual post details
- Set alerts for anomalous behavior

## 🔐 Security Measures

- API key access control
- Request throttling
- Input validation and sanitation
- Secure headers

## 🛤️ Roadmap

- [ ] Feedback sentiment classification
- [ ] More social platform integrations
- [ ] Categorized anomaly types
- [ ] Mobile app with notifications
- [ ] Custom widget support

## 📄 License

Licensed under the ISC License.

---

<p align="center">
  Crafted with ❤️ to empower smarter decisions
</p>
