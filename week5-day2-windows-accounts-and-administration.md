# Week 5 — Day 2
# Windows Accounts & Administration

---

# Warm-Up — Multiple Choice Review

Try these WITHOUT notes.

---

### 1. Which device primarily forwards traffic between different networks?

A) Switch

B) Router

C) DHCP Server

D) Access Point

Answer: b

---

### 2. Which device primarily forwards traffic using MAC addresses?

A) Router

B) Switch

C) DNS Server

D) DHCP Server

Answer: b

---

### 3. What does DNS do?

A) Assign IP addresses automatically

B) Encrypt web traffic

C) Translate domain names into IP addresses

D) Route packets

Answer: c

---

### 4. What does DHCP do?

A) Assign IP addresses automatically

B) Resolve domain names

C) Encrypt traffic

D) Route packets

Answer: a

---

### 5. Which protocol is connection-oriented?

A) UDP

B) TCP

C) ICMP

D) DNS

Answer: b

---

### 6. Which protocol is generally faster because it does not retransmit lost packets?

A) TCP

B) HTTPS

C) UDP

D) SSH

Answer: c

---

### 7. Which port is commonly used by SSH?

A) 21

B) 53

C) 80

D) 22

Answer: d

---

### 8. Which port is commonly used by HTTPS?

A) 443

B) 22

C) 80

D) 53

Answer: a

---

# Task 1 — User Accounts

# Windows User Accounts

---

## Multiple Choice

### What is a Standard User account?

A) An account with unrestricted system access

B) An account used only by Windows services

C) An account with limited permissions for everyday use

D) A hidden account

Answer: c

---

### What is an Administrator account?

A) An account with elevated privileges that can make system-wide changes

B) A guest account

C) A networking account

D) A backup account

Answer: a

---

## Short Answer

### What is a user account?
A user account is a collection of settings, permissions, and an identity that defines the items a user can access or make. 

---

### What is the purpose of a Standard User account?
The purpose of a stand user account is to allow the user to perform daily tasks with limited permissions, preventing unauthorized changes on the system. 

---

### What is the purpose of an Administrator account?
The purpose of an administrator account is to give elevated priviledges to the desired user for managing the system. 

---

# User Profiles

---

## Multiple Choice

### Where are Windows user profiles typically stored?

A) C:\Windows

B) C:\Program Files

C) C:\Users

D) C:\System32

Answer: c

---

### What does a user profile contain?

A) Only passwords

B) User settings, files, and preferences

C) Only applications

D) Network cables

Answer: b

---

## Fill In The Blanks

A user profile is stored inside:
C:\Users

---

A user profile contains:
User settings, files, and prefrences.

---

## Short Answer

### What is a user profile?
A user profile is a creditional-based identity that determines what perimissions a user has on Windows. 
Note: A collection of user-specific files, settings, desktop configurations, documents, and preferences stored for a user account. (Graded)

---

### Why are user profiles useful?
User profiles are important because they let people use the Windows system with a personalized interface that is secure and consistant. They are also useful because each profile has a set of permissions assigned to them, which can prevent personal user data being mixed in with configuration files. 
Note: The profile stores the user's environment. (Graded)

---

# Local Accounts

---

## Multiple Choice

### What is a local account?

A) An account stored only on the local computer

B) A cloud account

C) A router account

D) A DNS account

Answer: a

---

### Which type of account can be used without Internet access?

A) Local account

B) Microsoft account only

Answer: a

---

## Short Answer

### What is the difference between a local account and a Microsoft account?
A local account on windows is an offline, device specific identity stored locally, while a Microsoft Account is a cloud-based identity linked to an email address that syncs settings across multiple devices. 

---

# Security Concepts

---

## Multiple Choice

### Why should you avoid using an Administrator account for daily activities?

A) It makes the computer slower

B) It uses more storage

C) Malware would gain administrator privileges if the account is compromised

D) It prevents software installation

Answer: c

---

## Short Answer

### Why is it safer to use a Standard User account for daily tasks?
Using a standard user account for daily tasks is desired because if the computer were to be compromised, then the threat would have full access to the computer, something we don't want to happen. 


---

### What could happen if malware runs under an Administrator account?
If malware runs under an Administrator account, then it has full access to the system, and can cause system altering changes. 

---

# In Your Own Words

