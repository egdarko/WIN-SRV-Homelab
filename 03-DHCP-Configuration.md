# 3. DHCP Configuration

## Objective

Configure the Dynamic Host Configuration Protocol (DHCP) service to automatically assign IP addresses and network settings to domain clients within the **mazen.local** environment.

---

## Why DHCP?

DHCP automates IP address assignment, reducing manual configuration and ensuring that all domain clients receive the correct network settings.

---

## Lab Configuration

| Component | Configuration |
|-----------|---------------|
| Domain | `mazen.local` |
| Network | `10.10.10.0/24` |
| DHCP Server | `SRV1` |
| Server IP Address | `10.10.10.2` |
| DNS Server | `10.10.10.2` |
| Router | `10.10.10.1` |

### DHCP Scope

| Setting | Value |
|---------|-------|
| Start IP Address | `10.10.10.10` |
| End IP Address | `10.10.10.200` |
| Subnet Mask | `255.255.255.0` |
| Exclusion Range | `10.10.10.10 – 10.10.10.30` |

> **Note:** The exclusion range reserves addresses for infrastructure devices and prevents them from being assigned to DHCP clients.

---

## Step 1 - Install and Configure the DHCP Server

Install the **DHCP Server** role from **Server Manager** and complete the post-installation configuration by authorizing the DHCP server in Active Directory.

---

## Step 2 - Create a DHCP Scope

Create a new IPv4 scope using the following configuration:

- Scope Name: **LAN**
- Network: **10.10.10.0/24**
- IP Range: **10.10.10.10 – 10.10.10.200**
- Exclusion Range: **10.10.10.10 – 10.10.10.30**
- Lease Duration: **10 Days**

![DHCP Configuration](images/config%20DHCP%20SERVER.PNG)
---


## Step 3 - Verify DHCP Operation

The client IP configuration and verify that the address is leased from the DHCP server.

### Screenshot

![DHCP Test](images/test%20DHCP.PNG)


![DHCP Client Verification](images/test%20dhcpp.PNG)

---

## Result

The DHCP server successfully distributes IP addresses and network configuration to domain clients.

### Verified

- ✅ DHCP Scope Created
- ✅ DHCP Server Authorized
- ✅ Client Received Dynamic IP Address
- ✅ Domain Connectivity Confirmed
