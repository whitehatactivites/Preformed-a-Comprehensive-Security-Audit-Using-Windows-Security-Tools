# Preformed-a-Comprehensive-Security-Audit-Using-Windows-Security-Tools

## 1. System Information Gathering
### Used msinf32 in command promt to gather details about the systems hardware and software
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
### Fortunately, I had no problems and no logs appeared. Refering back to the previous screenshot, I also leanred that you could insert certain IDs in the "<All Event IDs>" section. Event IDs are used to filter spefici events, some examples include 4624 to check successful logon, 4625 to check failed logon, 4634 to check logoff, or 4719 to check if the system audit policy was changed

## 4. System Integrity Check

## 5. Check for Installed Updates and patches

## 6. Network Security Assessment