### Explain the difference between a Standard User and an Administrator account.
A standard user account is a system identity that is meant to have limited permissions, allowing the user to be able to access their personal data privately and securely. An Administrator account is a system identity that has elevated privileges, gaining access to the full system, allowing them to download software and access other system related documents. 


---

### Explain why using least privilege improves security.
Using less privileges improves security due because if the machine were to be compromised, the threat would not have full access to the system, preventing permanent damage to the system. 
Note: Users should only receive the minimum permissions necessary to perform their job. (Graded)

---

# Task 2 — Administration Tools

# Exploring Administration Tools

Open and explore:

```text
compmgmt.msc
    #This tool allows you to manage components like Device Manager, Disk Management, Event Viewer, Task Scheduler, Services, and Local Users and Groups in a single window.
Control Panel
    #This tool allows you to view and change system setting, manage hardware/software, and configure user accounts. 

```

If available, also open:

```text
lusrmgr.msc
    #This tool is a Local Users and Groups manager that allows administrators to create, modify, disable, and delete local user accounts and groups on your system. 
    #Note: This tool was not on my vm, so I was not able to explore it. 
```

---

# Computer Management

## Multiple Choice

### What is Computer Management?

A) A game launcher

B) A centralized administration console

C) A web browser

D) A file explorer replacement

Answer: b

---

## Short Answer

### What sections did you see inside Computer Management?
I saw 3 big sections (System Tools, Storage, and Services and Applications), with there being 6 sections inside the System Tools section (Device Manager, Performance, Event Viewer, Task Scheduler, Shared Folders, and Local Users and Groups), 1 in the Storage section (Disk Management), and 2 in the Services and Applications (Services and WMI Control).

---

### What seemed most useful?
I would say Performance and Event Viewer seemed the most useful, as they seemed like the tools that would help the most (like viewing events that have happened on the system and what the performance is looking like on the computer).


---

# Users & Groups

## Fill In The Blanks

### What local user accounts exist?
There were 5 local user accounts on the system:
    Administrator
    DefaultAccount
    Guest
    jared (vm account i created not my real name)
    WDAGUtilityAccount

---

### What local groups exist?
There were 21 local groups that exist on the system, most of which seemed like elevated priviledged groups (but not administrators though).

---

## Short Answer

### Which built-in account seemed most important?
The Administrator account seemed the most important due to the elevated privileges it possesses. 

---

### Which built-in group seemed most important?
Once again, the Administrators group seemed the most important due to the elevated privileges the group possesses.

---

### Were there any accounts you did not create yourself?

A) Yes

B) No

Answer: a

---

### If yes, what were they?
    Administrator
    DefaultAccount
    Guest
    WDAGUtilityAccount

---

# Control Panel

## Multiple Choice

### What is Control Panel primarily used for?

A) Viewing websites

B) Managing Windows settings and administrative tasks

C) Playing media

D) Viewing network packets

Answer: b

---

## Short Answer

### What settings categories did you notice?
At the first page of the tool, it listed the categories as follows:
    System and Security
    Network and Internet
    Hardware and Sound
    Programs
    User Accounts
    Appearance and Personalization
    Clock and Region
    Ease of Access
Under each of these categories were a handful of settings you could access, like "Review your computer's status" and "Uninstall a program". 

---

### What category seemed most useful?
I would say the System and Security category seemed the most useful, as it relates directly the the system itself and has a lot of important system wide settings under it. 

---

# Observation Questions

## Short Answer

### What groups existed on your system?
There were 21 groups that existed on my system (vm), with most of them being ones with elevated privileges like Device Owners and Hyper-V Administrators. 

---

### What accounts already existed?
There were 4 accounts on my system that already existed, and they mainly existed in order to help with setting up the computer it seems like (though I am not 100% sure).
Note: Those account exist for specific purposes. (Graded)

---

### Did anything surprise you?
I was surprised at how many groups there were on the system. I expected some of course, but 21 seemed like a lot more than I thought. 

---

# Reflection

### What administration tool seemed most useful?
The Computer Managment tool seemed like the most useful, as it had multiple tools within it that could be of use futher down the line (like Performance and Event Viewer).

---

### Which section was easiest to understand?
The easiest section to understand was the Local Users and Groups section, as they seemed pretty straight forward. 

---

### Which section was most confusing?
The most confusing section was most likely the specific users like "WDAGUtilityAccount", as that seems like a very specific account for a very specific purpose. 

---

### In one sentence, explain why administrative tools are important.
Administrative tools are important because they help monitor and manage the system as a whole. 

---

