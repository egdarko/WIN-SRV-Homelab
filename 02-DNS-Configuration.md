# 2. DNS Configuration

## Objective

Configure the Domain Name System (DNS) required for Active Directory and verify that clients can resolve hostnames within the domain.

---

## Why DNS?

Active Directory relies on DNS to locate domain controllers and authenticate users. Without a properly configured DNS server, domain clients cannot join or communicate with the domain.

---

## Configuration

The DNS Server role was installed automatically during the Active Directory Domain Services (AD DS) installation.

The lab domain:

```text
mazen.local
```

The DNS server is configured with:

- Forward Lookup Zone
- Host (A) Records
- Active Directory Integration

---

## Create DNS Records

Create New DNS records for domain resources.

### Screenshot

![DNS Records](images/creating%20new%20dns%20records.PNG)

---

## Verify DNS Resolution

Verify that clients can resolve the domain and server hostname using `nslookup` and `ping`.

### Test 1

![DNS Test](images/test%20DNS.PNG)

### Test 2

![DNS Test 2](images/test%20dns2.PNG)

---

## Result

The DNS server successfully resolved domain resources and allowed clients to communicate with the Active Directory environment.

✅ DNS is fully operational.
