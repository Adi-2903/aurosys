# 🛡️ AuroSys Enterprise (v9.5)

<div align="center">
  <h3>Next-Generation Cyber-Physical Decision Intelligence for Automotive OEMs</h3>
  <p>Bridging the gap between Edge Telematics and Cloud Intelligence using Agentic AI.</p>
</div>

---

## 📖 Project Overview
AuroSys is a **production-oriented cyber-physical AI system** designed to help automotive OEMs move from reactive diagnostics to autonomous, cost-aware decision-making. Unlike traditional vehicle dashboards that stop at fault detection, AuroSys reasons across edge signals, cloud intelligence, logistics, and finance to recommend business-ready actions — such as recalls, OTA updates, or targeted inspections — within a **4-second decision loop**.

## 🚀 Problem Statement
Modern vehicles generate terabytes of data, yet the industry faces several critical bottlenecks:
1. **Mechanics** lack context-aware tools to diagnose complex, multi-layered issues.
2. **OEMs** struggle to correlate individual vehicle faults with broader supply chain defects, leading to expensive, untargeted global recalls.
3. **Drivers** receive cryptic error codes (e.g., Check Engine Light) instead of actionable, clear advice regarding safety and repair costs.

## 💡 Solution
AuroSys is a **Hybrid Agentic Architecture** that transforms "Rule-Based Alerts" into **"Agentic Reasoning"**. It combines:
* **Edge AI (In-Car)**: Processes high-fidelity sensor streams locally for real-time safety alerts, ensuring a privacy-first approach.
* **Cloud AI (OEM)**: Performs Root Cause Analysis (RCA), Supply Chain integration, and Predictive Maintenance.
* **Security AI (Watchdog)**: Monitors for financial fraud (UEBA) and policy violations in real-time.
* **Human-Centric UI**: Provides a 3D Digital Twin for engineers and a Companion App for drivers.

## ✨ Key Features
*   **🎧 NVH Forensics (Signal Core)**: 3D Waterfall Spectrograms and real-time metric calculations (Kurtosis, Crest Factor) to fingerprint fault signatures like a 2x Order resonance.
*   **💬 "Ask the Car" (RAG Chatbot)**: Context-aware GenAI chatbot that knows the current vehicle state and can estimate financial costs in real-time.
*   **📱 Driver Companion App Simulator**: A modern, dark-mode Glassmorphism mobile interface with real-time sync and emergency SOS protocols.
*   **📈 Advanced Vehicle Dynamics**: "Driver DNA Radar" scoring efficiency and aggression, Engine Load Matrix, and real-time Pro Gauges.
*   **🧠 Strategic Decision Intelligence (The "Executive Loop")**: Translates technical codes into business realities (Targeted Recall vs. Firmware OTA vs. Physical Inspection).
*   **🛡️ Security Watchdog (UEBA)**: Fails-closed logic that flags abnormal repair estimates or out-of-hours service bookings.

## 🏗️ System Architecture 
![AuroSys Architecture](architecture.png)

## 🤖 AI Pipeline / Workflow
AuroSys operates on a rapid **4-second decision loop** ("A Day in the Life of a Fault"):
1. **0.0s (The Event)**: A vibration pattern is detected by the **Telematics Agent** (400Hz).
2. **0.1s (Edge Inference)**: The **Diagnosis Agent** analyzes the waveform locally. 
3. **0.5s (Bandwidth Optimization)**: **Comms Module** packages a concise 1.5MB Blackbox Dump to the cloud.
4. **1.2s (Cloud Forensics)**: **RCA Agent** queries the DB and matches the batch defect.
5. **2.0s (Supply Chain)**: **Inventory Agent** scans regional warehouses for parts.
6. **2.5s (Costing)**: **Financial Agent** calculates total bill (Parts + Labor).
7. **3.0s (Logistics)**: **Scheduling Agent** reserves a service bay.
8. **3.5s (User Loop)**: **Driver App** alerts the driver with repair and booking details.

**The Swarm (12 Specialized Agents)**
AuroSys is powered by 12 autonomous agents: 
- **Edge**: Telematics, Driver Behavior, Diagnosis, Comms Module.
- **Cloud**: RCA, Inventory, Battery Health, Financial, Compliance, OTA, Scheduling.
- **Core**: Master Agent (Orchestrator).

## 🧩 Technical Challenges & Solutions
*   **Challenge:** Processing high-fidelity 400Hz telematics data in real-time without overwhelming network bandwidth.
    *   **Solution:** Implementing edge-based inference (Diagnosis Agent) that only transmits a concise 1.5MB "Blackbox Dump" during critical anomalies, rather than streaming raw data continuously.
*   **Challenge:** Orchestrating multiple asynchronous AI agents across edge and cloud layers to reach a consensus within seconds.
    *   **Solution:** Utilizing a Master Agent to synchronize the edge-cloud handshake and manage the state deterministically (`core.py`), ensuring a strict 4-second decision loop.
*   **Challenge:** Translating complex mechanical faults into actionable business and financial metrics.
    *   **Solution:** Building a decoupled Hybrid Decision Engine where pure deterministic logic maps faults, and a presentation layer generates targeted financial impact models.

## 🛠️ Tech Stack
*   **Language**: Python 3.10+
*   **App Framework**: Streamlit (Modular Architecture)
*   **AI/LLM**: Google Gemini 2.0 Flash (via `google-genai`)
*   **Data Visualization**: Plotly (3D Surface Plots, Scatter 3D)
*   **Database**: SQLite (Robust local logging)
*   **Design**: Material Design / Glassmorphism CSS

## 📸 Screenshots / Demo
### The Engineering Console
*A unified view for fleet managers to monitor vehicle health and agent reasoning logs.*
*(Refer to the live demo for the latest interactive console)*

### Intelligent Diagnostics & Dynamics
*View the "Driver DNA" and real-time engine health gauges alongside the agent decision trace.*

## 🏆 Results & Recognition
*   **EY Hackathon Submission**: Showcased as a pioneering solution for bridging Edge Telematics and Cloud Intelligence using Agentic AI.
*   **Business Impact**: 
    *   **OEMs**: Reduces Warranty Fraud & Recall Costs by pinpointing targeted batch recalls (e.g., isolating Batch-2023-A saves massive costs compared to a global recall).
    *   **Supply Chain**: Enables Just-In-Time (JIT) inventory management.
    *   **Drivers**: Increases safety and provides transparent repair costs without "Mechanic Shock".

## 📚 Lessons Learned
*   **Deterministic Logic vs. GenAI**: While GenAI is excellent for RCA forensics and natural language context ("Ask the Car"), relying on strict deterministic logic for core business rules (e.g., recall criteria, security blocks) is essential for production reliability.
*   **Edge-Cloud Symbiosis**: Keeping heavy computation at the edge drastically reduces cloud latency and costs, making instantaneous autonomous decisions viable.
*   **UI Responsiveness**: Complex 3D visualizations (Plotly) need to be carefully optimized to run smoothly within a real-time Streamlit dashboard environment.

## 🔮 Future Roadmap
- [ ] **V2X Communication**: Vehicle-to-Everything for traffic optimization.
- [ ] **AR Maintenance**: Augmented Reality overlays for mechanics.
- [ ] **Blockchain Ledger**: Immutable service history.

## 🌐 GitHub + Live Demo

*   **Live Interactive Demo (No Installation Required)**: [https://aurosys.streamlit.app/](https://aurosys.streamlit.app/)
*   **GitHub Repository**: [Your Repo Link Here]

---
> **Built with ❤️ for the EY Hackathon**
