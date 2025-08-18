# CSV Data Import Guide – EcoStruxure Building Data Platform

## Overview
This guide explains how to import building telemetry and configuration data into the EcoStruxure platform using CSV files.

CSV import is ideal for:
- Bulk onboarding of devices or rooms
- Historical data migration
- Offline data preparation

---

## 📁 Supported CSV Formats

### 1. Room Configuration

```csv
room_id,room_name,floor,area_sqft
A101,Conference Room 1,1,350
B202,Office 2,2,180

## Sensor Telemetry

```csv
timestamp,room_id,temperature,humidity
2025-08-18T12:00:00Z,A101,22.5,45
2025-08-18T12:05:00Z,A101,22.6,44

🔧 Import Workflow
- Prepare CSV File
- Ensure headers match schema
- Validate data types and formats
- Upload via Admin Console
- Navigate to Data Import → CSV Upload
- Select file and choose target schema
- Validate & Preview
- System checks for missing fields, duplicates, and format errors
- Preview parsed data before final import
- Import & Monitor
- Confirm import
- Monitor logs for success/failure messages

✅ Best Practices
- Use ISO 8601 format for timestamps (YYYY-MM-DDTHH:MM:SSZ)
- Avoid special characters in headers
- Keep file size under 10MB for optimal performance
- Use UTF-8 encoding

🛡️ Security Notes
- Only authorized users can perform imports
- Uploaded files are scanned for malware
- Audit logs track all import activity

📌 Troubleshooting
| Issue | Solution | 
| "Invalid header format" | Check for typos or extra whitespace | 
| "Timestamp parse error" | Use ISO 8601 format | 
| "Duplicate room ID" | Ensure unique identifiers per row | 


