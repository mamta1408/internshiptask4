# Task 4: Setup and Use a Firewall on Windows/Linux

## Objective
Configure and test basic firewall rules to allow or block traffic on specific ports. Learn how firewalls manage network traffic and protect your system.

## Tools
- Windows: Windows Defender Firewall
- Linux: UFW (Uncomplicated Firewall)

---

## Steps

### 1. Open Firewall Configuration Tool

#### Windows:
- Press `Win + R`, type `wf.msc`, and press Enter  
  or  
- Go to:  
  `Control Panel > System and Security > Windows Defender Firewall > Advanced Settings`
  
2. List Current Firewall Rules  
Windows:  

Open wf.msc  

Check Inbound Rules and Outbound Rules  

3. Add a Rule to Block Inbound Traffic on Port 23 (Telnet)  
Windows:  

Go to Inbound Rules, then New Rule  

Select Port, then TCP, and enter port 23  

Choose Block the connection  

Apply to Domain, Private, Public  

Name it: Block Telnet Port 23  

4. Test the Rule  

Try connecting to port 23:  

telnet 127.0.0.1 23  

Expected Output:  

Connecting to 127.0.0.1...  
Could not open connection to the host on port 23: Connect failed  

Summary: How Firewalls Filter Traffic  

A firewall controls network traffic based on user-defined security rules.  

Inbound Rules control traffic coming into the system.  

Outbound Rules control traffic leaving the system.  

Rules are based on:  

- Port numbers (e.g., 22 for SSH, 23 for Telnet)  
- Protocols (TCP/UDP)  
- Applications  
- IP addresses  

Actions:  

Allow means permit traffic through.  

Block means deny traffic access.  

Profiles:  

Domain is for networks in an Active Directory environment.  
Private is for trusted home networks.  
Public is for untrusted networks (e.g., public Wi-Fi).  
