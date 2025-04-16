# 🔥 Cloud Firewall Inbound Rules (Secure VM Access)

This document lists firewall rules required for securely exposing a cloud-hosted VM used for banking operations.

---

## 🔐 Inbound Rules Table

| Type | Protocol | Port Range | Source             |
|------|----------|------------|--------------------|
| RDP  | TCP      | 3389       | 18.66.78.112/32    |
| SSH  | TCP      | 22         | 18.66.78.112/32    |
| HTTP | TCP      | 80         | 0.0.0.0/0          |
| HTTPS| TCP      | 443        | 0.0.0.0/0          |

---

## 🔎 Rule Explanation

- **RDP (Port 3389)**: Restricted to the cloud administrator's static IP.
- **SSH (Port 22)**: Same as above, allowing secure admin access via terminal.
- **HTTP/HTTPS (Ports 80/443)**: Open to all (public web traffic).

✅ Security best practices applied:
- Only essential ports are exposed.
- Administrative access is IP-restricted.
- All traffic to sensitive services is encrypted via HTTPS or SSH.
