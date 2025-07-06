# 💧 IoT IV Bag Monitoring System

An Internet of Things (IoT)–based smart healthcare project designed to **monitor the fluid level in IV bags** in real time using **ESP8266**, **Load Cell**, **HX711**, and the **Blynk app**. The system helps prevent fluid overflow or empty IV bags by sending alerts to caregivers through mobile notifications.

---

## 🔧 Technologies & Components Used

- **ESP8266 NodeMCU** – Wi-Fi microcontroller
- **Load Cell** – for weight sensing
- **HX711 Amplifier** – signal amplification for Load Cell
- **PCF8574 I/O Expander** 
- **Blynk App** – real-time data visualization & alerts
- **Arduino IDE** – code development 

---

## ⚙️ Features

- 📶 Real-time fluid level tracking via Blynk
- 🔔 Instant notifications for low fluid levels
- 🧠 Lightweight & scalable for hospitals or home care

---

## 🛠️ Circuit Diagram

> 🔽 **Download/View Diagram**  
> ![Circuit Diagram](![hardware_design](https://github.com/user-attachments/assets/63c13995-4453-4198-816c-f7edde0fa7f6)
)  
> 

## 🚀 Getting Started

### ✅ Hardware Setup
1. Connect the Load Cell to HX711 module.
2. Connect HX711 to NodeMCU using GPIO (e.g., D2 & D3).
3. Power the circuit using USB or external source.
4. Upload code from Arduino IDE (include Blynk Auth Token).

### ✅ Software Setup
- Libraries needed:
  - `HX711.h`
  - `BlynkSimpleEsp8266.h`
  - `ESP8266WiFi.h`
- Create a project in **Blynk** and get the Auth Token.

---

## 📲 Blynk Dashboard

- **Value Display** for weight monitoring
- **Notification Widget** for alerts
- **Auth Token** pasted into Arduino code

---

## 🌱 Future Improvements

- Automatic IV flow control
- Local alert system with buzzer
- OLED display integration
- Integration with hospital data platforms

---

## 👨‍💻 Developed By

**[Arya Sasikumar]**  
Final-Year Electronics and Communication Engineering Student (ECE ‘26)  
Interested in **IoT, Python, Embedded Systems, and Real-Time Smart Devices**

📫 [www.linkedin.com/in/arya-sasikumar]

---

## ⚠️ License

This project is shared **without any license**.  
Use it for educational purposes or personal learning only.  
