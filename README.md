# 🛡️ Configuring VPN Lab

In this lab, I configured a secure VPN connection in Windows using the built‑in VPN client. The goal was to create a reliable remote‑access connection for users who need to securely reach internal network resources. This included selecting the appropriate tunneling protocol, configuring authentication, and customizing the connection for a Windows‑based environment.

## 🧠 Skills Demonstrated
- VPN configuration in Windows  
- Understanding of tunneling protocols (SSTP)  
- Knowledge of SSL/TLS‑based VPN transport  
- Authentication configuration using EAP‑MSCHAPv2  
- Remote access setup using public IP endpoints  
- Windows networking and security fundamentals  

## 🧑‍💻 About This Lab
I created a new VPN connection in Windows and named it **SalesVPN** to reflect its purpose for remote sales staff. Remote users connect to the VPN server using the organization’s public IP address **198.10.20.12**, which serves as the remote access endpoint.

For the VPN type, I selected **Secure Socket Tunneling Protocol (SSTP)**. SSTP encapsulates PPP traffic inside an SSL/TLS channel over **port 443**, allowing the VPN to pass through most firewalls and NAT devices without requiring special configuration. This makes SSTP a strong choice for environments where users connect from various networks with unknown restrictions.

## 🔐 Authentication Method
In the VPN properties, I configured the authentication method to use **Microsoft Secured Password (EAP‑MSCHAPv2)**.

I selected EAP‑MSCHAPv2 because:

- It is the standard password‑based authentication method supported by SSTP  
- It integrates cleanly with Windows environments  
- It works seamlessly with **Active Directory** and **Network Policy Server (NPS)**  
- It operates securely inside SSTP’s TLS‑encrypted tunnel  

This combination provides a secure and manageable authentication workflow for remote users.

## 🛠️ Tools Used
- Windows 10 / Windows 11 built‑in VPN client  
- Network & Internet Settings  
- VPN Properties & Authentication Settings  

## 📝 Steps Performed
- Opened Windows VPN settings and created a new VPN connection  
- Entered the public IP address **198.10.20.12** as the server name  
- Renamed the connection to **SalesVPN**  
- Selected **SSTP** as the VPN type  
- Configured authentication to use **EAP‑MSCHAPv2**  
- Saved and reviewed the connection properties
  
## 📸 Screenshots
Screenshots in this repository show:

- No-VPNs-configured — the starting point before adding any connections
- Creating-the-new-VPN - VPN connection and naming it SalesVPN
- Editing-the-SalesVPN-properties - Configuring EAP‑MSCHAPv2 authentication
- Successful-VPN-connection, confirming that the configuration works
 
## 📂 Repository Structure
Configuring-VPN-LLab/  
- Screenshots/  
  - vpn-setup.png  
  - vpn-properties.png  
  - vpn-authentication.png  
- README.md  

