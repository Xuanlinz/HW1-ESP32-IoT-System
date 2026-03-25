# Local Python AIoT Workspace

Welcome to a fully functional **AIoT Sensor Demo Project**.  
This repository provides both:

- 🧪 A **software simulation environment**
- 🔌 A **real hardware deployment (ESP32 + DHT11)**

All components share the same backend and frontend, making the system **modular, scalable, and easy to switch between environments**.

---

## 🌟 Live Demo

👉 **[Live Streamlit Dashboard](https://xuanlinz.github.io/HW1-ESP32-IoT-System/)**

---

## 🏗️ Architecture Overview

### 🔙 Backend API (`app.py`)
- Built with Flask
- `/sensor` endpoint
- Handles HTTP POST JSON data

### 🗄️ Database (`aiotdb.db`)
- SQLite database
- Stores sensor data

### 📊 Frontend (`dashboard.py`)
- Streamlit dashboard
- Displays:
  - KPI metrics
  - Tables
  - Line charts

---

## 🔄 Deployment Modes

### 🧪 Simulation Mode
- No hardware required
- Script: `esp32_sim.py`
- Sends fake data every 5 seconds

### 🔌 Real Hardware Mode
- ESP32 + DHT11
- Script: `esp32_real.cpp`
- Uses WiFi + HTTP POST

---

## 🚀 Run Locally

### 1. Setup
```bash
python -m venv venv
.\venv\Scripts\Activate.ps1
pip install -r requirements.txt
```

### 2. Start Backend
```bash
python app.py
```

### 3. Start Dashboard
```bash
streamlit run dashboard.py
```

### 4. Choose Mode

Simulation:
```bash
python esp32_sim.py
```

Hardware:
- Update WiFi + IP in `esp32_real.cpp`
- Upload to ESP32

---

## 📌 Summary

Sensor → API → Database → Dashboard
