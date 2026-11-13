# Weather Reports Automation via Integrations in ServiceNow

Automated weather data collection, threshold-based email alerting, and analytical monitoring dashboard built on ServiceNow using REST API Integrations, Flow Designer, and Platform Analytics.

## Project Overview

- **Domain:** Sustainability & Green Tech
- **Platform:** ServiceNow Personal Developer Instance (`dev407431`)
- **Application Scope:** `Weather Reports Automation`

## Key Features

1. **Automated Weather Data Ingestion**
   - Integrates with the OpenWeatherMap REST API via ServiceNow Outbound REST Messages.
   - Periodically retrieves weather metrics (temperature, humidity, weather condition, and location data for Tangerang) and stores them as structured records.

2. **Custom Data Model and Access Control**
   - Custom table `u_weather_report` (`Weather Report`) designed to store normalized API payloads.
   - Dedicated role-based access control configured through the `u_weather_report_user` role.

3. **Extreme Weather Alerting and Error Logging**
   - `Extreme Weather Alert Flow` developed in Flow Designer to evaluate incoming weather records.
   - Automatically dispatches email notifications when temperature readings exceed 32°C and logs execution errors for system monitoring.

4. **Platform Analytics Monitoring Dashboard**
   - `Weather Reports Monitoring Dashboard` featuring the `Weather Condition Distribution` visualization to track recorded weather patterns.

## Repository Structure

```text
├── now.config.json          # ServiceNow Fluent application scope configuration
├── package.json             # Project dependencies and build scripts
└── src/                     # Application metadata, UI components, and Fluent definitions
