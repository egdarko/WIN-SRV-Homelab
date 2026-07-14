# 4. File Server Configuration

## Objective

Deploy and configure a Windows File Server to provide secure shared folders for different departments using NTFS permissions and Access-Based Enumeration (ABE).

---

## Why File Server?

A File Server centralizes company data, allowing users to securely access shared resources based on their permissions.

---

## Lab Configuration

| Component | Configuration |
|-----------|---------------|
| Server | SRV1 |
| Operating System | Windows Server 2022 |
| Domain | mazen.local |
| Storage | Additional Virtual Hard Disk |
| File System | NTFS |

---

## Step 1 - Add an Additional Virtual Hard Disk

A secondary virtual hard disk was added to store departmental shared folders separately from the operating system drive.

### Screenshot

![Additional Disk](images/adding%20harddrive%20for%20HR%20department.PNG)

---

## Step 2 - Initialize and Format the Disk

Open **Disk Management**, initialize the new disk, create a new volume, and format it using **NTFS**.

### Screenshot

![Disk Management](images/Disk%20managment.PNG)

---

## Step 3 - Create Department Shares

Create shared folders for different departments.

Example:

- HR
- IT
- Public

Configure both **Share Permissions** and **NTFS Permissions** according to each department's requirements.

### Screenshot

![Create Share](images/share%201.PNG)

---

## Step 4 - Configure Share Permissions

Assign the appropriate permissions to allow authorized users access to departmental resources.

### Screenshot

![Share Permissions](images/share%202.PNG)

---

## Step 5 - Enable Access-Based Enumeration (ABE)

Enable **Access-Based Enumeration** so users only see folders they have permission to access.

### Screenshot

![Enable ABE](images/enable%20access-based-enum.PNG)

---

## Step 6 - Verify Access-Based Enumeration

### Before Enabling ABE

Users could view all shared folders regardless of their permissions.

![Before ABE](images/share%20before.PNG)

---

### After Enabling ABE

Users can only view the folders they are authorized to access.

![After ABE](images/share%20after%20enum%20enable.PNG)

---

---

## Step 7 - Deploy Drive Mapping Using Group Policy

To provide users with automatic access to departmental shared folders, a **Group Policy Object (GPO)** was configured to map network drives during user logon.

### Configuration

- Open **Group Policy Management**.
- Create a new GPO or edit an existing one.
- Navigate to:

```
User Configuration
└── Preferences
    └── Windows Settings
        └── Drive Maps
```

- Create a new **Mapped Drive**.
- Configure the following settings:

| Setting | Value |
|---------|-------|
| Action | Update |
| Location | `\\SRV1\IT-Shared` |
| Drive Letter | I: |
| Label | IT-Map |
| Reconnect | Enabled |

- Link the GPO to the appropriate Organizational Unit (OU).

### Screenshot

![Drive Mapping GPO](images/share%203%20map.PNG)

---

## Step 8 - Verify Group Policy

Log on as a domain user and verify that the mapped drive is automatically created.

### Verification

- The **I:** drive appears in **File Explorer**.
- The drive points to the correct shared folder.
- Users can access files according to their assigned permissions.
- The drive is recreated automatically after every logon.

### Screenshot

![Mapped Drive](images/share%204%20map%20sucess.PNG)

---

## Result

The network drive was successfully deployed using **Group Policy Preferences (GPP)**.

### Features Implemented

- ✅ Additional Storage Disk
- ✅ NTFS File System
- ✅ Shared Folders
- ✅ Share Permissions
- ✅ NTFS Permissions
- ✅ Access-Based Enumeration (ABE)
- ✅ Centralized Drive Deployment
- ✅ Automatic Drive Mapping at Logon
- ✅ Department-Based Access
- ✅ Active Directory Integration
- ✅ Group Policy Preferences (GPP)
- ✅ Persistent Network Drive
