# 🌿 SmartFence AI — Protect Crops, Save Wildlife

**An AI-powered smart farm protection system for wildlife-aware crop protection.**

🤖 AI Detection • 🌾 Smart Farming • 🗺️ Interactive Map • 💧 Smart Water Deterrence

---

## 📌 Overview

**SmartFence AI** is an intelligent farm protection prototype designed to help farmers monitor agricultural fields and respond to potential wildlife intrusion.

The system combines camera-based animal detection, YOLO object detection, ultrasonic distance sensing, and a controlled water-spray deterrent. An interactive dashboard displays the farm environment, camera locations, detection events, sensor readings, and system status.

The project aims to reduce crop damage while promoting safer, non-harmful coexistence between farmers and wildlife.

## 🎯 Problem Statement

Farmers can experience crop damage when wild animals enter agricultural fields, particularly during nighttime. Continuous manual monitoring is difficult, and conventional deterrents may be expensive, unreliable, or harmful to wildlife.

There is a need for an affordable, intelligent monitoring system that can detect potential intrusions, notify farmers, and support a timely response.

## 💡 Our Solution

SmartFence AI provides a smart monitoring and deterrence workflow:

1. **Camera monitoring:** A compatible camera captures the farm area during the day or at night.
2. **AI animal detection:** A YOLO-based model identifies supported animal classes in the camera feed.
3. **Distance sensing:** An ultrasonic sensor provides distance measurements near a monitored area.
4. **Zone identification:** The dashboard highlights the camera's assigned farm zone on an interactive map.
5. **Smart deterrence:** A controller can activate a low-pressure water spray when configured conditions are met.
6. **Farmer alerts:** A notification service can inform the farmer about a detection event.
7. **Event history:** The dashboard records detections, sensor readings, alerts, and device actions.

> **Note:** The interactive prototype can simulate these stages. Real detection, physical pump activation, map integration, and SMS delivery require the corresponding hardware and services to be configured.

## ✨ Key Features

- **AI Animal Detection:** YOLO-based detection, bounding boxes, confidence scores, timestamps, and camera identification.
- **Interactive 3D Farm:** Animated crop rows, moving animal demonstrations, camera poles, sensor nodes, and glowing farm boundaries.
- **Interactive Satellite Map:** Farm boundaries, zones, device markers, event locations, and map-layer controls where supported.
- **Water-Spray Deterrence:** Pump controls, animated water particles, configurable spray duration, and cooldown.
- **Sensor Monitoring:** Ultrasonic distance readings, thresholds, and device status.
- **Alerts and Event History:** Detection alerts, device warnings, event timestamps, searchable logs, and optional SMS integration.
- **Live Prototype Demo:** A separate demonstration page showing the full workflow from animal approach to event recording.

## 🏗️ System Architecture

