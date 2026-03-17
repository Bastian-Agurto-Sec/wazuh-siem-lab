# Wazuh Agent Configuration (Windows)

## Overview

The Wazuh agent collects logs from the Windows endpoint and sends them to the Wazuh Manager.

---

## Sysmon Integration Issue

Sysmon logs were not being ingested initially.

---

## Root Cause

The Sysmon event channel was not included in the agent configuration.

---

## Solution

Added the following block to ossec.conf:

<localfile>
  <location>Microsoft-Windows-Sysmon/Operational</location>
  <log_format>eventchannel</log_format>
</localfile>

---

## File Location

C:\Program Files (x86)\ossec-agent\ossec.conf

---

## Restart Service

Restart-Service WazuhSvc

---

## Verification

Used PowerShell:

Get-WinEvent -LogName "Microsoft-Windows-Sysmon/Operational" -MaxEvents 5

---

## Result

* Sysmon events successfully ingested
* Process creation and file creation events visible
