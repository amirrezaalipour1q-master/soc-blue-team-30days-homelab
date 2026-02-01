# Day 07 – SSH Brute Force Detection & SOC Triage

## 🎯 Objective
In this lab, I simulated and analyzed an SSH brute-force attack to understand
how a SOC analyst detects authentication abuse, performs triage, and makes
incident-handling decisions based on log evidence.

---

## 🧪 Lab Environment
- **Operating System:** Kali Linux
- **Service:** OpenSSH
- **Log Source:** systemd journal
- **Log Tool:** journalctl

> Note: Kali Linux does not use `/var/log/auth.log` by default.  
> SSH authentication logs are accessed via `journalctl`.

---

## 🔥 Attack Simulation

### Failed Login Attempts
Multiple incorrect SSH login attempts were performed to generate brute-force
authentication events.
```bash
ssh localhost
