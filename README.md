

# Suspicious Login Detection Workflow for n8n

Monitor login activity in real time and detect suspicious logins using a single n8n workflow. This solution enriches login events with IP reputation, geolocation, and device/browser data, prioritizes threats, and sends alerts via Slack and email.

## Features

* Real-time login monitoring (webhook & manual triggers)
* IP reputation analysis via **GreyNoise**
* Geolocation enrichment using **IP-API**
* Device & browser anomaly detection with **UserParser**
* Consolidated data for accurate threat assessment
* Automated notifications to users and security teams

## Setup

1. Import the workflow into n8n.
2. Configure API keys for GreyNoise and UserParser.
3. Set up Slack and Gmail credentials for alerts.
4. Connect your Postgres database for user info.


 ## How It Works

Trigger: Workflow starts on a new login event (webhook) or manual execution.

Data Extraction: Login info (IP, user agent, user ID) is captured.

Analysis:

GreyNoise → IP reputation & priority

IP-API → Geolocation

UserParser → Device & browser info

Data Merge: Consolidates all information into a complete login profile.

Anomaly Detection: Checks for new devices, browsers, or locations.

User & Team Alerts:

Email sent to user for suspicious activity

Slack alert sent to security team with priority and details

