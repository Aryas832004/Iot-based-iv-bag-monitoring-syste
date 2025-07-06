# Iot-based-iv-bag-monitoring-syste
Real-time monitoring of medicines inside intravenous fluid bag 
# 💧 IoT IV Bag Monitoring System

An Internet of Things (IoT)–based smart healthcare project designed to **monitor the fluid level in IV bags** in real time using **ESP8266**, **Load Cell**, **HX711**, and the **Blynk app**. The system aims to prevent IV fluid overflow or empty bag situations by sending timely alerts to caregivers or nurses.

---

## 🔧 Technologies & Components Used

- **ESP8266 NodeMCU** – for Wi-Fi connectivity and microcontroller logic
- **Load Cell** – to measure the weight of the IV fluid
- **HX711 Amplifier** – to amplify the signal from the Load Cell
- **PCF8574 I/O Expander** – (if used for extending pins)
- **Blynk App** – for real-time monitoring and mobile notifications
- **Arduino IDE** – for programming the ESP8266 (C/C++)

---

## ⚙️ Features

- 📶 Real-time fluid level updates via Blynk app  
- 🔔 Sends alerts when IV bag is nearly empty  
- 🔋 Low power consumption  
- 🧠 Simple, scalable design for hospitals or home care

---

## 🚀 Getting Started

### Hardware Setup
1. Connect the **Load Cell** to the **HX711 amplifier**.
2. Connect HX711 to **ESP8266** using `D2` and `D3` (or your preferred pins).
3. Use Blynk mobile app to create a new project and get your **Auth Token**.
4. Power up the NodeMCU and upload the Arduino sketch.

### Software Setup
- Install the following libraries in Arduino IDE:
  - `HX711`
  - `Blynk`
  - `ESP8266WiFi`

---

## 🔌 Circuit Diagram

*You can add a Fritzing diagram or an image here for clarity.*

---

## 📲 Blynk Dashboard
- Value Display widget for weight
- Notification widget for alerts
- Auth Token pasted into code

---

## 🧠 Future Improvements
- Add automatic IV flow control
- Integrate with hospital management system
- Add local display (OLED or LCD)

---

## 👨‍💻 Developed By

**[Your Name]**  
Final-Year Electronics and Communication Engineering Student (Graduating 2026)  
Passionate about **IoT, Python, and Embedded Systems**  
📫 [Add your email or LinkedIn link here]

---

## 📌 License

This project is open-source and free to use under the [MIT License](LICENSE).


---

✅ Next Step:

You can copy this into a file called README.md in your project folder. Then run:

git add README.md
git commit -m "Added professional README"
git push
