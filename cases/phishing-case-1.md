 # Phishing case-1 Malicious attachement and URL analsysis.
 #Case overview
 A phishing email was analyzed to identify impersonation techniques , malicious infrastructure and file based thereats.
 In the investigation i mainly focused on extracting indicators of compromise(IOC) and assessing potential impact.
 #TOOLS USED
 CyberChef
 ANY.RUN
 Email Header Analysis
 #Evidence collected 
 An impersonated brand :NETFLIX
 Sender Domain:Netflix<JGQ47wazXe1xYVBrkeDg-JODDwW@JOgDDQwWdR-yVkCaBkTNp.gogolecloud.com>
 Originating IP:209[.]85[.]167[.]226
 Defanged Domain :etekno[.]xyz
 Defanged URL:hxxps[://]t[.]co/yuxfZm8KPg?==1

 #File indicators

File name:Pyament-updatedid.pdf
File type:PDF
SHA-256:cc6f1a04b10bcb168aeec8d870b97bd7c20fc161e8310b5bce1af8ed420e20e2c24
#Behavioral Analysis 
Network activity :Suspicious Activity 
Suspicious Windows Processes:svchost.exe
Malicious Ip Domains:2.16.107.24,2.16.107.49
#Technique identified 
The attachment uses social engineering to encourage user interaction,triggering embedded content that initiates outbond network.
#Analyst Decision
The severenity level is high
This phishing attempt demonstrates malicious intent through a weaponised attachment and confirmed communication.
#Lessons Learned 
Using Sandbosing and defanging tools improved my ability to safetly analyze malicious infrastructure without risking system exposure
