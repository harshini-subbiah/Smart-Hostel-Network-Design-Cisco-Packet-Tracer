# Setup Guide

This document explains how to set up and run the **Smart Hostel Network Design** project using Cisco Packet Tracer.

---

# Software Requirements

- Cisco Packet Tracer 8.0 or later
- Windows, Linux, or macOS

---

# Installation

## 1. Install Cisco Packet Tracer

Download and install Cisco Packet Tracer from Cisco Networking Academy.

After installation, verify that Packet Tracer opens correctly.

---

## 2. Clone the Repository

```bash
git clone https://github.com/yourusername/Smart-Hostel-Network-Design-Cisco-Packet-Tracer.git
```

or simply download the repository as a ZIP file and extract it.

---

## 3. Open the Project


Open

```
hostel.pkt
```

using Cisco Packet Tracer.

---

# Running the Simulation

1. Open **hostel.pkt**.
2. Wait until all devices finish initializing.
3. Use either:
   - Realtime Mode
   - Simulation Mode
4. Allow routing tables and DHCP services a few seconds to stabilize.

---

# Validation Steps

## 1. DHCP Test

Open any PC.

Go to:

```
Desktop → IP Configuration
```

Select

```
DHCP
```

Expected Result:

- IP Address assigned automatically
- Subnet Mask assigned
- Default Gateway assigned
- DNS Server assigned

---

## 2. DNS Test

Open

```
Desktop → Command Prompt
```

Run:

```text
ping hostel.com
```

Expected Result:

Hostname resolves successfully.

---

## 3. HTTP Server Test

Open

```
Desktop → Web Browser
```

Visit:

```text
http://hostel.com
```

Expected Result:

The configured web page loads successfully.

---

## 4. VLAN Communication Test

From a PC, run:

```text
ping <IP address of another authorized VLAN device>
```

Expected Result:

Ping succeeds if communication is allowed.

---

## 5. ACL Validation

From the Guest Laptop, attempt to access restricted internal resources.

Expected Result:

Access is denied according to the configured ACL rules.

---

## 6. Internet Connectivity Test

From a PC or Guest Laptop, verify internet connectivity (as configured in the simulation).

Expected Result:

Internet access is available while internal restrictions remain enforced.

---

## 7. Wireless Connectivity Test

Connect the Guest Laptop to the configured wireless network.

Verify that:

- Wireless connection is established
- DHCP assigns an IP address
- Internet access works
- ACL restrictions remain active

---

## 8. Switch Trunk Verification

Verify that trunk links correctly carry traffic between VLANs.

Expected Result:

Inter-switch VLAN communication functions correctly.

---

## 9. Syslog Verification

Generate network activity.

Verify that logs are received by the Syslog Server.

---

# Troubleshooting

### Devices remain red

Wait a few seconds for Packet Tracer to initialize interfaces and routing.

---

### DHCP is not assigning IP addresses

- Ensure DHCP service is enabled.
- Verify VLAN configuration.
- Check router interfaces.

---

### DNS is not resolving

- Confirm the DNS server IP is correctly configured.
- Verify the DNS records.
- Ensure clients received the DNS server address via DHCP.

---

### Web server cannot be reached

- Verify HTTP service is enabled.
- Check server IP configuration.
- Ensure ACL rules permit HTTP traffic where intended.

---

### Guest network can access restricted resources

- Verify ACL configuration.
- Confirm ACLs are applied to the correct router interfaces.
- Test from the Guest Laptop again.

---

# Notes

This project is intended for educational purposes and demonstrates practical enterprise networking concepts including VLAN segmentation, inter-VLAN routing, DHCP, DNS, ACL security, wireless networking, centralized services, and network monitoring using Cisco Packet Tracer.
