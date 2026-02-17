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

## Lessons Learned

- Repeated failed authentication attempts are a common brute force indicator.
- Monitoring Event ID 4625 is critical for detecting unauthorized access attempts.
- Proper logging and alert thresholds reduce response time.

- # Windows Brute Force Detection Lab

## Overview
This project simulates the detection and investigation of a potential brute force attack using Linux/SSH authentication logs. 
The goal is to demonstrate log analysis, attack detection, and incident reporting skills.

---

## Scenario
Multiple failed SSH login attempts were detected from an external IP targeting high-value accounts (admin, root). 
A successful login occurred from a separate internal user. The pattern indicates potential automated brute force activity.

---

## Skills Demonstrated
- Log analysis and interpretation
- Detection of suspicious login patterns
- Risk assessment and incident prioritization
- False positive analysis
- MITRE ATT&CK mapping (T1110 – Brute Force)
- Security recommendations and mitigation planning

---

## Evidence
- `auth.log` file showing failed login attempts
- Incident report (`incident_report.md`) documenting investigation, timeline, and reasoning

---

## Outcome
Identified brute force activity with high confidence and recommended mitigations to prevent future attacks.

