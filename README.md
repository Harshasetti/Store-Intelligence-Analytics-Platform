# Store Intelligence Analytics Platform

## Overview

Store Intelligence Analytics Platform is an AI-powered retail analytics system that uses computer vision and data analytics to monitor customer behavior inside retail stores. The solution detects and tracks customers from video feeds, generates events, stores analytics data, and visualizes insights through interactive dashboards.

## Features

* YOLOv8-based person detection
* Multi-person tracking
* Entry and Exit detection
* Zone-based customer movement analysis
* Conversion funnel analytics
* Store heatmap generation
* Anomaly detection
* FastAPI REST APIs
* SQLite data storage
* Streamlit dashboard

## Technology Stack

* Python
* FastAPI
* Streamlit
* YOLOv8
* OpenCV
* SQLite
* Pandas
* NumPy

## Project Architecture

Video Feed
→ YOLO Detection
→ Person Tracking
→ Event Generation
→ SQLite Database
→ FastAPI APIs
→ Streamlit Dashboard

## API Endpoints

### Metrics

GET /stores/{store_id}/metrics

Returns:

* Unique visitors
* Entries
* Exits

### Funnel

GET /stores/{store_id}/funnel

Returns:

* Entry count
* Zone visits
* Billing visits
* Purchase conversions

### Heatmap

GET /stores/{store_id}/heatmap

Returns:

* Zone-wise visitor counts

### Anomalies

GET /stores/{store_id}/anomalies

Returns:

* Operational alerts
* Traffic anomalies

## Installation

```bash
pip install -r requirements.txt
```

## Run FastAPI

```bash
python -m uvicorn app.main:app --reload
```

## Run Detection

```bash
python pipeline/detect.py
```

## Send Events

```bash
python pipeline/send_events.py
```

## Run Dashboard

```bash
python -m streamlit run dashboard/streamlit_app.py
```

## Dashboard

The dashboard provides:

* Visitor Analytics
* Conversion Funnel
* Zone Heatmap
* Anomaly Detection
* Real-time Metrics

## Project Outcome

The platform enables retailers to understand customer behavior, optimize store layouts, improve conversion rates, and make data-driven decisions using AI-powered analytics.
