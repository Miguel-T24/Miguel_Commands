# 🐧 Core Linux Commands

A collection of practical, complex, or hard-to-remember Linux commands used for server administration and environment setup.

## 🗂️ Command Reference

| Description | Command |
| :--- | :--- |
| Show only the primary IPv4 address of the current server | `ip -4 addr show \| grep -oP '(?<=inet\s)\d+(\.\d+){3}'` |
| Minimize the Linux terminal prompt to a '$' sign | `export PS1='$'` |
| Minimize the PowerShell prompt to a '$' sign | `function prompt {"$"}` |

---
