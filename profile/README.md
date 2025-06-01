# AlProtein Organization Overview

## About AlProtein

**AlProtein** is a biotech startup pioneering sustainable, eco-friendly, vegan, and gluten-free protein powders derived from plant and algae-based sources. We deliver advanced protein production solutions for food & beverage manufacturers, leveraging local organic nutrients for scalable aqua farming and state-of-the-art protein purification. Our approach addresses the environmental, social, and economic challenges of traditional protein production, meeting the nutritional needs of a growing global population. AlProtein is committed to offering sustainable alternative protein sources to build a greener and healthier future.

---

## Table of Contents

- [About AlProtein](#about-alprotein)
- [Organization Technology Stack](#organization-technology-stack)
  - [Comprehensive AIoT System](#comprehensive-aiot-system)
    - [IIoT System Architecture](#iiot-system-architecture)
    - [Monitored Parameters](#monitored-parameters)
    - [Hardware & Firmware](#hardware--firmware)
    - [Cloud & Data Processing](#cloud--data-processing)
    - [Security and Maintenance](#security-and-maintenance)
    - [Testing and Failover](#testing-and-failover)
  - [AI & Data Science Solutions](#ai--data-science-solutions)
  - [Web Data Entry and Dashboards](#web-data-entry-and-dashboards)
- [Repository Overview](#repository-overview)
- [Contact](#contact)

---

## Organization Technology Stack

### Comprehensive AIoT System

AlProtein’s **Comprehensive AIoT System** is designed for full-stack monitoring, control, and optimization of aqua farming environments, integrating edge hardware, cloud platforms, AI models, and data-driven dashboards.

#### IIoT System Architecture

- **Purpose:** Monitor and optimize environmental conditions for sustainable protein culture growth.
- **Key Features:**
  - Real-time data collection from field sensors
  - Automated alerts and preventive actions
  - Remote control of actuators (valves, pumps, fans)
  - Secure, redundant data transmission to the cloud

#### Monitored Parameters

- Humidity (Greenhouses)
- CO₂ Levels (Greenhouses)
- Air & Water Temperature
- Dissolved Oxygen (Spirulina Tanks)
- TDS (Total Dissolved Solids, Spirulina Tanks)
- pH (Tanks)
- Light Intensity (Spirulina Tanks)
- Water Level (Tanks)

#### Hardware & Firmware

- **Sensors:** Industrial-grade for CO₂, temperature, humidity, DO, TDS, pH, light, water level
- **Edge Devices:** ESP32 MCUs, Raspberry Pi 4 Compute, 4G RS485 Data Logger
- **Connectivity:** Wi-Fi, Bluetooth, 4G LTE, RS485/Modbus
- **Power:** 5V/12V/24V with UPS backup
- **Firmware:** 
  - ESP32: C++ (Arduino IDE, PlatformIO)
  - Raspberry Pi: Python (Raspberry Pi OS/Ubuntu; Visual Studio Code, Jupyter Notebooks)
  - Key libraries: Atlas Sensors, OneWire, DallasTemperature, Paho MQTT, AWS SDK (boto3)

#### Cloud & Data Processing

- **Cloud Platform:** AWS IoT Core
- **Data Storage:** AWS DynamoDB
- **Analytics:** Python (pandas, numpy)
- **Dashboards:** AWS QuickSight (real-time and periodic reporting)
- **Alerts:** AWS IoT Events (email/SMS notifications)
- **Protocols:** MQTT, HTTP/REST

#### Security and Maintenance

- **Wi-Fi Encryption:** WPA2
- **MQTT Auth:** Username/Password/Certificates
- **Data Encryption:** TLS/SSL
- **Role-Based Access:** Dashboard RBAC
- **Sensor Calibration:** Every 3 months (pH: every 2 weeks)
- **Firmware Updates:** OTA/USB
- **Backup:** Weekly cloud backup

#### Testing and Failover

- **Testing:** Multi-phase (lab + field) for accuracy, stability, cloud sync, alerting, and power resilience
- **Failover:**
  - Multi-path data routing (4G, Wi-Fi, RS485)
  - Local buffering (SQLite, up to 7 days)
  - UPS-backed power continuity
  - Automated alerting and recovery
  - Self-healing edge device routines

#### Future Developments

- Automated nutrient dispensing
- AI/ML for optimal growth prediction
- Predictive sensor maintenance

---

### AI & Data Science Solutions

AlProtein develops and deploys advanced AI models for operational optimization and quality control:

- **AlgaPredict:** Predicts microalgae concentration from multivariate sensor data.
- **Morphology Detection:** Classifies images as Spirulina or non-Spirulina.
- **Purity Model:** Analyzes Spirulina image purity, detecting contaminants.
- **Sensor Stream:** Forecasts sensor readings for trend prediction and anomaly detection.

---

### Web Data Entry and Dashboards

- **Data Entry Platform:** Streamlit-based web app for numerical and image data entry, fully integrated with the cloud.
- **Dashboards:** AWS QuickSight dashboards for real-time monitoring, periodic reporting, and alert notifications.

---

## Repository Overview

Below is a summary of key repositories in the AlProtein organization:

| Repository              | Description                                                                                  | Main Tech      |
|-------------------------|----------------------------------------------------------------------------------------------|---------------|
| **AlProtein_DataEntry** | Streamlit web app for uploading and managing numerical/image data linked to cloud storage.   | Python        |
| **AWS**                 | Cloud integration scripts, AWS IoT Core, DynamoDB, and QuickSight dashboard automation.      | Python        |
| **IOT**                 | Firmware and edge logic for IIoT system (ESP32, Raspberry Pi, sensor integrations).          | C++, C        |
| **Datasets**            | Storage and management of curated datasets for AI model development.                         | Data/Various  |
| **SageMaker**           | Jupyter Notebooks and pipelines for training and deploying AI/ML models on AWS SageMaker.    | Jupyter NB    |
| **.github**             | Organization-wide GitHub Actions, issue templates, and community health files.               | Meta/Config   |
| **AlgaPredict**         | AI model for predicting microalgae concentration from sensor data.                           | Jupyter NB    |
| **Sensor_Stream**       | Sensor data forecasting models and utilities.                                                | Jupyter NB    |
| **Dynamical_Modelling** | Notebooks and scripts for modeling aquaculture system dynamics and parameter estimation.     | Jupyter NB    |
| **morphology-model**    | Image classification for Spirulina morphology and purity analysis.                           | Python        |

---

## Contact

For more information, partnership, or technical inquiries, please visit our website or contact the AlProtein team.

- **Website:** [www.alprotein.com](https://www.alprotein.com)
- **Email:** info@alprotein.com

---

*AlProtein – Building the next generation of sustainable proteins for a healthier planet.*
## Work Flow

<img src="High-Level Architecture Diagram.png">
