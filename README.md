<h1 align="center">🌡️ IoT Weather Monitoring System</h1>

<p align="center">
  <b>A real-time embedded system that senses, processes, and displays environmental data locally —</b><br/>
  built as a foundation for scaling into edge-computing and cloud-connected IoT architectures.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Arduino-00979D?style=for-the-badge&logo=arduino&logoColor=white"/>
  <img src="https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white"/>
  <img src="https://img.shields.io/badge/IoT-0078D4?style=for-the-badge&logo=internetofthings&logoColor=white"/>
</p>

---

## 📌 Overview

The **IoT Weather Monitoring System** is a real-time embedded system that captures environmental parameters — **temperature, humidity, and atmospheric pressure** — using low-cost sensors interfaced with a microcontroller, processes the readings locally, and displays them on an LCD in real time.

While built as a solo academic project for my BCA program, it's designed around the same layered sensing → processing → output architecture used in production IoT deployments. The current implementation processes and displays data locally (a lightweight form of **edge computing** — handling data at the source rather than shipping every raw reading to the cloud), with the architecture structured so that adding **MQTT-based messaging** for cloud/broker communication is a natural next layer rather than a redesign. That distinction — processing at the edge vs. transmitting everything — is deliberate: it keeps the system responsive and functional even without a network connection, which mirrors how real-world IoT sensor networks are designed to degrade gracefully.

---

## 🎯 Objectives

- Monitor temperature, humidity, and atmospheric pressure in real time
- Design a cost-effective, portable weather monitoring solution
- Process sensor data locally at the edge before any optional cloud transmission
- Display live readings on an LCD for immediate on-site monitoring
- Provide a scalable base for future enhancements such as MQTT-based cloud integration

---

## ⚙️ System Features

- Real-time temperature and humidity monitoring using **DHT11**
- Atmospheric pressure measurement using **BMP180**
- Live data display on a **16×2 LCD with I2C module**
- Stable sensor readings with calibration and error handling
- Modular, expandable architecture designed for edge-first processing
- Optional cloud integration pathway for remote monitoring

---

## 🧩 Hardware Components

| Component | Role |
|---|---|
| 🧠 Arduino Uno | Microcontroller — reads and processes sensor data |
| 🌡️ DHT11 Sensor | Temperature & humidity measurement |
| 🌬️ BMP180 Sensor | Atmospheric pressure measurement |
| 📟 16×2 LCD + I2C Module | Local real-time data display |
| 🔌 Breadboard | Circuit prototyping |
| 🔗 Jumper Wires | Component interconnects |
| 🔋 USB / Battery Supply | Power source |

---

## 💻 Software & Tools

**Environment:** Arduino IDE · C/C++

**Libraries:**
- `DHT.h`
- `Adafruit_BMP085.h`
- `LiquidCrystal_I2C.h`

**Optional Cloud/Edge Extensions:**
- ThingSpeak
- Firebase
- Google Sheets
- MQTT broker (e.g., Mosquitto) — for scalable, low-bandwidth sensor-to-cloud messaging

---

## 🏗️ System Architecture

```mermaid
flowchart TD
    subgraph Sensing Layer
        A1[DHT11<br/>Temperature & Humidity]
        A2[BMP180<br/>Atmospheric Pressure]
    end

    subgraph Processing Layer
        B[Arduino Uno<br/>Reads & Processes Sensor Data]
    end

    subgraph Output / Communication Layer
        C[16x2 LCD Display<br/>Local Real-Time Output]
        D[Optional MQTT / Cloud Platform<br/>ThingSpeak · Firebase · Google Sheets]
    end

    A1 --> B
    A2 --> B
    B --> C
    B -.optional.-> D
