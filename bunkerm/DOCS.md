# BunkerM - MQTT Management Platform

BunkerM is an open-source MQTT management platform that bundles a pre-configured
Mosquitto MQTT broker with a comprehensive web-based management interface.

## Features

- Real-time dashboard with connected clients, message statistics, and broker metrics
- Dynamic security controls with ACL configuration
- Client authentication and credential management
- MQTT Explorer for inspecting live broker traffic
- Statistical anomaly detection engine
- Support for MQTT 3.1.1, 5.0, and WebSocket protocols

## Configuration

### Option: `mqtt_username`

Username for the MQTT broker admin account. Default: `bunker`

### Option: `mqtt_password`

Password for the MQTT broker admin account. Default: `bunker`

**Important:** Change the default credentials for production use!

### Option: `log_level`

Log verbosity. One of: `DEBUG`, `INFO`, `WARNING`, `ERROR`. Default: `INFO`

## Ports

| Port | Description |
|------|-------------|
| 1900 | MQTT Broker (connect your IoT devices here) |
| 2000 | Web Management UI (accessible via Ingress sidebar) |

## Access

The Web UI is accessible directly from the Home Assistant sidebar via Ingress.
MQTT clients should connect to port **1900** using the configured credentials.

## Data Persistence

All data (Mosquitto config, broker data, authentication, secrets) is persisted
in the addon's `/data` directory and survives addon restarts and updates.

## Upstream

Based on [BunkerM by BunkerIoT](https://github.com/bunkeriot/BunkerM).
