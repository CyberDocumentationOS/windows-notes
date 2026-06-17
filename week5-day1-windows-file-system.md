# Day 1 — Windows File System

## Warm-Up — Multiple Choice Review

Try these WITHOUT notes.

---

### 1. Which permission string represents `chmod 755`?

A) rw-r--r--  
B) rwxrwxrwx  
C) rwxr-xr-x  
D) rwx------

Answer: c

---

### 2. Which command shows the groups a user belongs to?

A) chmod  
B) groups  
C) pwd  
D) touch

Answer: b

---

### 3. What is the primary purpose of an IP address?

A) Store files

B) Identify a device on a network

C) Identify a MAC address

D) Assign permissions

Answer: b

---

### 4. What does DNS do?

A) Assigns IP addresses

B) Encrypts web traffic

C) Translates domain names into IP addresses

D) Routes packets

Answer: c

---

### 5. What does DHCP do?

A) Resolves domain names

B) Assigns IP addresses automatically

C) Encrypts traffic

D) Stores MAC addresses

Answer: b
---

### 6. Which protocol is connection-oriented?

A) UDP

B) ICMP

C) TCP

D) DNS

Answer: c

---

### 7. Which protocol is generally faster because it does not retransmit lost packets?

A) TCP

B) UDP

C) HTTP

D) HTTPS

Answer: b

---

### 8. Which port is commonly used by SSH?

A) 20

B) 21

C) 22

D) 443

Answer: c

---

### 9. Which port is commonly used by HTTPS?

A) 22

B) 53

C) 80

D) 443

Answer: d

---

### 10. What protocol does ping primarily use?

A) TCP

B) UDP

C) ICMP

D) HTTP

Answer: c

---

# Task 1 — Windows Drives & File Structure

# Windows File System

---

## Multiple Choice

### What is the primary drive letter used by Windows?

A) A:

B) B:

C) C:

D) Z:

Answer: c

---

### Which folder contains most Windows operating system files?

A) Users

B) Program Files

C) Windows

D) Downloads

Answer: c

---

### Which folder contains user profiles?

A) Users

B) System32

C) Program Files

D) Temp

Answer: a

---

## Short Answer

### What is the purpose of the C: drive?
The purpose of the C: drive is to store the operating system, system files, and installed programs, essentially acting as the central location for booting and daily operations. 

---

### What is stored inside the Windows folder?
The Windows folder contains the core files and system directories, which are required for the system to run. 


---

### What is stored inside the Users folder?
The Users folder contains mainly stores personal data, settings, and app configurations for every user account on the system. 

---

# Major Windows Directories

## Fill In The Blanks

### Program Files

Purpose:
The Program Files folder is usually where third-party applications are typically installed. 


---

### Program Files (x86)

Purpose:
The Progam Files (x86) folder is specifically meant for installing and storing 32 bit applications on a 64 bit operating system. This is mainly done to seperate the the different types of programs in order for there to be no conflicts between the software architectures. 

---

### Windows

Purpose:
The Windows folder is the central repository for all files and resources required for the system to function. 


---

### System32

Purpose:
The System32 folder is where the core system files, drivers, and dynamic link libraries (DLLs) required for the OS to function are stored. 


---

### Users

Purpose:
The Users folder is where all the user-specific data, settings, and application configurations for every account on the system are stored. 

---

## Multiple Choice

### What is System32 primarily used for?

A) Storing personal documents

B) Storing Windows system files and utilities

C) Storing games

D) Storing internet history

Answer: b

---

### Which folder typically contains 64-bit applications?

A) Program Files

B) Program Files (x86)

Answer: a

---

### Which folder typically contains 32-bit applications?

A) Program Files

B) Program Files (x86)

Answer: b

---

## Short Answer

### What is the difference between Program Files and Program Files (x86)?
The Program Files folder is meant for 64 bit applications, while the Program Files (x86) folder is meant for 32 bit applications. This is done to prevent conflicts with different software architecture.



---

### Why is System32 important?
The System32 folder is important because it is where the core system files, drivers, and dynamic link libraries that are required for the system to function are stored. Without that folder, those items would either be scattered around random inconvient places, or the system would not function. 

---

# In Your Own Words

### Explain the purpose of the C: drive to a beginner.
The purpose of the C: drive is to store the operating system, the system files, and any installed programs on the system, essentially acting as the home directory for Windows. 
Note: C:\ is more like the root filesystem rather than a home directory. (Graded)

---

### Explain what the Users folder is used for.
The Users folder is for storing user-specific data, settings, and application configurations for every user on the system. 


---

### Explain why System32 is one of the most important folders in Windows.
System32 is one the most important folder in Windows because it contains all the items needed for the system to function. Without it, the system would not be able to function. 


---

# Task 2 — Explore the File System

Open and explore:

```text
C:\Users
C:\Windows
C:\Windows\System32
C:\Program Files
```

Take a few minutes to click through each folder.

---

# Directory Exploration

## C:\Users

### What did you notice inside this folder?
I noticed it had a folder named public, a folder named after the dummy user I set up, and a folder called defaultuser0 that I needed special access to use. 

---

## C:\Windows

### What did you notice inside this folder?
Inside this folder was a lot of folders that relate to the os, including system32, which is one that was touched on earlier. 

---

## C:\Windows\System32

### What did you notice inside this folder?
Inside this folder, I found tons of core system items. When I opened the file comctl32.dll.mui from the ka-GE folder, I couldn't understand anything inside it, as it was too complex for me. 

---

## C:\Program Files

### What did you notice inside this folder?
In this folder, I noticed that all the default windows apps are installed here, like Internet Explorer and Windows Defender. Windows PowerShell was present as well, which is something that I am probably going to learn about when I get to active directory. 
Note: Many installed applications and Windows components are located here. (Graded)


---

# Questions

### Which folder seemed largest?
The Windows folder definitely seemed the largest, as since it contains all the stuff necessary to run the OS, that is probably why. 


---

### Which folder would you avoid deleting files from?
I would avoid deleting files from the Windows folder (system32 too but it is in the Windows folder), as everything in there is required for making sure the OS can run. 

---

### Why is System32 important?
System32 is important because it contains all the items needed for the system to function, as without it, the system wouldn't be able to. 


---

# Major Directory Summary

| Directory | Purpose |
|------------|------------|
| C:\Users | User data |
| C:\Windows | OS items |
| C:\Windows\System32 | Core System items |
| C:\Program Files | 64-bit applications |
| C:\Program Files (x86) | 32-bit applications |

---

# Interesting Observations

### What was the most surprising thing you found?
The most surprising thing I found is that system32 is a subfolder under the Windows folder. For some reason, that didn't cross my mind. 


---

### What directory seemed the most important?
The Windows and system32 directories are definitely the most important, as they are needed to run the system. 


---

### What directory would be the most dangerous to modify?
The most dangerous directory to modify would be the system32 directory, as it could halt the functionality of the system. 


---

# Reflection

### Which Windows directory was easiest to understand?
I would say the Users directory was the easiest to understand, as it seems pretty straight forward. 


---

### Which Windows directory was most confusing?
I would say the Program Files (x86) was the most confusing (even though it was not that hard to understand), as I wouldn't have guessed that it was meant for 32-bit applications.


---

### In one sentence, explain how the Windows file system is organized.
The Windows file system is organized in a tree like structure, starting with the C:\ drive and working down to other directories like the Windows and Program Files directories. 


---