# **Hosting a ReactJS Web Application on Your Computer**

This document provides a step-by-step guide for hosting a ReactJS web application on your computer and making it accessible from other devices on your network. It includes instructions for setting a static IP address, ensuring the port is open, and specific details for hosting on port 3001\.

## **1\. Hosting Your ReactJS Application**

1. 1\. Build Your React Application

Run the command:

npm run build

This will create a 'build' folder with optimized files.

2. 2\. Install a Local Web Server

Install 'serve' globally:

npm install \-g serve

3. 3\. Serve Your Application

Run the command to serve your application on the default port 3000:

serve \-s build

4. 4\. Find Your Computer’s Local IP Address

Windows: Open Command Prompt and type 'ipconfig'. Look for 'IPv4 Address'.

5. 5\. Make Sure the Port is Open

Windows:

Open 'Windows Defender Firewall' and go to 'Advanced settings'.

Click on 'Inbound Rules' and then 'New Rule…'.

Choose 'Port', then 'TCP', and enter 3000\.

Allow the connection and apply the rule.

6. 6\. Access the Application from Other Devices

Use the local IP address and port number in the format:

http://\<your-computer-ip\>:3000

## 

## **2\. Hosting on Port 3001**

7. 1\. Using 'serve' to Host on Port 3001

Run the command:

serve \-s build \-l 3001

Access the application with:

http://\<your-computer-ip\>:3001

## 

## **3\. Static IP Address Configuration**

8. 1\. Choosing an IP Address

Internal Network Range: 192.168.1.10, 192.168.1.50, etc.

External IP: Obtain from ISP (e.g., 203.0.113.10).

9. 2\. Configuring Static IP Address

Windows:

Open 'Network & Internet settings' \> 'Change adapter options'.

Right-click on your adapter, select 'Properties'.

Set 'Internet Protocol Version 4 (TCP/IPv4)' to use a static IP (e.g., 192.168.1.50).

10. 3\. For Production:

Internal Static IP Example: 192.168.1.10

External Static IP: Obtain from your ISP (e.g., 203.0.113.10).

Security Considerations: Ensure firewall rules and secure protocols are in place.

## 

## **Summary**

Internal Network: Use a static IP like 192.168.1.10.

External Network: Obtain a public IP from ISP and set up port forwarding.

Host on Port 3001: Use 'serve' with the '-l' flag.