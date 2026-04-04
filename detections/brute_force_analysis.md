# Brute Force Attack Detection

## Description
This detection identifies multiple failed login attempts from a single source IP.

## Log Source
- Windows Security Logs
- Event ID: 4625 (Failed Login)

## Detection Logic
If multiple failed login attempts occur from the same IP within a short time, it may indicate a brute-force attack.

## Analysis
In this lab, repeated failed login attempts were observed from the attacker machine (Kali Linux), indicating a brute-force attempt.

## Conclusion
The activity was flagged as suspicious and aligns with brute-force attack behavior.
