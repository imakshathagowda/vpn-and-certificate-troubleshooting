# 🔐 VPN and Certificate Troubleshooting

---

## 📄 Overview

This project covers real-world network security tasks related to:
- Troubleshooting SSL/TLS certificate errors
- Configuring secure cloud firewall rules
- Designing VPN solutions for Windows and Ubuntu users

Each task reflects common enterprise-level challenges and includes solutions based on best practices.

---

## ✅ Tasks Performed

### 🔹 Task 1: Certificate Issue Troubleshooting

Resolved browser and certificate-related errors reported by users:
- IP address access instead of domain name
- Certificate still shown as expired after renewal
- Untrusted root certificate errors

📄 Detailed analysis: [`certificate_issues.md`](./certificate_issues.md)

---

### 🔹 Task 2: Cloud Firewall Inbound Rule Configuration

Configured cloud VM inbound rules for a secure banking website setup:

| Type | Protocol | Port Range | Source             |
|------|----------|------------|--------------------|
| RDP  | TCP      | 3389       | 18.66.78.112/32    |
| SSH  | TCP      | 22         | 18.66.78.112/32    |
| HTTP | TCP      | 80         | 0.0.0.0/0          |
| HTTPS| TCP      | 443        | 0.0.0.0/0          |

📄 Firewall rules setup: [`firewall_rules.md`](./firewall_rules.md)

---

### 🔹 Task 3: VPN Configuration for Remote Access

Designed two types of VPNs for secure remote access by employees:

#### 📌 VPN Connection 1 – Ubuntu Developers (OpenVPN)
- **VPN Type**: Remote Access
- **Tunnel**: Full Tunnel
- **Protocol**: OpenVPN (UDP 1194)
- **Purpose**: Route all traffic through the corporate network
- **Encryption**: 256-bit AES
- **Key Exchange**: SSL/TLS

#### 📌 VPN Connection 2 – Windows Users (L2TP/IPsec)
- **VPN Type**: Remote Access
- **Tunnel**: Split Tunnel
- **Protocol**: L2TP/IPsec (UDP 500, 4500, 1701)
- **Purpose**: Allow personal traffic (e.g. Netflix) to bypass VPN
- **Encryption**: 256-bit AES
- **Key Exchange**: SSL/TLS

📄 VPN configuration details: [`vpn_configuration.md`](./vpn_configuration.md)

---

## 📂 Project Files

| File | Description |
|------|-------------|
| `Akshatha_NetworkSecurity.pdf` | Original report (all tasks included) |
| `certificate_issues.md` | Analysis of SSL/TLS certificate errors |
| `firewall_rules.md` | Cloud firewall rule setup |
| `vpn_configuration.md` | VPN setup guide for Ubuntu and Windows users |
| `README.md` | This documentation file |

---

## 🚀 How to Use This Repo

1. **Clone the repo** or download the files.
2. Review the markdown files for each task (`*.md`) — easy to read and understand.
3. Use the PowerShell, VPN, and firewall steps in real scenarios or lab environments.
4. Apply the logic to real infrastructure setups (e.g., AWS, Azure, local VM).

---

## 📚 References

- [SSL Labs Test](https://www.ssllabs.com/ssltest/)
- [OpenVPN Setup Guide](https://openvpn.net/community-resources/)
- [L2TP/IPsec Setup (Microsoft)](https://learn.microsoft.com/en-us/windows-server/remote/remote-access/)
- [Firewall Rule Configuration](https://docs.microsoft.com/en-us/azure/virtual-network/)
- [VPN Tunneling Concepts](https://csrc.nist.gov/publications/detail/sp/800-77/rev-1/final)

---

## 👩‍💻 Author

**Akshatha K**  
Network Security Consultant | GitHub: [@imakshathagowda](https://github.com/imakshathagowda) 

---

## 🏷️ Tags

`Network Security` `VPN` `SSL/TLS` `Firewall Rules` `Digital Certificates` `Remote Access` `Windows VPN` `OpenVPN` `Cloud Security`
