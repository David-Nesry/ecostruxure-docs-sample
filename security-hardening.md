{% include nav.md %}

# Security Hardening Guide – EcoStruxure Building Data Platform

## Overview
This guide outlines best practices for securing integrations and data flows within the EcoStruxure Building Data Platform.

## Key Recommendations

- Enforce HTTPS across all endpoints.
- Rotate API keys every 90 days.
- Implement role-based access control (RBAC).
- Validate incoming JSON payloads against schema.
- Monitor system logs for unauthorized access attempts.

## Authentication Best Practices

- Use OAuth 2.0 or JWT for secure token exchange.
- Store credentials securely using environment variables or vaults.
- Avoid hardcoding secrets in source code.

## Data Protection

- Encrypt sensitive data in transit and at rest.
- Use field-level encryption for personally identifiable information (PII).
- Apply schema validation to all incoming data.

## Audit & Monitoring

- Enable audit logging for all API activity.
- Set up alerts for failed authentication attempts.

- Review access logs regularly for anomalies.

