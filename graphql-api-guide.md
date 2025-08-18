---
title: GraphQL API
nav_order: 2
---

# GraphQL API Guide – EcoStruxure Building Data Platform

## Overview
The GraphQL API allows clients to query building telemetry data with precision and flexibility.

## Sample Query: Room Temperature

```graphql
query {
  room(id: "A101") {
    temperature {
      value
      unit
      timestamp
    }
  }
}

## Sample Response

```json
{
  "data": {
    "room": {
      "temperature": {
        "value": 22.5,
        "unit": "Celsius",
        "timestamp": "2025-08-18T12:00:00Z"
      }
    }
  }
}


## Security Notes

- Use JWT tokens for authentication.
- Limit query depth to prevent abuse.

- Monitor query performance and caching.

