# Week 5 Day 4 — Registry Basics

---

# Warm-Up — Multiple Choice Review

Try these WITHOUT notes.

---

### 1. Which protocol is connection-oriented?

A) UDP

B) ICMP

C) TCP

D) DNS

Answer: c

---

### 2. Which protocol is generally faster because it does not retransmit lost packets?

A) TCP

B) UDP

C) HTTPS

D) SSH

Answer: b

---

### 3. Which port is commonly used by HTTPS?

A) 22

B) 53

C) 80

D) 443

Answer: d

---

### 4. Which port is commonly used by SSH?

A) 20

B) 21

C) 22

D) 443

Answer: c

---

### 5. What is HTTP primarily used for?

A) Assigning IP addresses

B) Transferring web content

C) Encrypting files

D) Routing packets

Answer: b

---

### 6. Why is HTTPS safer than HTTP?

A) It is faster

B) It uses more ports

C) It encrypts data in transit

D) It blocks malware automatically

Answer: c

---

### 7. What protocol does ping primarily use?

A) TCP

B) UDP

C) ICMP

D) HTTP

Answer: c

---

### 8. What is Nmap primarily used for?

A) Editing files

B) Network scanning and discovery

C) Managing users

D) Installing software

Answer: b

---

# Task 1 — Registry Fundamentals

# Windows Registry

---

## Multiple Choice

### What is the Windows Registry?

A) A folder that stores documents

B) A database that stores Windows and application settings

C) A networking protocol

D) A user account

Answer: b

---

### Which tool is used to view the Registry?

A) services.msc

B) compmgmt.msc

C) regedit

D) taskmgr

Answer: c

---

## Short Answer

### What is the Windows Registry?
The Windows registry is a hierarchical database used by the Windows OS to store low-level configuration settings for the OS, hardware, and applications. 

---

### Why is the Registry important?
The Windows registry is important because it serves as the centralized database that store all the low-level configuration settings for the OS, hardware, and installed applications. Without, Windows would not know how to boot, what drivers to use, and how to maintain user preferences. 

---

### What kinds of information are stored in the Registry?
The registry stores important data that dictates how the computer looks, feels, and behaves.

---

# Registry Hives

The Registry is divided into sections called **hives**.

---

## Fill In The Blanks

### HKEY_LOCAL_MACHINE (HKLM)
HKLM is a primary hive in the Windows Registry that serves as the central repository for system-wide configuration settings. 

---

### HKEY_CURRENT_USER (HKCU)
HKCU is a registry hive that serves to store configuration settings and preferences for the current logged in user. 

---

### HKEY_USERS (HKU)
HKU is a registry hive that serves to store user-level configuration information for all user profiles on the system. 

---

### HKEY_CLASSES_ROOT (HKCR)
HKCR is a registry hive that serves to store file associations, OLE (Object Linking and Embedding) settings, and COM (Component Object Model) class registration information.
Note: I don't know what any of these things are, and I'm guessing these are more advanced topics that this week provides. I will learn these things eventually, just not now. 

---

## Multiple Choice

### Which hive contains settings for the currently logged-in user?

A) HKLM

B) HKCU

C) HKCR

D) HKU

Answer: b

---

### Which hive contains system-wide settings?

A) HKCU

B) HKCR

C) HKLM

D) HKU

Answer: c

---

## Short Answer

### What is the difference between HKLM and HKCU?
HKLM is a registry hive that stores system wide configuration settings, while HKCU is a registry hive that stores configuration settings and preferences for the current logged in user. 

---

### Why are Registry hives useful?
Registry hives are important because they serve as containers for the Windows OS to store important configuration settings and other items in a manageable and secure structure. 

---

# In Your Own Words

### Explain the Windows Registry to a beginner.
The Windows Registry is a hierarchical database used by the Windows OS to store important low-level configuration settings. 

---

### Explain what a Registry hive is.
A registry hive is a container in the Windows Registry that store important configuration settings for the system.  

---

# Task 2 — Explore Registry Editor

# Registry Editor Exploration

Open:

```text
regedit (short for Registry Editor)
    #This tool allows you to monitor and manage the Windows Registry. 
```

Browse:

```text
HKEY_LOCAL_MACHINE (HKLM)
HKEY_CURRENT_USER (HKCU)
```

Take a few minutes to explore.

---

# HKLM Exploration

## HKEY_LOCAL_MACHINE

### What did you notice inside this hive?
I noticed in this hive a lot of basic system configuration folders, like COMPONENTS and DRIVERS, and that some of the folders can't be opened, like SCHEMA. 

---

### What kinds of settings appeared to be stored?
In this hive, I saw the following folders:
    BCD00000000
    COMPONENTS
    DRIVERS
    HARDWARE
    SAM
    SCHEMA
    SECURITY
    SOFTWARE
    SYSTEM
This is in line with what the whole hive stores, which is system wide configuration settings.  

---

# HKCU Exploration

## HKEY_CURRENT_USER

### What did you notice inside this hive?
In this hive, I noticed that there were some personalization folders, like Keyboard Layout and Enviroment, and that all the folders were accessible. 

---

### What kinds of settings appeared to be stored?
In this hive, I saw the following folders:
    AppEvents
    Console
    Control Panel
    Enviroment
    EUDC
    Keyboard Layout
    Microsoft
    Network
    Printers
    Software
    System
    Volatile Enviroment
Some of these were expected, like Keyboard Layout, but some I didn't quite understand, like Volatile Enviroment. I guess I will learn what these all are specifically in the future. 

---

# Observation Questions

## Multiple Choice

### Why should administrators be careful when editing the Registry?

A) Registry changes can break Windows or applications

B) The Registry controls network cables

C) The Registry cannot be modified

D) The Registry only stores passwords

Answer: a

---

## Short Answer

### Why is the Registry important to Windows?
The Windows Registry is important because it stores all the low-level configuration settings for the OS, hardware, and installed applications. Without it, the system could not run. 

---

### What information appeared to be stored in HKLM?
The HKLM hive seemed to have information regarding system wide settings, like COMPONENTS and DRIVERS.

---

### What information appeared to be stored in HKCU?
The HKCU hive appeared to store configuration settings and preferences tailored to the current logged in user. 

---

### What could happen if a critical Registry entry is deleted?
If a critical Registry entry is deleted, it could cause system instability, application crashes, or a complete failure for the Windows system to boot. It is best that critical entries do not get deleted. 

---

# Reflection

### What part of the Registry was easiest to understand?
I would say the easiest part to understand was the concept itself, and it seems pretty straight when you get to the brass of it. 

---

### What part of the Registry was most confusing?
I would say that certain folders under some of the hives confused me a little, like SCHEMA and stuff like OLE settings are quite intracate.  

---

### Did anything surprise you while exploring?
I think the main thing that surprised me was that the hives were more different than I thought they were going to be, like HKLM and HKCU are a little similar, but HKCR is completely different and is filled with settings and files. 

---

### In one sentence, explain why administrators must be careful when editing the Registry.
Administrators must be careful when editing the Registry because if a critical entry gets deleted, then the system could have troubles and become unstable, maybe even failing to boot.

---

# In Your Own Words

### Explain Registry Editor to a beginner.
The Windows Registry Editor is a tool on Windows that allows you to view, use, and edit the Windows Registry on your system. 

---
