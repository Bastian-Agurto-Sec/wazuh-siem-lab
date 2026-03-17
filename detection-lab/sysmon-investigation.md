# Sysmon Event Investigation

## Overview

This section demonstrates how Sysmon events can be used for basic threat analysis.

---

## Test Activity

Executed the following commands on Windows:

* whoami
* notepad.exe
* ipconfig

---

## Observed Events

Event ID 1 (Process Create):

* Image: notepad.exe
* ParentImage: explorer.exe

---

## Key Fields for Analysis

* CommandLine
* Image
* ParentImage
* User
* EventID

---

## Example Investigation

Scenario:

powershell.exe spawns cmd.exe

This may indicate:

* Script execution
* Potential malicious activity

---

## Detection Value

Sysmon provides:

* Process visibility
* Parent-child relationships
* Execution context

---

## Conclusion

Sysmon significantly enhances visibility and detection capability in a SIEM environment.
