# creating-a-backdoor-with-SET
creating a backdoor with SET - Ethical Hacking Techniques course

# AIM:
To Create a backdoor with Social Engineering Toolkit (SET)

## DESIGN STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode


### Step 2:

Investigate on the various categories of tools as follows:

### Step 3:

Open terminal and try execute some kali linux commands

### Architecture Diagram

```
+----------------+        +------------------------+        +----------------------+
| Attacker's PC  | -----> | SET (Credential        | -----> | Fake Login Page      |
| (Kali Linux)   |        | Harvester via Apache)  |        | (Hosted by SET)      |
+----------------+        +------------------------+        +----------------------+
       |                                                             |
       |                                                             v
       |   1. Configure SET with phishing site (e.g., Gmail clone)   |
       |                                                             |
       |                                                             v
       |                                                 +----------------------+
       |                                                 | Victim's Browser     |
       | <------------------------------------------------| Clicks Phishing Link|
       |                                                 +----------------------+
       |                                                             |
       |                                                             v
       |     2. Victim Enters Credentials → Sent to SET/Attacker    |
       |                                                             |
       |                                                             v
       |                                                 +----------------------+
       |                                                 | Credentials Captured |
       |                                                 | in Apache log/SET DB |
       |                                                 +----------------------+

```

## EXECUTION STEPS AND ITS OUTPUT:
Social Engineering attacks are the various cons used by the hackers to trick people into providing sensitive data to the attackers.

**Steps to Use SET for Phishing (Credential Harvester Attack Method)**

**1. Open terminal:**
```bash
sudo setoolkit
```
<img width="238" height="95" alt="image" src="https://github.com/user-attachments/assets/b735f4e3-df4f-49db-afb0-a535f0d46fc3" />

**2. Navigate:**
```bash
1) Social-Engineering Attacks  
2) Website Attack Vectors  
3) Credential Harvester Attack Method  
```
<img width="957" height="1005" alt="image" src="https://github.com/user-attachments/assets/47c78205-944d-4c28-b4fd-c130ecd90e8a" />

**3. Enter your IP address as the attacker server.**
**4. Choose:**
```bash
2) Site Cloner
```
<img width="952" height="341" alt="image" src="https://github.com/user-attachments/assets/e18bd46e-cfc3-476e-8d00-1de044893dd0" />

**5. Enter the URL of the legitimate site ```(e.g., https://accounts.google.com)```**
<img width="955" height="1066" alt="image" src="https://github.com/user-attachments/assets/72364d29-9e19-418f-bea3-f7aacd38371a" />

**6. Send the generated link to the victim.**

**7. Once the victim logs in → their credentials are stored in:**
```bash
/var/www/html/
```
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/6cee4f39-5c9d-4249-b5d7-a0b4190ff338" />




## RESULT:
The Social Engineering Toolkit (SET) is used to create backdoor is  examined successfully
