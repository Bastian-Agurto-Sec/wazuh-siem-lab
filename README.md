# Wazuh SIEM Lab: Windows Telemetry Monitoring with Sysmon

## Overview

This project demonstrates the implementation of a Security Information and Event Management (SIEM) lab using Wazuh and Sysmon.

The lab collects telemetry from a Windows endpoint and centralizes logs in a Wazuh server, simulating a real SOC (Security Operations Center) environment.

---

## Technologies Used

* Wazuh
* Sysmon
* Filebeat
* OpenSearch
* Ubuntu Server
* Windows 10

---

## Lab Architecture

### Endpoint

* Windows 10
* Sysmon
* Wazuh Agent

### Server

* Ubuntu
* Wazuh Manager
* Wazuh Indexer
* Wazuh Dashboard
* Filebeat

### Data Pipeline

Sysmon
↓
Wazuh Agent
↓
Wazuh Manager
↓
archives.json / alerts.json
↓
Filebeat
↓
Wazuh Indexer
↓
Wazuh Dashboard

---

## Key Features

* Collection of Windows Security logs
* Ingestion of Sysmon telemetry
* Centralized log management
* Event investigation via dashboard
* Access to raw logs via wazuh-archives-*

---

## Project Goals

* Build a functional SIEM lab
* Understand log pipelines
* Practice troubleshooting in security environments
* Simulate real SOC workflows

---

## Status

✅ Fully functional
✅ Sysmon logs ingested
✅ wazuh-archives-* index created