\`\`\`text
Camera / Night-Vision Camera
             |
             v
      Python + YOLO
      Animal Detection
             |
             v
       Backend API
       /    |     \\
      /     |      \\
     v      v       v
  Dashboard Map   Event Store
     |             |
     |             v
     |         Alert Service
     |
     v
 ESP32 <---- Ultrasonic Sensor
     |
     v
 Pump Driver / Relay
     |
     v
 Low-Pressure Water Spray
\`\`\`

This is the proposed integration architecture. Only configured and connected components operate as real devices; other components may run in simulation mode.

## 🧰 Technology Stack

| Component | Technology |
|---|---|
| Frontend | React, TypeScript |
| Styling | Tailwind CSS |
| Animations | Framer Motion |
| 3D visualization | Three.js / React Three Fiber |
| Interactive maps | Leaflet |
| Charts | Recharts |
| AI detection | Python, Ultralytics YOLO |
| Backend API | FastAPI (planned/integration-ready) |
| Microcontroller | ESP32 |
| Distance sensor | HC-SR04 or suitable outdoor sensor |
| Camera | Compatible USB/IP camera with IR night vision where needed |
| Deterrent | Mini water pump, nozzle, suitable driver and power supply |
| Notifications | Backend SMS provider integration |
| Data storage | LocalStorage for demo; SQLite/PostgreSQL as deployment options |

*Confirm the actual libraries and integrations used in your repository before publishing.*

## 🎬 Prototype Workflow

1. Start the Live Prototype Demo.
2. Watch the simulated animal move into a selected farm zone.
3. Observe the camera tracking and detection overlay.
4. View the sensor distance change.
5. Watch the relevant farm zone highlight on the map.
6. Activate the simulated water spray or enable the configured demo response.
7. Watch the animal turn away along the simulated route.
8. Review the alert and event history.

The demo should clearly distinguish simulated activity from real sensor readings and live AI inference.

## 🚀 Getting Started

### Prerequisites

- Node.js and npm
- Git
- A code editor such as Visual Studio Code

For real hardware integration, additional requirements may include Python, a compatible camera, an ESP32, sensors, a suitable pump driver, and a configured backend.

### Installation

Clone the repository:

\`\`\`bash
git clone <YOUR_GITHUB_REPOSITORY_URL>
cd <YOUR_PROJECT_FOLDER>
\`\`\`

Install dependencies:

\`\`\`bash
npm install
\`\`\`

Start the development server:

\`\`\`bash
npm run dev
\`\`\`

Open the local URL printed in your terminal.

*These commands assume a Vite-based React project. If your project uses another setup, follow the scripts in package.json.*

## ⚙️ Configuration

For a real deployment, configure the necessary service endpoints and credentials through environment variables or secure backend configuration.

Possible settings include:

- Backend API URL
- YOLO inference service endpoint
- Camera connection settings
- Map tile provider configuration
- ESP32 communication endpoint
- SMS provider credentials
- Detection confidence threshold
- Sensor distance threshold
- Pump duration and cooldown

Never commit API keys, SMS credentials, or camera passwords to a public repository.

Satellite imagery availability depends on the selected provider, its terms, and any required API key or billing setup.

## 🔌 Hardware Requirements

| Component | Purpose |
|---|---|
| Compatible camera | Captures the monitored field |
| IR night-vision camera | Supports compatible nighttime monitoring |
| Laptop or edge computer | Runs YOLO inference |
| ESP32 | Reads sensors and controls connected devices |
| Ultrasonic sensor | Measures distance |
| DC water pump and nozzle | Produces a low-pressure deterrent spray |
| Properly rated driver/relay | Controls the pump safely |
| Suitable power supply | Powers the controller and pump |
| Weather-resistant enclosure | Protects outdoor electronics |
| Optional cellular module | Supports SMS on a compatible network |

Use a suitable pump driver and appropriate electrical protection. Never connect a pump directly to an ESP32 GPIO pin.

## 🛡️ Safety and Responsible Wildlife Protection

- Use a non-harmful, low-pressure deterrent.
- Do not use electric shocks, traps, or harmful chemicals.
- Configure spray duration and cooldown to prevent repeated activation.
- Avoid directing water at an animal's face.
- Protect outdoor wiring and electronics from water and weather.
- Do not claim a detection or notification is real unless the corresponding service confirms it.
- Treat map-based animal movement as simulated unless a genuine tracking system provides location data.

## 🔮 Future Enhancements

- Fine-tune YOLO using a labelled dataset of locally relevant wildlife.
- Improve detection in low-light and difficult weather conditions.
- Integrate multiple real-time camera feeds.
- Add reliable cellular alerts and delivery status.
- Add solar-powered monitoring devices.
- Improve farm-zone configuration and camera coverage estimation.
- Add offline event storage and synchronization.
- Evaluate detection accuracy, false alarms, latency, and deterrent effectiveness through controlled testing.

## 👥 Team

**Team Name:** Ms Square  
**Institution:** Sri Sai Ram Engineering College

## 🌱 Impact

SmartFence AI explores how AI, embedded systems, and interactive mapping can support crop protection while encouraging non-harmful wildlife deterrence.

The prototype demonstrates a possible approach to smarter farm monitoring, timely alerts, and more informed decision-making.

## 📄 License

Choose a license before publishing the repository publicly. For example, the MIT License can be suitable for an open-source project when its terms meet your team's requirements.

---

**SmartFence AI — Protect Crops. Save Wildlife. 🌿**
