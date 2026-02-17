<img width="1451" height="676" alt="Screenshot 2026-02-17 095758" src="https://github.com/user-attachments/assets/ac65c07a-27dc-465e-9662-eceaf41f7816" />
<img width="1223" height="994" alt="Screenshot 2026-02-17 095749" src="https://github.com/user-attachments/assets/d4c03d62-533d-403a-87de-845e5d4e86bc" />
<img width="1023" height="234" alt="Screenshot 2026-02-17 095722" src="https://github.com/user-attachments/assets/8ed20a52-448e-4a2e-8cb3-ec9c5dce14f3" />
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

---

## Evidence
- `auth.log` file showing failed login attempts
- Incident report (`incident_report.md`) documenting investigation, timeline, and reasoning

---

## Outcome
Identified brute force activity with high confidence and recommended mitigations to prevent future attacks.

---

## Lessons Learned

- Repeated failed authentication attempts are a common brute force indicator.
- Monitoring Event ID 4625 is critical for detecting unauthorized access attempts.
- Proper logging and alert thresholds reduce response time.

---

