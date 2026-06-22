# Day 5 — Event Viewer & Windows Boot Process

---

# Warm-Up — Multiple Choice Review

Try these WITHOUT notes.

---

## 1. Which Linux command displays currently running processes?

A) chmod

B) ps

C) mkdir

D) touch

Answer: b

---

## 2. Which Linux command provides a real-time view of system processes?

A) top

B) ls

C) cp

D) pwd

Answer: a

---

## 3. What does DNS do?

A) Assigns IP addresses automatically

B) Translates domain names into IP addresses

C) Encrypts traffic

D) Routes packets

Answer: b

---

## 4. Which protocol is connection-oriented?

A) UDP

B) ICMP

C) TCP

D) DNS

Answer: c

---

## 5. Which port is commonly used by HTTPS?

A) 22

B) 53

C) 80

D) 443

Answer: d

---

## 6. What protocol does ping primarily use?

A) TCP

B) UDP

C) ICMP

D) HTTP

Answer: c

---

## 7. What is Nmap primarily used for?

A) Editing files

B) Network scanning and discovery

C) Managing users

D) Installing software

Answer: b

---

## 8. Which Windows folder contains user profiles?

A) C:\Windows

B) C:\Program Files

C) C:\Users

D) C:\System32

Answer: c

---

## 9. Which Windows tool is used to manage services?

A) regedit

B) taskmgr

C) services.msc

D) cmd

Answer: c

---

## 10. Which Registry hive stores settings for the currently logged-in user?

A) HKLM

B) HKCU

C) HKCR

D) HKU

Answer: b

---

# Task 1 — Event Viewer

# Event Viewer

---

## Multiple Choice

### What is Event Viewer?

A) A web browser

B) A Windows logging and monitoring tool

C) A file manager

D) A user account manager

Answer: b

---

### Which command opens Event Viewer?

A) taskmgr

B) regedit

C) eventvwr.msc

D) services.msc

Answer: c

---

## Short Answer

### What is Event Viewer?
Event Viewer is a tool in Windows that allows you to view, filter, and analayze event logs recorded by the system. 


---

### Why is Event Viewer useful?
Event Viewer is useful because it serves as a central diagnostic tool for troubleshooting system errors, monitoring application crashes, and reviewing security audits. 


---

# Windows Logs

Open:

```text
eventvwr.msc
    #This tool allows you to monitor and manages event logs recorded by the system. 
```

Navigate to:

```text
Windows Logs
    Application
    System
    Security
```

Spend a few minutes exploring.

---

## Application Log

### What types of events did you notice?
When I was in this log, I noticed that all the logs related to applications of some sort (which makes sense). It was mostly information about things that happened to applications, but there were a couple warnings and errors as well. 


---

### Did you see any warnings or errors?
I did see 1 warning, which was about the Windows Search Service, and 3 different errors relating to license activation. I decided to look up the error code (Error code 0x803F7001) to see why that happened, and it told me that it was that the system couldn't find a valid digital license or product key to activate the os, which makes sense as this is the free version afterall. 


---

## System Log

### What types of events did you notice?
When I was in this log, I noticed that all the logs here were all about system events like Windows Updates, which makes sense. There was one event that was about access history in a hive of the Windows Registry, but that was about it. 


---

### Did you see any warnings or errors?
I saw 1 warning that was about the time service, and 3 errors regarding failed Windows updates, but that was about it. 


---

## Security Log

### What types of events did you notice?
All the events I saw in the security log were audit successes. My guess is that these are all security audits, which is why there are so many. 


---

### What kinds of activities appear to be recorded?
From what I saw, the activites that were recorded were about reading stored credentials, probably indicating that they are not to be seen by everyone. 
Note: Security logs record many things, like Logins, Logouts, Account Creation, and so on. (Graded)

---

# Observation Questions

## Multiple Choice

### Which log is generally most useful when troubleshooting application crashes?

A) Application

B) Security

C) Setup

D) Forwarded Events

Answer: a

---

### Which log is generally most useful when troubleshooting hardware or driver problems?

A) Application

B) Security

C) System

D) Setup

Answer: c

---

## Short Answer

### Which log seemed most useful for troubleshooting?
The System log is the best log when it comes to broad troubleshooting. 
Note: Different logs are best for different problems. (Graded)

---

### Why?
The reason why the System log is the best is because it records critical os events, like driver failures and hardware errors. 


---

### What events did you see?
All the events I saw in the System log related to the system in some way, like Windows Updates and the time service.


---

# In Your Own Words

### Explain Event Viewer to a beginner.
Event Viewer is a tool in Windows that allows you to view and manage events that the OS has logged. 


---

### Why is logging important in cybersecurity?
Logging is important in cybersecurity because it gives detailed events of everything that has happened on the system, allowing administrators to view and troubleshoot events like errors or unauthorized activities. 


---

# Task 2 — Windows Boot Process

# Windows Boot Process

---

## Multiple Choice

### What happens first when a computer starts?

A) User Login

B) Services Start

C) Power On

D) Windows Desktop Loads

Answer: c

