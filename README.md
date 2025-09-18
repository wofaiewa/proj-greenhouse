# Greenhouse Monitoring System (Sub-$1k Build)
## Overview
This is a learning project to master the [Viam robotics platform](https://www.viam.com/) while building a practical automated greenhouse monitoring system. The system combines distributed sensor nodes, a thermal imaging rig, and a DJI Mini 4 Pro drone to detect plant stress, operate offline-first, and coordinate multiple machines.

## System Architecture
- **Drone**: DJI Mini 4 Pro (MSDK v5 supported, autonomous missions)
- **Sensors**: ESP32 nodes with BME680 (temp/RH/VOC) + SCD30 (CO₂) sensors
- **Thermal**: FLIR Lepton 3.5 on ground-based pan-tilt rig
- **Coordinator**: Raspberry Pi 4 (Viam base station, SQLite storage, Flask API)
- **Offline-first**: Pi hosts local Wi-Fi AP, devices sync when cloud is available

## Development Timeline
- **Phase 1**: Sensor network foundation
- **Phase 2**: Data pipeline & thresholds
- **Phase 3**: Drone integration (RGB)
- **Phase 4**: Automation & coordination
- **Phase 5**: Testing, refinement, final demo

## Goals
- Operate with poor/no internet
- Trigger drone missions from sensor data
- Detect thermal anomalies (plant stress, airflow issues)
- Document and share the entire build process

## Repo Structure
- ```/docs → diagrams, design docs, BOM, engineering log```
- ```/firmware → ESP32 MicroPython code```
- ```/pi → Raspberry Pi Flask bridge, DB schemas```
- ```/android → Android MSDK client snippets```
- ```/data → sample logs, exports, test datasets```

## Engineering Log
See `/docs/engineering-log.md` for daily progress.

## Bill of Materials (BOM)
See `/docs/bom.md` for hardware/software tracking.
