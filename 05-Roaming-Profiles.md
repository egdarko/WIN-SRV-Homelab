# 5. Roaming Profiles

## Objective

Configure Roaming Profiles to allow users to access the same desktop environment, settings, and personal files regardless of which domain-joined computer they use.

---

## Why Roaming Profiles?

Roaming Profiles store user profiles on a central file server instead of the local computer. When users sign in to another domain-joined computer, their profile is automatically downloaded, providing a consistent user experience.

---

## Lab Configuration

| Component | Configuration |
|-----------|---------------|
| Server | SRV1 |
| Domain | mazen.local |
| Profile Storage | Shared Folder |
| Profile Type | Roaming Profile |

---

## Step 1 - Create the Profile Share

Create a shared folder that will store roaming profiles.

Configure:

- Share Permissions
- NTFS Permissions

### Screenshot

![Roaming Permissions](images/roaming%20permission.PNG)

---

## Step 2 - Configure the User Profile Path

Open **Active Directory Users and Computers**.

Navigate to:

User Properties → Profile

Configure the **Profile Path** using the following format:

```text
\\SRV1\Profiles\%username%
```

### Screenshot

![Profile Path](images/change%20Manager%20user%20from%20local%20to%20roaming%20user.PNG)

---

## Step 3 - Apply the Configuration

Save the configuration and verify that the user account is configured to use a roaming profile.

### Screenshot

![Roaming Profile Configured](images/roaming%20done.PNG)

---

## Step 4 - Test the Roaming Profile

Sign in using the configured domain user.

Create a file or modify the desktop.

Sign out and sign in again (or sign in from another domain-joined computer).

Verify that:

- Desktop settings are preserved.
- User files are synchronized.
- The roaming profile loads successfully.

### Screenshot

![Roaming Profile Test](images/roaming%20test.PNG)

---

## Result

Roaming Profiles were successfully configured and tested.

### Features Implemented

- ✅ Centralized User Profiles
- ✅ Domain User Profile Storage
- ✅ Profile Synchronization
- ✅ Consistent User Experience Across Computers
- ✅ Active Directory Profile Management