---

### Which component loads Windows after firmware initialization?

A) Registry Editor

B) Windows Boot Manager

C) Task Manager

D) Event Viewer

Answer: b

---

## Basic Boot Flow

```text
Power On
    ↓
UEFI / BIOS
    ↓
Windows Boot Manager
    ↓
Windows Kernel
    ↓
System Services
    ↓
User Login
```

---

## Fill In The Blanks

### Step 1

The computer receives:
Power Supply Activation

---

### Step 2

The firmware loads:
BIOS/UEFI
    POST to check essential hardware

---

### Step 3

The firmware starts:
Bootloader (Windows Boot Manager)


---

### Step 4

Windows loads the:
Windows Loader and Kernel


---

### Step 5

Windows starts:
Session 0 (System Services)


---

### Step 6

The user reaches:
User Login Page


---

## Short Answer

### What is the role of UEFI/BIOS?
The role of UEFI/BIOS is to run the Power-On Self Test, configure hardware, and locate the bootloader for Windows to launch. 


---

### What is the role of Windows Boot Manager?
The role of Windows Boot Manager is to read the Boot Configuration Data (BCD) to identify available operating systems, load the Windows kernal, and load essential drivers into memory. 


---

### What is the Windows Kernel responsible for?
The role of the Windows Kernel is to act as the bridge between user applications and computer hardware and manage system resources, among others. 


---

### What loads before user login?
Before the user login, the OS completes the POST (Power-On-Self-Test), loads the kernel, initializes hardware drivers, and load services. After that is done, it proceeds to load winlogon.exe, which then leads towards the user login. 


---

### Why is the boot process important?
The boot process is important for Windows because it is how the system boots up and runs. Without one part of the process, the system would not be able to function. 


---

# In Your Own Words

### Explain the Windows boot process to a beginner.
The Windows boot process is the process of how a Windows system boots up. There are 6 steps to the process:
    1. Power Supply Activation
    2. BIOS/UEFI
    3. Windows Boot Manager
    4. Windows Kernal
    5. System Services
    6. User Login
Each one of these steps in succession allow for the Windows system to boot up and function. 
Note: The Windows boot process is the sequence of events that starts when the computer powers on and ends when the user reaches the login screen, with each stage preparing the next stage to run. (Graded)

---

# Task 3 — Weekly Summary

# Windows Fundamentals Review

---

## Multiple Choice

### Which folder contains most Windows operating system files?

A) Users

B) Downloads

C) Windows

D) Temp

Answer: c

---

### Which folder primarily stores user profiles?

A) Users

B) Program Files

C) Windows

D) System32

Answer: a

---

### Which account type should generally be used for daily activities?

A) Administrator

B) Standard User

Answer: b

---

### Which tool is used to monitor running processes and system performance?

A) Registry Editor

B) Task Manager

C) Event Viewer

D) Services

Answer: b

---

### Which startup type launches automatically when Windows starts?

A) Disabled

B) Manual

C) Automatic

Answer: c

---

### Which Registry hive stores system-wide settings?

A) HKCU

B) HKCR

C) HKLM

D) HKU

Answer: c

---

### Which Registry hive stores settings for the current user?

A) HKLM

B) HKCU

C) HKCR

D) HKU

Answer: b

---

### Which Windows tool stores and displays system logs?

A) Registry Editor

B) Event Viewer

C) Task Manager

D) Control Panel

Answer: b

---

### Which component loads Windows after UEFI/BIOS?

A) Kernel

B) Services

C) Windows Boot Manager

D) Explorer.exe

Answer: c

---

### Which principle says users should have only the permissions they need?

A) Defense in Depth

B) Least Privilege

C) Segmentation

D) Availability

Answer: b

---

# End-of-Week Reflection

## Confidence Level (1–10)

Windows Fundamentals:

4 / 10

---

## Which topic felt easiest this week?

A) Windows File System

B) User Accounts & Administration

C) Task Manager & Services

D) Registry

E) Event Viewer

F) Windows Boot Process

Answer: d (or a)

---

## Which topic felt hardest this week?

A) Windows File System

B) User Accounts & Administration

C) Task Manager & Services

D) Registry

E) Event Viewer

F) Windows Boot Process

Answer: f

---

## What was the biggest thing you learned this week?
The biggest thing I learned this week is how the Windows file system worked, as I didn't realize how it was actually structured til recently. 


---

## Which Windows tool do you think will be most useful in cybersecurity?
Event Viewer seems like the most useful tool for cybersecurity, as it logs all the events that happen on the system, and will be helpful for things like forensics. 


---

## Which topic do you want to learn more about?
The topic I want to learn more about is the Windows Registry, as I know that attackers will go for that section of the computer at some point. 


---

## In one paragraph, summarize what you learned about Windows this week.
This week, I learned how to use the Windows operating system with basic administration knowledge. I learned about the Windows file system, accounts and administration, task manager, services, the Windows Registry, event viewer, and the Windows boot process. I feel more confident in the Windows than I did previously, and I hope that the confidence continues to grow in the future. 


---