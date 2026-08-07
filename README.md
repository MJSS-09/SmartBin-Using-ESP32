# 🗑️ SmartBin — IoT-Based Automatic Lid Dustbin using ESP32 and Blynk

SmartBin is an IoT-enabled waste bin that automatically opens its lid when an object or hand approaches it, and reports live status to a mobile/web dashboard in real time. An ultrasonic sensor detects proximity, a servo motor actuates the lid, and an ESP32 microcontroller runs the logic and pushes data to the cloud through the Blynk IoT platform.

## 👁️Overview

Smart Lid → ESP32 Control Unit → Blynk Monitoring

The goal was a low-cost, contactless, internet-connected dustbin that removes the need to touch the lid, while letting the user remotely monitor lid status and distance readings from anywhere via the Blynk dashboard.

## 💫Key Features 

- Contactless, automatic lid opening using ultrasonic proximity sensing
- Real-time distance visualization on a Blynk Gauge widget
- Real-time lid status (OPEN / CLOSED) on a Blynk Label widget
- Wi-Fi connectivity via the ESP32's built-in module — no extra networking hardware
- Cloud dashboard accessible from anywhere, on mobile or web
- Simple, low-cost hardware — no display module required on the device itself

## ⚙️Hardware Used

- ESP32 Development Board (Wi-Fi + Bluetooth microcontroller)
- HC-SR04 Ultrasonic Distance Sensor
- SG90 Micro Servo Motor (lid actuator)
- Jumper wires and breadboard
- USB cable for power and programming
- Bin enclosure / prototype housing

## 🖥️Software and Platforms

- Arduino IDE — firmware development and flashing
- Blynk IoT platform (Blynk Console) — cloud dashboard for visualization and monitoring
- ESP32 Arduino core, plus Blynk and ESP32Servo libraries

## 🔗Pin Connections 

| Component            | Pin / Signal | ESP32 GPIO |
|-----------------------|--------------|------------|
| HC-SR04 Ultrasonic     | TRIG         | GPIO 5     |
| HC-SR04 Ultrasonic     | ECHO         | GPIO 18    |
| SG90 Servo             | Signal       | GPIO 13    |


## 💪How It Works 

1. The HC-SR04 continuously measures distance in front of the bin.
2. When an object/hand comes within range, the ESP32 triggers the SG90 servo to open the lid.
3. Distance and lid status are pushed to the Blynk Cloud over Wi-Fi.
4. The Blynk dashboard updates a live Gauge (distance) and Label (lid status) in real time.

## 📄Documentation

Full project report (architecture, wiring diagrams, code walkthrough): see `SmartBin.docx` in this repo.

## ✍🏼Author

M. Jayantha Siva Srinivas | B.Tech (ECE), Seshadri Rao Gudlavalleru Engineering College

Contributors: P. Joshi, P.M. Shoaib Khan, Sk. Imran, G. Jayaraju,G. IndraNag





