# 🔗 Azure IoT Hub Integration Guide

This guide explains how to integrate the EcoStruxure Building Data Platform with **Azure IoT Hub** to enable secure, scalable telemetry ingestion from smart building devices.

---

## 📦 Prerequisites

- Azure subscription with IoT Hub deployed
- Device registered in IoT Hub
- EcoStruxure platform access with integration permissions
- JSON-formatted telemetry payloads

---

## 🛠️ Step-by-Step Integration

### 1. Register Your Device

Use Azure CLI or Portal:

```bash
az iot hub device-identity create --hub-name <your-hub> --device-id <device-name>