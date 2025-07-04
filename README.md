# ☁️ Fog-Prevention Sensor System (ESP32-Based)

**📅 Interim Progress Report — July 4, 2025**  
A smart embedded system to prevent sensor fogging in cold environments using ESP32, temperature & humidity sensors, MQTT, and remote data monitoring.

---

## 📌 Project Objective

This project aims to develop an embedded prototype system that:

- Continuously monitors **temperature** and **humidity** inside cold rooms or insulated boxes  
- Transmits sensor data in real time via **Wi-Fi / MQTT / Node-RED**  
- Automatically controls **heating or cooling actuators** (e.g., heater, Peltier module) to prevent fog formation  
- Calculates **dew point (Td)** and triggers actions when fog risk is detected

---

## 📆 Work Packages & Deliverables

| No | Work Package | Duration | Schedule | Deliverables / Success Criteria |
|----|--------------|----------|----------|----------------------------------|
| 1 | **ESP32 Installation & initial testing** | 2 week | Jul 7–20, 2025 | - Board definitions loaded in Arduino IDE<br>- “Blink”/Wi‑Fi scan demo runs<br>- Serial/USB connection verified |
| 2 | **ESP32 + SHT4X Setup Monitoring** | 1 week | Jul 20–27, 2025 | - SHT4x library integrated<br>- Continuous T & RH readings logged<br>- Basic accuracy check vs reference meter |
| 3 | **Combined Temperature & Humidity Operation** | 1 week | Jul 27–3, 2025 | - Integrated I²C/OneWire communication<br>- Dew point calculation logic<br>- Exportable CSV logging |
| 4 | **MQTT vs Wi-Fi vs Node-RED Research** | 2 days | Sep 3–5, 2025 | - Comparative documentation (pros/cons)<br>- Demo: MQTT Explorer & Node-RED dashboard |
| 5 | **Communication Architecture Decision** | 1 week | Sep 5–10, 2025 | - Final selection (e.g., Wi-Fi + MQTT)<br>- Security structure proposal<br>- Broker connectivity test |
| 6 | **Final System Assembly & Field Testing** | 1 week | Sep 10–17, 2025 | - Physical prototype assembly<br>- 48-hour continuous data logging<br>- Draft version of fog-prevention algorithm<br>- Slideshow for next development phase |

---

## ⚠️ Key Risks & Mitigation Plans

| Topic | Risk | Mitigation |
|-------|------|------------|
| **Sensor Calibration** | ±1 °C or ±3 %RH deviations possible | Use reference-grade thermometer/hygrometer for validation |
| **Power Budget** | Heater + Peltier might exceed ESP32 supply | Use 12V/6A power supply + separate buck converter |
| **MQTT Security** | Company firewall may block unencrypted connections | Use TLS 1.3 + login credentials + secure VLAN |
| **Data Loss** | Possible Wi-Fi disconnection | Add SD card logging as a backup (planned in WP6) |

---

## 🔭 Planned Next Steps

- Implement **PID-controlled environment regulation** (for heater and Peltier)
- Define **fog-risk thresholds** and send real-time alerts via Node-RED (email/SMS)
- Test **anti-fog coating** and **insulated casing designs**
- Run **1-week-long field tests** to evaluate energy use and control performance

---



