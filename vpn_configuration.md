# 🔐 VPN Configuration Summary

Designed secure VPN connectivity for remote workers using different operating systems.

---

## 📡 VPN 1: Ubuntu Developers (OpenVPN)

- **OS**: Ubuntu 20.04
- **VPN Type**: Remote Access
- **VPN Protocol**: OpenVPN
- **Tunnel Method**: Full Tunnel
- **Encryption**: 256-bit AES
- **Key Exchange**: SSL/TLS
- **Port**: UDP 1194
- **Traffic Routing**: All traffic routed through corporate network
- **Purpose**: Secure access to main software repository server

🛠 **Notes**:
- Install and configure OpenVPN on the developer systems.
- Restrict access to specific internal services.

---

## 📡 VPN 2: Windows Users (L2TP/IPsec)

- **OS**: Windows 10
- **VPN Type**: Remote Access
- **VPN Protocol**: L2TP/IPsec
- **Tunnel Method**: Split Tunnel
- **Encryption**: 256-bit AES
- **Key Exchange**: SSL/TLS
- **Ports**: UDP 500, UDP 4500, UDP 1701
- **Traffic Routing**: Personal traffic (e.g., Netflix) bypasses corporate network
- **Purpose**: Ease of setup, non-corporate traffic allowed outside the tunnel

🛠 **Notes**:
- Set up pre-shared keys or install certificates.
- Configure Windows VPN client to allow split tunneling.
- Ensure firewall allows IPsec-related ports.
