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

## Result

The Windows File Server was successfully configured with secure departmental shares.

### Features Implemented

- ✅ Additional Storage Disk
- ✅ NTFS File System
- ✅ Shared Folders
- ✅ Share Permissions
- ✅ NTFS Permissions
- ✅ Access-Based Enumeration (ABE)
- ✅ Department-Based File Access
