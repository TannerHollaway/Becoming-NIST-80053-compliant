# Becoming-NIST-80053-compliant. This one's a long one!

Security Posture Improvement and Compliance Implementation:

Building on the honeynet developed in previous labs, I focused on enhancing the security posture of the environment by addressing specific recommendations from Microsoft Defender for Cloud (MDC) and aligning with NIST 800-53 security controls. Initially, the environment's security score was assessed at 55%. My goal was to implement three key recommendations from MDC and observe the subsequent impact on the overall security score.

<p align="center">
<img src="https://github.com/user-attachments/assets/fd15f20d-430e-4233-ad11-1500434201e3"height="80%" width="50%" alt="NSGALLOW"/>

Implementation of NIST 800-53 Security Controls:

Before addressing the MDC recommendations, I incorporated additional security controls from NIST 800-53. For demonstration purposes, I focused on three core areas: Virtual Machines, Key Vault, and Storage Accounts.

<p align="center">
<img src="https://github.com/user-attachments/assets/42534344-5612-4fc2-b7f6-5b66533cb99b"height="80%" width="80%" alt="NSGALLOW"/>

Virtual Machines Hardening: I restricted all inbound and outbound traffic to the virtual machines, permitting only access from my trusted IP address. This ensured that the virtual machines were isolated from unauthorized external traffic.

<p align="center">
<img src="https://github.com/user-attachments/assets/8192ba29-08b4-4400-b60c-46f604b1c3c0"height="80%" width="50%" alt="NSGALLOW"/>

Key Vault Configuration: I enhanced the security of the Key Vault by removing public internet access and integrating it into a private virtual network. This step mitigated the risk of unauthorized access by restricting the Key Vault to a secure, internal environment 

<p align="center">
<img src="https://github.com/user-attachments/assets/9efabd3d-4ed2-415b-9cf9-6488a8aacd5c"height="80%" width="80%" alt="NSGALLOW"/>
<p align="center">
<img src="https://github.com/user-attachments/assets/16422d09-2052-47d1-a6df-f147ac14a2b1"height="80%" width="50%" alt="NSGALLOW"/>

Storage Account Protection: Similarly, I removed public access to the Storage Account and added it to a private subnet within the virtual network, ensuring that it is accessible only from within the secure environment.
<p align="center">
<img src="https://github.com/user-attachments/assets/4135bc22-633c-4d87-a58f-b7e7a33efdfa"height="80%" width="80%" alt="NSGALLOW"/>
<p align="center">
<img src="https://github.com/user-attachments/assets/78f0cb32-f34d-435b-8588-9b1362b82b62"height="80%" width="50%" alt="NSGALLOW"/>

By implementing these measures, both the Key Vault and Blob Storage were securely integrated into the private network.

<p align="center">
<img src="https://github.com/user-attachments/assets/e261adcf-8e86-4c1a-a2f5-9e6ab4ff7b3a"height="80%" width="50%" alt="NSGALLOW"/>

Verification and Troubleshooting

After configuring the private endpoints, I logged into the Windows VM to verify connectivity using the nslookup command. Initially, the lookup failed due to an incorrect URL format. After troubleshooting and correcting the issue by removing the HTTPS prefix and slashes, the connectivity was successfully verified, confirming that the private endpoints were functioning as intended (screenshot).
<p align="center">
<img src="https://github.com/user-attachments/assets/fd77a385-f779-49f5-b357-0c42e7b90b1f"height="80%" width="80%" alt="NSGALLOW"/>
<p align="center">
<img src="https://github.com/user-attachments/assets/a802a385-f9a9-4837-a3e6-3ec9bb94caa1"height="80%" width="80%" alt="NSGALLOW"/>

Attaching a Network Security Group (NSG)

To further enhance security, I attached a Network Security Group (NSG) to the subnet. This additional layer of security enforced strict traffic controls at the network level, contributing to the overall hardening of the environment.

<p align="center">
<img src="https://github.com/user-attachments/assets/cf7fddd6-ebe3-4f7e-8cca-ea42957da313"height="80%" width="80%" alt="NSGALLOW"/>
<p align="center">
<img src="https://github.com/user-attachments/assets/05845140-be88-462d-a84d-660f70836559"height="80%" width="80%" alt="NSGALLOW"/>

Final Assessment and Results

After completing the recommended hardening steps and aligning the environment with both MDC and NIST 800-53 controls, I re-assessed the security posture. Following a 24-hour observation period, the security score showed a significant improvement, reflecting the effectiveness of the implemented measures.

<p align="center">
<img src="https://github.com/user-attachments/assets/8725f0b6-a6a9-4d85-b96d-dc7bf62f1788"height="80%" width="50%" alt="NSGALLOW"/>


