🏭 Industrial Hub: Integrated IoT & Predictive AI Ecosystem
Author: Raghav Metange

Focus: Autonomous Safety, Predictive Maintenance, and Signal Processing
This repository contains a modular, three-pillar engineering framework designed for a modern "Smart Factory" or "Industrial Hub." The project demonstrates the integration of Computer Science (Machine Learning), Robotics (Control Theory), and IoT (Wireless Signal Processing).

🏗️ System Architecture
The Industrial Hub is built on three independent yet interconnected modules that share a common data pipeline to ensure factory safety and operational uptime.
1. 🛡️ Aegis-Drive: Autonomous Collision Avoidance
Role: The "Reflexes" of the system.
Tech: Physics-based Control Theory, NumPy, Matplotlib.
  i. Problem: aGVs (Automated Guided Vehicles) often suffer from sensor noise and mechanical latency, leading to collisions.
  ii. Solution: Implemented a Predictive Controller that calculates a dynamic stopping threshold and uses an EWMA (Exponentially Weighted Moving Average) filter to clean 100Hz sensor telemetry.
  iii. Outcome: Achieved a stable 0.732m safety margin in high-noise simulations.

🧠 2. ForgeSight: Predictive Maintenance Engine
Role: The "Brain" of the system.
Tech: Scikit-Learn, Pandas, SMOTE, Random Forest.
  i. Problem: Real-world industrial failure data is highly imbalanced (only 3% failure rate), causing standard AI models to miss critical warnings.
  ii. Solution: Used SMOTE to balance the dataset and engineered a custom Power-to-Heat feature ratio.
  iii. Outcome: Created a classification model with 96.04% accuracy that identifies mechanical stress before hardware failure occurs.

📶 3. ProxiLink: BLE Social Interaction Tracker
Role: The "Senses" of the system.
Tech: Signal Processing, Wireless Path-Loss Modeling.
  i.   Problem: Bluetooth RSSI signals are notoriously volatile due to multipath fading and body absorption.
  ii. Solution: Built a Log-Distance Path Loss model to simulate worker proximity and a sliding-window classifier to distinguish between "Close Interaction" and "Safe Proximity."
  iii. Outcome: Accurately detected interaction events with a 23.60s duration, providing the "Personnel Location" data for the Aegis-Drive safety layer.

🔗 The "Industrial Hub" Orchestrator
To demonstrate the full power of this ecosystem, the Hub_Master_Integration.ipynb acts as the system's heart. It creates a Logic Bridge where:
  i. ProxiLink detects a worker entering a danger zone.
  ii. Aegis-Drive receives that wireless trigger and automatically engages "Active Braking."
  iii. ForgeSight audits the braking force to update the machine's "Maintenance Risk" profile in real-time.

🛠️ Tech Stack & Requirements
Environment: Conda (Python 3.10+)
Libraries: pandas, numpy, scikit-learn, matplotlib, seaborn
Hardware Simulations: Digital Logic Counters (555 Timers/74LS series), ESP32/ESP8266 IoT Logic.

