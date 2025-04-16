# 📜 Certificate Troubleshooting Guide

This document explains common SSL/TLS certificate-related errors raised by users and how to resolve them effectively.

---

## 🧾 Ticket 1: IP Address vs Domain Name

- **Problem**: Browsing the site via IP shows a certificate error.
- **Root Cause**: Certificates are issued for domain names (FQDNs), not IP addresses.
- **Solutions**:
  - Use the domain name, not the IP.
  - Check certificate CN and SAN fields.
  - Verify the certificate isn't expired or revoked.
  - Ensure intermediate certificates are properly configured.

---

## 🧾 Ticket 2: Renewed Certificate Still Shows Expired

- **Problem**: Browser still reports certificate as expired after renewal.
- **Possible Causes**:
  - Old certificate is still in use.
  - System time is incorrect.
  - Browser caching the old cert.
  - Certificate not properly bound to the domain.
  - Missing intermediate certificates.

- **Solutions**:
  - Reinstall the renewed certificate and restart the web server.
  - Sync time on server/client devices.
  - Clear browser cache or use incognito mode.
  - Verify full certificate chain is installed.

---

## 🧾 Ticket 3: Root Certificate Not Trusted

- **Problem**: Browser error shows root certificate is not trusted.
- **Root Cause**: Client system does not recognize the certificate authority.

- **Solutions**:
  - Update the browser and OS to get the latest trusted root CAs.
  - Manually install missing root certificate (if using private CA).
  - Check for any SSL interception (antivirus, proxy).
  - Use tools like SSL Labs to inspect server certificate setup.
