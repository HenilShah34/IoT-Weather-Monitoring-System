# IoT Weather Monitoring System

## 📌 Overview
The **IoT Weather Monitoring System** is a real-time embedded system designed to monitor environmental parameters such as **temperature, humidity, and atmospheric pressure**. The system uses low-cost sensors integrated with a microcontroller to collect, process, and display weather data locally on an LCD and optionally transmit it to cloud platforms using IoT principles.

This project was developed as a **solo academic mini project** for the Bachelor of Computer Applications (BCA) program and demonstrates the practical application of **IoT, embedded systems, and sensor interfacing**.

---

## 🎯 Objectives
- Monitor temperature, humidity, and atmospheric pressure in real time  
- Design a cost-effective and portable weather monitoring solution  
- Display sensor data on an LCD screen for local monitoring  
- Demonstrate IoT concepts using embedded hardware and software  
- Provide a scalable base for future enhancements such as cloud integration  

---

## ⚙️ System Features
- Real-time temperature and humidity monitoring using **DHT11**
- Atmospheric pressure measurement using **BMP180**
- Live data display on **16×2 LCD with I2C module**
- Stable sensor readings with calibration and error handling
- Modular and expandable system architecture
- Optional cloud integration for remote monitoring

---

## 🧩 Hardware Components
- Arduino Uno (Microcontroller)  
- DHT11 Temperature & Humidity Sensor  
- BMP180 Atmospheric Pressure Sensor  
- 16×2 LCD Display with I2C Module  
- Breadboard  
- Jumper Wires  
- USB / Battery Power Supply  

---

## 💻 Software & Tools
- Arduino IDE  
- C/C++  
- Libraries:
  - `DHT.h`
  - `Adafruit_BMP085.h`
  - `LiquidCrystal_I2C.h`
- Optional Cloud Platforms:
  - ThingSpeak
  - Firebase
  - Google Sheets

---

## 🏗️ System Architecture
The system follows a **layered architecture**:

1. **Sensing Layer**  
   Sensors (DHT11, BMP180) collect environmental data.

2. **Processing Layer**  
   Arduino processes raw sensor values and converts them into readable data.

3. **Output / Communication Layer**  
   Data is displayed on an LCD and can be transmitted to cloud platforms for remote monitoring.

---

## 🔄 Working Principle
1. Sensors capture environmental parameters.
2. Arduino reads and processes sensor data using predefined libraries.
3. Processed data is displayed on the LCD in real time.
4. (Optional) Data is transmitted to a cloud platform via IoT modules.
5. The system updates readings at regular intervals.

---
## 📷 Project Output

![Breadboard Setup](Images/Breadboard.png)
![LCD Display](Images/LCD_Screen.png)

---

## 🧪 Testing & Results
- System tested in indoor and outdoor environments.
- Sensor readings remained stable and consistent under normal conditions.
- Real-time updates were displayed without noticeable delay.
- Minor fluctuations observed due to environmental changes, which are expected.

---

## ✅ Advantages
- Low-cost and energy-efficient
- Easy to implement and use
- Real-time data monitoring
- Modular and expandable design
- Suitable for academic and real-world applications

---

## ⚠️ Limitations
- Limited sensor accuracy under extreme conditions
- Dependency on Wi-Fi for cloud features
- Limited display capacity on 16×2 LCD
- Arduino Uno not ideal for large-scale data processing

---

## 🚀 Future Enhancements
- Upgrade sensors (DHT22, BMP280) for higher accuracy  
- Integrate long-range communication (LoRa, NB-IoT)  
- Add solar power support  
- Develop a mobile application for monitoring  
- Apply data analytics and machine learning for weather prediction  

---

## 👤 Author
**Henil Shah**  
Data Analyst & Software Developer  
📍 Bhuj, Gujarat, India  

📧 Email: henils885@gmail.com  
🔗 LinkedIn: https://linkedin.com/in/henil-shah-5958b327a  

---

## 📜 License
This project is developed for academic and learning purposes. You are free to use and modify it with proper attribution.
