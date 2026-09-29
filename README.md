# 🚚 Green Logistics Optimizer

### AI-Powered Route Optimization for Sustainable Logistics

Green Logistics Optimizer is a logistics intelligence platform designed to optimize delivery routes, estimate transportation carbon emissions, and forecast future demand.

The project combines **route optimization, machine learning, carbon estimation, and interactive map visualization** into a single platform for more efficient and sustainable logistics planning.

> 🏆 Developed for **Walmart Sparkathon 2025**

---

## 🎯 Problem

Modern logistics systems need to balance multiple objectives:

* Efficient delivery routes
* Transportation cost
* Vehicle and fuel constraints
* Delivery load
* Carbon emissions
* Future demand

Traditional route planning may not adequately account for these factors together.

Green Logistics Optimizer addresses this by combining optimization and machine learning techniques to support data-driven logistics decisions.

---

## 💡 Solution

The platform provides three major capabilities:

### 🗺️ Route Optimization

Generates optimized delivery routes based on logistics constraints such as:

* Vehicle type
* Fuel type
* Load weight
* Delivery locations

The optimization engine processes the input data and generates optimized waypoints that can be visualized on an interactive map.

### 🌱 Carbon Emission Estimation

Estimates the environmental impact associated with transportation based on relevant vehicle, fuel, load, and route parameters.

This allows logistics planning to consider both operational efficiency and environmental impact.

### 📈 Demand Forecasting

Uses **time-series forecasting** to estimate future logistics demand and support better planning.

The forecasting pipeline uses **Prophet** for demand prediction.

---

## 🏗️ System Architecture

```text
                        ┌──────────────────┐
                        │      User        │
                        └────────┬─────────┘
                                 │
                                 ▼
                     ┌─────────────────────┐
                     │   React + Vite      │
                     │     Frontend        │
                     └──────────┬──────────┘
                                │
                                ▼
                     ┌─────────────────────┐
                     │   Node.js +         │
                     │   Express Backend   │
                     └──────────┬──────────┘
                                │
              ┌─────────────────┼─────────────────┐
              │                 │                 │
              ▼                 ▼                 ▼
       ┌──────────────┐  ┌──────────────┐  ┌──────────────┐
       │    Route     │  │    Carbon    │  │  Forecasting │
       │ Optimization │  │   Estimator  │  │    Engine    │
       └──────┬───────┘  └──────────────┘  └──────┬───────┘
              │                                    │
              ▼                                    ▼
       ┌──────────────┐                    ┌──────────────┐
       │ Optimization │                    │    Prophet   │
       │  Algorithms  │                    │     Model    │
       └──────┬───────┘                    └──────┬───────┘
              │                                    │
              └────────────────┬───────────────────┘
                               ▼
                    ┌─────────────────────┐
                    │ Interactive         │
                    │ Logistics Dashboard │
                    └─────────────────────┘
```

---

## 🔄 Route Optimization Workflow

```text
Vehicle Type
      +
Fuel Type
      +
Load Weight
      +
Delivery Locations
      │
      ▼
┌──────────────────────┐
│ Optimization Engine  │
└──────────┬───────────┘
           │
           ▼
  Optimized Waypoints
           │
           ▼
┌──────────────────────┐
│ Map Visualization    │
└──────────────────────┘
```

The optimization backend exposes the optimized route information through an API, which is then consumed by the frontend for visualization.

---

## 📈 Forecasting Workflow

```text
Historical Logistics Data
          │
          ▼
    Data Preprocessing
          │
          ▼
      Prophet Model
          │
          ▼
   Demand Forecast
          │
          ▼
   Logistics Planning
```

Forecasting can help identify expected demand patterns and support proactive resource and route planning.

---

## ✨ Key Features

* 🚚 Vehicle-aware route optimization
* 🗺️ Interactive route visualization
* 🌱 Carbon emission estimation
* 📊 Demand forecasting
* 📍 Optimized waypoint generation
* ⛽ Fuel-type consideration
* ⚖️ Load-weight consideration
* 🔌 REST API integration
* 📈 Data-driven logistics planning

---

## 🛠️ Tech Stack

### Frontend

* React
* Vite
* JavaScript
* Leaflet

### Backend

* Node.js
* Express.js

### Machine Learning

* Python
* Prophet
* Optimization algorithms

### Database

* MongoDB

### Development

* Git
* GitHub
* REST APIs

---

## 📸 Application

### Dashboard

*Add your main dashboard screenshot here.*

```text
docs/
└── screenshots/
    ├── dashboard.png
    ├── route-optimization.png
    ├── carbon-analysis.png
    └── forecasting.png
```

### Route Optimization

*Show the optimized route and waypoints on the map.*

### Carbon Analysis

*Show the carbon-emission output generated by the system.*

### Demand Forecasting

*Show the forecasting visualization and predicted demand.*

---

## 👨‍💻 My Contribution

As part of the team, I contributed to the development of the Green Logistics Optimizer.

### My work included:

* Developed and integrated the logistics optimization workflow.
* Worked on the route optimization API and optimized waypoint generation.
* Integrated the machine-learning backend with the application.
* Worked on map-based visualization of optimized routes.
* Contributed to carbon-emission estimation and logistics analysis.
* Integrated vehicle type, fuel type, and load-weight parameters into the optimization workflow.

> **Note:** This section should be updated to reflect the exact components personally implemented by each team member.

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone <repository-url>
cd green-logistics-optimizer
```

### 2. Install frontend dependencies

```bash
cd frontend
npm install
```

### 3. Start the frontend

```bash
npm run dev
```

### 4. Start the backend

```bash
cd backend
npm install
npm run dev
```

### 5. Start the ML service

```bash
cd ml-backend

pip install -r requirements.txt

python server.py
```

The ML service runs on port `5001`.

> Update the commands above if your repository uses different folder names, scripts, or environment variables.

---

## 🔌 API

### Optimize Route

```http
POST /optimize-route
```

Example input parameters include:

```json
{
  "vehicle_type": "...",
  "fuel_type": "...",
  "load_weight": "..."
}
```

The optimization service returns route information including optimized waypoints and an optimization summary.

---

## 📊 Project Impact

Green Logistics Optimizer demonstrates how optimization and machine learning can be combined to support more sustainable logistics planning.

The platform brings together:

**Route Optimization + Carbon Analysis + Demand Forecasting**

to provide a unified view of logistics efficiency and environmental impact.

---

## 🔮 Future Improvements

* Multi-objective optimization for cost, time, and emissions
* Real-time traffic integration
* Dynamic route re-optimization
* Real-time fleet tracking
* More advanced demand forecasting models
* Large-scale fleet optimization
* Integration with real-world logistics APIs

---

## 🏆 Hackathon

**Walmart Sparkathon 2025**

Built as a solution focused on improving logistics efficiency while reducing environmental impact.

---

## 👥 Contributors

Built collaboratively as part of Walmart Sparkathon 2025.

Anannaya Agarwal
Ishita Sodhiya
Loheyta Dhanrue
Prisha Birla

---

## 📄 License

This project was developed as a hackathon project.
