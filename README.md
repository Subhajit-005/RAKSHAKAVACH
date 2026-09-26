# 🛡️ RAKSHAKAVACH

### IoT-Based Disaster Monitoring & Early Warning System

RAKSHAKAVACH is an IoT-based disaster monitoring and early warning
system designed to detect and monitor potential flood, fire, and
gas/smoke hazards in real time.

The system combines an ESP32-C6 based sensor node with a web-based
monitoring dashboard to collect sensor data, evaluate risk levels,
and provide real-time alerts.

---

## 📌 Overview

Natural disasters and environmental hazards can develop rapidly,
making early detection essential for reducing damage and improving
safety.

RAKSHAKAVACH continuously monitors environmental conditions using
multiple sensors connected to an ESP32-C6. The collected data is
transmitted through Wi-Fi to a Node.js backend, stored in SQLite,
and visualized through a React-based dashboard.

The system provides a centralized interface for monitoring sensor
values and identifying different levels of disaster risk.

---

## ✨ Key Features

- 🌊 Real-time flood level monitoring
- 🔥 Fire and flame detection
- 🌡️ Temperature and humidity monitoring
- 💨 Gas and smoke detection
- ⚠️ Risk-level classification
- 📊 Real-time web dashboard
- 🚨 Disaster alerts and status monitoring
- 📡 Wi-Fi-based ESP32 communication
- 🗄️ Sensor data storage using SQLite
- 🔄 REST API-based communication

---

## 🏗️ System Architecture

```text
                    ┌─────────────────────┐
                    │      Sensors        │
                    │                     │
                    │  HW-038 Water Level │
                    │  MQ-2 Gas/Smoke     │
                    │  DHT22              │
                    │  IR Flame Sensor    │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │      ESP32-C6        │
                    │ Sensor Processing &  │
                    │ Wi-Fi Communication  │
                    └──────────┬──────────┘
                               │
                             Wi-Fi
                               │
                               ▼
                    ┌─────────────────────┐
                    │   Node.js + Express │
                    │      REST API       │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │       SQLite        │
                    │   Sensor History    │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │   React + Vite      │
                    │ Monitoring Dashboard│
                    └─────────────────────┘
