# AI-Enhanced Engagement Dashboard

> Discover insights with intelligent anomaly detection and real-time metrics

A unified analytics solution to track customer behavior and Reddit sentiment, equipped with real-time anomaly alerts and detailed visualizations.

## Highlights

- Intelligent Anomaly Alerts – Detects irregular activity using machine learning  
- Multi-Channel Metrics – Aggregates data from customer sources and Reddit discussions  
- Live Visual Analytics – Interactive charts with data connections and anomaly indicators  
- Proactive Notifications – Email alerts for data irregularities  
- Easy Exports – Downloadable CSV files for offline analysis  
- Theme-Aware UI – Supports automatic light/dark mode switching  

## Machine Learning-Based Anomaly Monitoring

Employs Isolation Forest algorithms to detect spikes and dips in engagement data, delivering timely alerts.

```
Spike detected on April 15
Engagement exceeded typical levels by 30%
Notification dispatched to team@company.com
```

## System Overview

The platform is composed of three primary components that operate in coordination:

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
- Data visualizations powered by Chart.js and Recharts  
- Detailed modal views for granular data inspection  

### Backend (Node.js)

- REST API developed with Express.js  
- Integration with Azure Anomaly Detector  
- Automated reporting and email notification services  

### ML Engine (Python)

- FastAPI serving real-time ML inferences  
- Reddit data integration via PRAW  
- Metrics exposed through Prometheus  

## Technologies Used

### UI / Frontend

- React 19 – Functional component-based UI  
- Vite – Optimized for fast development and builds  
- Chart.js & Recharts – Interactive data visualizations  

### Server / API

- Express.js – Scalable API layer  
- Azure Anomaly Detector – Cloud-based anomaly detection  
- Node-cron and Nodemailer – Task scheduling and email alerts  

### Anomaly Detection

- FastAPI – Lightweight Python API for inference  
- scikit-learn and pandas – Core ML and data preprocessing  
- PRAW – Reddit API integration  

## Setup Instructions

### Requirements

- Node.js 18 or higher  
- Python 3.10 or higher  
- npm or yarn  

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

Create a `.env` file in the `anomaly-backend` directory with the following:

```
DATA_DIR=data
SAMPLE_DATA_FILE=sampleData.json
ALLOWED_ORIGINS=http://localhost:5173
API_KEY=your_api_key
REDDIT_CLIENT_ID=your_reddit_client_id
REDDIT_CLIENT_SECRET=your_reddit_client_secret
```

### Running the Services

```bash
# Start Node.js API
cd backend && node server.js

# Start FastAPI anomaly service
cd anomaly-backend && uvicorn main:app --reload

# Launch React frontend
cd frontend && npm run dev
```

Access the dashboard at: `http://localhost:5173`

## Usage Scenarios

### Customer Activity Monitoring

- Select a customer from the dropdown  
- View metrics with detected anomalies  
- Configure thresholds for alerts  
- Export selected metrics to CSV  

### Reddit Sentiment Analysis

- Input subreddit and desired time range  
- Analyze sentiment trends and flagged activity  
- Drill into individual post metrics  
- Set up alerts for unexpected behavior  

## Security Features

- API key-based authentication  
- Rate limiting and request throttling  
- Input validation and sanitization  
- Secure HTTP headers  

## Development Roadmap

- [ ] Sentiment classification of customer feedback  
- [ ] Integration with additional social platforms  
- [ ] Categorization of anomaly types  
- [ ] Mobile application with notifications  
- [ ] Support for custom visual widgets  
