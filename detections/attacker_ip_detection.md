# Attacker IP Detection (Sysmon Event ID 3)

## Description
This detection monitors network connections between systems to identify suspicious communication.

## Log Source
- Sysmon Logs
- Event ID: 3 (Network Connection)

## Detection Logic
Track source and destination IP addresses to identify unusual or unauthorized connections.

## Analysis
The logs showed communication between:
- Source IP: Kali Linux (Attacker)
- Destination IP: Windows System (Target)

This indicates attacker activity in the network.

## Conclusion
The connection was identified as part of the simulated attack and successfully detected using Splunk.
