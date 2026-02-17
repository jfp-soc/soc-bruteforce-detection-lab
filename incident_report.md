# Incident Report: SSH Brute Force Attempt

## Summary
Multiple failed SSH login attempts were detected from IP address 192.168.1.55.

## Evidence
The auth.log file shows repeated "Failed password" entries from the same source IP.

## Analysis
The IP 192.168.1.55 attempted to authenticate multiple times using the username "admin".

This behavior is consistent with a brute force attack.

## MITRE ATT&CK Mapping
Technique: T1110 - Brute Force

## Recommendation
- Block the attacking IP
- Enforce strong password policy
- Implement account lockout policy
