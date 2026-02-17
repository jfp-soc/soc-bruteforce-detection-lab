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

## Timeline of Events
10:21:33 – Failed login attempt – invalid user 'admin' – 192.168.1.55
10:21:35 – Failed login attempt – invalid user 'admin' – 192.168.1.55
10:21:38 – Failed login attempt – invalid user 'admin' – 192.168.1.55
10:22:01 – Failed login attempt – root – 10.0.0.8
10:22:05 – Failed login attempt – root – 10.0.0.8
10:25:10 – Successful login – user1 – 192.168.1.10

The failed login attempts occurred in rapid succession from the same IP, indicating automated behavior rather than user error.

## Risk Assessment
Level: High
Justification:
- Targeted high-value accounts (admin, root)
- Rapid repeated failures
- Source IP from outside the network

## False Positive Considerations
- Legitimate user mistyping password
- Misconfigured script attempting authentication
- Cached credentials retrying

However, the frequency and external IP make this likely malicious.

## Detection Recommendations
- Alert on more than 3 failed login attempts from the same IP in 1 minute
- Monitor privileged accounts closely
- Implement account lockout policy after multiple failed attempts
- Consider geolocation alerts for external IPs

- Upgraded incident report with timeline, risk, false positives, and reasoning


## Analyst Reasoning
While failed logins can be caused by user error, repeated rapid attempts from an external IP significantly increase the likelihood of brute force activity. 
Given the target accounts and timing, this would be treated as a high-confidence incident requiring immediate action.
