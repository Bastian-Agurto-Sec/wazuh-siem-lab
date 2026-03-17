# Filebeat Configuration

## Overview

Filebeat is responsible for shipping logs from the Wazuh Manager to the Wazuh Indexer.

---

## Problem Identified

Initially, raw logs were not appearing in the dashboard.

The wazuh-archives-* index was not created.

---

## Root Cause

The Filebeat configuration had archives ingestion disabled:

archives:
enabled: false

---

## Solution

The configuration was modified to enable archives ingestion:

archives:
enabled: true

---

## File Location

/etc/filebeat/filebeat.yml

---

## Service Restart

sudo systemctl restart filebeat

---

## Result

* archives.json logs were successfully ingested
* wazuh-archives-* index was created
* Raw logs became visible in the dashboard
