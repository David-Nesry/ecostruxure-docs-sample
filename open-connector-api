{% include nav.md %}

# Open Connector Framework – REST API Guide

## Overview
The Open Connector Framework enables integration between EcoStruxure Building Operation and third-party systems using RESTful APIs.

## Authentication

```http
POST /auth/token
Content-Type: application/json

{
  "client_id": "your-client-id",
  "client_secret": "your-client-secret"
}

## Get Connector Status

```http
GET /api/v1/connectors/{connectorId}/status
Authorization: Bearer {access_token}

```json
{
  "connectorId": "modbus-01",
  "status": "active",
  "lastHeartbeat": "2025-08-18T12:00:00Z"
}

## Register New Connector

```http
POST /api/v1/connectors
Content-Type: application/json

{
  "name": "Modbus Connector",
  "type": "modbus",
  "config": {
    "ip": "192.168.1.100",
    "port": 502
  }
}

## Security Guidelines
- Validate connector configurations before deployment.
- Use encrypted channels for connector communication.
- Monitor heartbeat and status endpoints for anomalies.

## Changelog
| Version | Date | Changes | 
| 1.0 | 2025-08-01 | Initial release | 

| 1.1 | 2025-08-18 | Added heartbeat monitoring | 
