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

## Bash

az iot hub device-identity create --hub-name <your-hub> --device-id <device-name>

### 1. Configure Device Twin
Set desired properties for telemetry routing:
# Json
{
  "desired": {
    "telemetryUploadEnabled": true,
    "uploadInterval": "30s"
  }
}

### 3. Connect via MQTT or AMQP
EcoStruxure supports MQTT over TLS:
# Bash
mqtt://<iot-hub-hostname>:8883

4. Format Payloads
Send telemetry in JSON format:
# json
{
  "temperature": 22.5,
  "humidity": 45,
  "timestamp": "2025-08-20T14:00:00Z"
}

### 5. Monitor Events
Use Azure Event Hub or Stream Analytics to route data to dashboards or storage.

## 🔐 Security Notes
• 	Use X.509 certificates or SAS tokens
• 	Rotate credentials periodically
• 	Validate payload schema before ingestion

## 📚 Resources

- [Azure IoT Hub Documentation](https://learn.microsoft.com/en-us/azure/iot-hub/)  
  Official Microsoft documentation for setting up, managing, and integrating with Azure IoT Hub.

- [Azure Device Provisioning Service](https://learn.microsoft.com/en-us/azure/iot-dps/)  
  Learn how to automate device provisioning at scale using DPS with IoT Hub.

- [EcoStruxure Integration Patterns](https://david-nesry.github.io/ecostruxure-docs-sample/)  
  Sample documentation site showcasing integration guides and developer resources for EcoStruxure Building Data Platform.

