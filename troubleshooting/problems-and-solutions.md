# Troubleshooting

## Issue 1: Sysmon logs not received

Cause:
Sysmon event channel not configured in agent.

Solution:
Added Sysmon configuration block in ossec.conf.

---

## Issue 2: wazuh-archives-* index not appearing

Cause:
Filebeat archives ingestion disabled.

Solution:
Enabled archives in filebeat.yml.

---

## Issue 3: Unauthorized error in curl

Cause:
Wazuh Indexer requires authentication.

Solution:
Used dashboard Dev Tools instead of curl.

---

## Issue 4: Dashboard error "Failed to fetch"

Cause:
Session expiration or temporary backend issue.

Solution:
Restarted Wazuh dashboard service.

---

## Issue 5: SSH session closed unexpectedly

Cause:
Possible VM resource issue or service restart.

Solution:
Reconnected via SSH. System remained stable.

---

## Lessons Learned

* Log pipelines require end-to-end validation
* Misconfigurations often occur at ingestion points
* SIEM systems depend on multiple components working together
