# Week 5 — Day 3
# Task Manager & Services

---

# Warm-Up — Multiple Choice Review

Try these WITHOUT notes.

---

### 1. Which command displays currently running processes in Linux?

A) mkdir

B) chmod

C) ps

D) cd

Answer: c

---

### 2. Which Linux command provides a real-time view of system processes?

A) touch

B) top

C) cp

D) pwd

Answer: b

---

### 3. Which tool is commonly considered a more user-friendly version of top?

A) htop

B) ls

C) rm

D) sudo

Answer: a

---

### 4. Which command is used to terminate a process?

A) ps

B) top

C) kill

D) cat

Answer: c

---

### 5. What is a process?

A) A running instance of a program

B) A network cable

C) A user account

D) A service port

Answer: a

---

### 6. Which protocol is connection-oriented?

A) UDP

B) ICMP

C) TCP

D) DNS

Answer: c

---

### 7. Which port is commonly used by SSH?

A) 21

B) 22

C) 53

D) 80

Answer: b

---

### 8. Which port is commonly used by HTTPS?

A) 80

B) 22

C) 443

D) 53

Answer: c

---

# Task 1 — Task Manager

# Windows Task Manager

---

## Multiple Choice

### What is Task Manager primarily used for?

A) Editing system files

B) Viewing and managing running processes and system performance

C) Installing Windows

D) Managing DNS records

Answer: b

---

### Which tab shows CPU, RAM, disk, and network usage?

A) Startup

B) Users

C) Performance

D) Details

Answer: c

---

### Which tab shows programs that run when Windows starts?

A) Startup

B) Performance

C) Users

D) Services

Answer: a

---

### Which tab provides detailed information about individual processes?

A) Startup

B) Details

C) Performance

D) App History

Answer: b

---

## Short Answer

### What is a process?
A process is an executing program that serves as an isolated for code, memory, and system resources. Basically a running instance of a program is a process. 

---

### What information can Task Manager provide?
Task Manager can provide information on computer performance, running software, and system resources. 

---

### Why is Task Manager useful?
Task manager is useful because it not only lets you see all the processes on your computer, but it lets you manage them aswell, allowing you to optimize performance, troubleshoot issues, and maintain system security. 

---

# Process Exploration

Open:

```text
Task Manager
    #This tool allows you to see monitor and manage processes on your system. 
```

Explore:

- Processes
- Performance
- Startup
- Details

Spend a few minutes looking around each section.

---

## Processes Tab

### Which process was using the most RAM?
The process that was using the most RAM was the Antimalware Service Executable. 

---

### Approximately how much RAM was it using?
It was using around 225-250 MB of RAM. 

---

### Which process was using the most CPU?
The process that was using the most CPU was Service Host: Windows Update, though Task Manager itself took the top spot once or twice itself. 

---

### Approximately how much CPU was it using?
It was using around 5-20% of the CPU.

---

## Performance Tab

### What information was displayed?
The Performance tab had four different sections, being CPU, Memory, Disk 0 (C:), and Ethernet. 

---

### How much RAM is installed on your VM?
There is around 6.1 GB of ram installed on my VM, and it was using around 2.1-2.8 GB of it at a time. 

---

### What was your CPU utilization approximately?
The CPU utilization seemed to jump all over the place, but it was usually around 20-60%. 

---

## Startup Tab

### How many startup applications were enabled?
There were only 3 startup applications enabled, being Microsoft Edge, Microsoft OneDrive, and Windows Security notifications. 

---

### Did any startup applications surprise you?
None of the startup applications surprised me, as they all make sense to some degree why they would be startup applications. 

---

## Details Tab

### What information did the Details tab provide?
The Details tab provided information about processes on the system, which are as follows: 
    Name
    PID
    Status
    User name
    CPU
    Memory
    Architechure
    Description
Under each of the columns, it provided a brief description of what they meant. 

---

# In Your Own Words

### Explain Task Manager to a beginner.
Task Manager is a tool for Windows systems that allows you to monitor and manage processes that are happening on the system. It gives you different tabs you can view to manage these processes, such the Performance tab and the Startup apps tab. It is an important tool on the Windows system.

---

# Task 2 — Windows Services

# Services

---

## Multiple Choice

### What is a Windows service?

A) A type of user account

B) A background process that performs system functions

C) A network cable

D) A file type

Answer: b

---

### Which tool is commonly used to manage Windows services?

A) Task Manager

B) services.msc

C) ipconfig

D) cmd

Answer: b

---

## Short Answer

### What is a Windows service?
A Windows service is a long-running executable application that operates in the background of the Windows os, designed to perform specific functions without requiring user intervention. 

---

### Why are services important?
Services are important in Windows because they enable long-running background processes that can operate independently of user sessions, allowing for the os to remain stable and functional at all times. 

---

# Services Exploration

Open:

```text
services.msc
    #This tool allows you to monitor and manage services on your Windows system. 
```

Explore:

- Running services
- Stopped services
- Startup types

---

## Running Services

### Name three running services you found.

1. Application Identity

2. Application Information

3. AppX Deployment Service (AppXSVC)

---

## Stopped Services

### Name three stopped services you found.

1. App Readiness

2. AVCTP service

3. BranchCache

Note: On the status column, no services said "Stopped", so I chose ones that were blank (which when I looked it up, means not running).

---

# Startup Types

## Multiple Choice

### Which startup type starts automatically when Windows boots?

A) Disabled

B) Manual

C) Automatic

Answer: c

---

### Which startup type starts only when needed?

A) Automatic

B) Manual

C) Disabled

Answer: b

---

### Which startup type prevents a service from starting?

A) Automatic

B) Manual

C) Disabled

Answer: c

---

## Short Answer

### Why might an administrator disable a service?
An administrator may disable a service on the system for a multitude of reasons, like to troubleshoot an issue, to enhance security, reduce resource footprint, or boost OS performance overall. 

---

### Why might a service be set to Manual instead of Automatic?
A service might be set to manual to reduce resource consumption, as some services can weigh the whole system down if left on all the time. Another reason the service might be set to manual is to help system performance, allowing for it to run smoother. 
Note: Manual doesn't necessarily improve performance directly. The bigger reason is that some services only start when another program actually needs it. (Graded)

---

# Observation Questions

### Which service seemed most important?
There was not one service I saw as most important, but the security services seemed more important than some others. 

---

### Which service name was the most confusing?
I would say DevQuery Background Discovery Broker seemed like one that is pretty complicated for me at the moment. 

---

### Did you notice any services related to networking?

A) Yes

B) No

Answer: a

---

### If yes, which ones?
The services related to networking (at least in the name) are as follows:
    Network Connected Devices Auto-Setup
    Network Connection Broker
    Network Connections
    Network Connectivity Assistant
    Network List Service
    Network Location Awareness
    Network Setup Service
    Network Store Interface Service
There were probably more networking related service on the system with specific names, but those are the main ones I noticed. 

---

# In Your Own Words

### Explain what a Windows service is to a beginner.
A Windows service is a program that operates in the background of the Windows system, not requiring user input of any kind. 

---
