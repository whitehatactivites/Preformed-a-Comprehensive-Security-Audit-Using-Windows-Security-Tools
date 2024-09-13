# Preformed-a-Comprehensive-Security-Audit-Using-Windows-Security-Tools

## 1. System Information Gathering
### System information gathering is essential for establishing a comprehensive overview of a system's hardware and software configuration, enabling effective management, troubleshooting, and security assessment. I used msinfo32 in command promt to gather details about the systems hardware and software
![msinfo](https://github.com/user-attachments/assets/25ae7f69-445e-4008-bd91-6ff853d8aa69)
#### I then was able to retrieve  more information regarding my computer, such as the OS Name, System Manufacturer, System Model, System Type, Processor, and Memory
![msinfo322](https://github.com/user-attachments/assets/66760768-d537-4c1a-aec0-dcf09d5cdcc2)

## 2. Windows Security Settings Review
### Reviewing Windows Security Settings is a crucial part of a security audit to ensure that the built-in security features of the operating system are configured correctly and functioning optimally. This review helps identify any security misconfigurations or weaknesses that could expose the system to threats. Here I opened Windows Virus & Threat Protection and ran a scan
![Capture](https://github.com/user-attachments/assets/740728ef-f418-4191-8bbd-01640ae11d17)
### Here is the result of the scan
![numbe3](https://github.com/user-attachments/assets/dca09a49-70be-4930-a335-616f93975048)
### I then located the Windows Virust & Threat Protection histroy to review latest protection actions
![number4](https://github.com/user-attachments/assets/430140c0-c5ec-4547-b6dc-c031264360fa)

## 3. Event Log Analysis
### Event log analysis is crucial for detecting and investigating security incidents by providing detailed records of system activities, which helps identify unauthorized or suspicious activities early. Here, I was able to locate the the Security Windows Logs and the filter option
![n5](https://github.com/user-attachments/assets/a4b6502b-51e8-4d8a-8f19-0d7765927969)
### Using the Filter Current Log, I was able to customize logs within the past 7 days. I specfically looked for events regarding security, therfore I checked critical, warning, and error, as these have to do with security.
![neww](https://github.com/user-attachments/assets/5fbf5919-f223-4e08-b0a1-ef32a87893bc)
### Fortunately, I had no problems and no logs appeared. Refering back to the previous screenshot, I also learned that you could insert certain IDs in the "All Event IDs" section. Event IDs are used to filter spefici events, some examples include 4624 to check successful logon, 4625 to check failed logon, 4634 to check logoff, or 4719 to check if the system audit policy was changed

## 4. System Integrity Check
### The System Integrity Check is a vital part of a thorough security audit, designed to verify that the core operating system files remain intact and unaltered. This process is crucial for preserving system stability and security, as any corruption or tampering of these files can result in vulnerabilities, crashes, or other significant issues. I ran command prompt as administrator and ran sfc /scannow
![n7](https://github.com/user-attachments/assets/9c7e25ed-f799-47b0-b562-eac5ea7ca37a)
### The SFC tool will start scanning all protected system files for integrity violations. This process might take some time, depending on the system's performance and the number of files. Here was the result
![SFC](https://github.com/user-attachments/assets/b2f18e44-2778-42de-8b24-998a7c6dce16)
### Once the scan is complete, SFC will provide you with a message as seen above. "Windows Resource Protection did not find any integrity violations" means no issues were found, but this might not always be the case. SFC could also say any of the following messages: "Windows Resource Protection found corrupt files and successfully repaired them": This indicates that SFC found issues and repaired them, "Windows Resource Protection found corrupt files but was unable to fix some of them": Some files could not be repaired and further action might be needed, pr "Windows Resource Protection could not perform the requested operation": There was an issue running SFC, which might require additional troubleshooting

## 5. Check for Installed Updates and patches
### Regular updates are essential for maintaining system security, as they frequently contain patches for vulnerabilities that could be targeted by attackers. Keeping a system fully updated helps safeguard against threats and minimizes the risk of security breaches. The first thing I did was locate Windows Update and checked for updates
![windows portion](https://github.com/user-attachments/assets/7d2f41c1-a6be-4897-b46d-75625f456866)
### I then looked up previous Windows Update History
![windwosupdate](https://github.com/user-attachments/assets/9d373ef6-2596-49b1-a2cc-b76850db0fdb)
### Lastly, I located the Advanced Options to review all possible Update Options
![advanced options](https://github.com/user-attachments/assets/a145a78f-df5e-4412-ab57-24cf3b20c0d8)

## 6. Network Security Assessment
### A thorough security audit that focuses on assessing the security posture of the network infrastructure must include the Network Security Assessment. This evaluation assists in locating potential weak points, incorrect setups, and regions where network defenses need to be strengthened. To start, I opened Windows Defender Firewall and made sure both Firewalls were turned on for Private Networks and Public Networks
![firewall sssss](https://github.com/user-attachments/assets/4969433d-1aac-4a24-a6af-1bb81626cd16)
### I then clicked on advanced settings and checked the confirugation of inbound and outbound rules
![inbounrules](https://github.com/user-attachments/assets/0e90b657-e24c-4163-9060-26e6181442e3)
### Inbound Rules control incoming traffic to your system. Ensures that only necessary services are allowed through the firewall. Outbound Rules control outgoing traffic. Ensures that applications and services are not exposing sensitive data. Lastly for the Network Security Assessment, I used netstat -an to review open network ports and listening services
![netstattt](https://github.com/user-attachments/assets/230d952b-289e-4e28-805c-a95f1dac25d3)


