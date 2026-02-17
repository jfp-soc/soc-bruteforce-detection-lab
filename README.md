# Windows Brute Force Detection Lab

## Overview
This project simulates the detection and investigation of a potential brute force attack using Windows Security Event Logs.

The objective was to analyze failed authentication attempts and determine whether the activity was malicious.

---

## Scenario

A Windows host generated multiple failed login events (Event ID 4625) originating from a single source IP address.

---

## Log Analysis

- Event ID 4625 = Failed logon
- Event ID 4624 = Successful logon
- Logon Type 3 = Network logon

Multiple 4625 events from IP 192.168.1.50 targeted the "administrator" account.

---

## Detection Logic

Alert if:
- Event ID = 4625
- Same Source IP
- Repeated attempts within short timeframe

---

## MITRE ATT&CK Mapping

Technique: T1110 – Brute Force

---

## Skills Demonstrated

- Windows Event Log analysis
- Threat detection methodology
- Basic incident investigation
- Security documentation
