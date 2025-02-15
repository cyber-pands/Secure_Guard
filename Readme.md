# SecureGuard

SecureGuard is a Python-based program designed to provide essential cybersecurity features for Linux systems via the command line. It integrates multiple security tools for threat detection, vulnerability scanning, endpoint protection, data encryption, compliance management, user training, and incident response. SecureGuard is intended for small to medium-sized businesses seeking an all-in-one solution for cybersecurity on Linux systems.

# Summary

SecureGuard leverages popular open-source cybersecurity tools, making it a versatile and accessible security solution. This program is designed to run without a GUI, allowing for efficient operation directly from the terminal. Each security feature is encapsulated in a function that performs specific tasks, making it easy to maintain, extend, and adapt to new security requirements.

# Tools Overview

| Tool                | Functionality                                | Purpose in SecureGuard                                                       |
| :------------------ | :------------------------------------------- | :--------------------------------------------------------------------------- |
| OSSEC               | Host-based Intrusion Detection System (HIDS) | Detect and alert on    potential security threats by monitoring system logs. |
| OpenVAS             | Vulnerability Assessment System              | Identify and assess system vulnerabilities.                                  |
| ClamAV              | Antivirus and Malware Detection              | Scan the system for viruses and malicious software.                          |
| GnuPG               | Data Encryption and Decryption               | Encrypt sensitive files specified by the user.                               |
| Lynis               | Security Auditing and Compliance             | Perform system audits and assess compliance.                                 |
| mailutils           | Command-line Email Tool                      | Send training emails to educate users on phishing awareness.                 |
| subprocess (Python) | Standard Library for Command Execution       | Integrates security tools and executes their commands from within Python.    |

# Installation

To set up SecureGuard on your Linux system, follow these steps:

## 1. Clone the Repository

```
git clone https://github.com/cyberpands/SecureGuard.git
```
```
cd SecureGuard
```


## 2. Install Dependencies
SecureGuard relies on several Linux tools and packages. Install them with the following commands:
```
sudo apt update
```
```
sudo apt install ossec-hids openvas clamav gnupg lynis mailutils python3
```

### Note: python3 should be installed by default on most Linux systems. If not, install it with:
```
sudo apt install python3
```


## 3.	Set Up Tools
- **OSSEC**: OSSEC requires configuration for HIDS capabilities; follow OSSEC’s setup guide for any additional configurations.
- **OpenVAS**: OpenVAS requires an initial setup. Run sudo openvas-setup or refer to OpenVAS documentation for complete configuration.
- **ClamAV**: Update the virus definitions with sudo freshclam.
- **mailutils**: Ensure your system’s mail settings allow mailutils to send outgoing emails.

# Running SecureGuard

Once installed, you can run the program by executing:
```
python3 secureguard.py
```
The program will provide an interactive menu, allowing you to select from the following options:
1.	Threat Detection: Starts OSSEC for monitoring and analyzing system logs for suspicious activity.

2.	Vulnerability Scanning: Starts OpenVAS to assess vulnerabilities on the system.

3.	Endpoint Protection: Runs a ClamAV scan to detect any viruses or malware.

4.	Data Encryption: Encrypts user-specified files with GPG for data security.

5.	Compliance Management: Executes a Lynis audit to check for compliance and system security recommendations.

6.	User Training: Sends an email to educate users about phishing awareness.

7.	Incident Response Plan Generation: Generates an incident response plan template for handling security incidents.

# Conclusion

SecureGuard Cybersecurity offers an integrated solution for various cybersecurity needs on a Linux system. By combining powerful, open-source tools into a unified Python program, SecureGuard provides a convenient command-line interface for maintaining system security, auditing for vulnerabilities, and educating users about cybersecurity. This tool is highly customizable, allowing users to adapt it to their unique security requirements. SecureGuard is ideal for administrators seeking a cost-effective and comprehensive cybersecurity solution.