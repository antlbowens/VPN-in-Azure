<p align="center">
  <a href="https://imgur.com/a/cbc7MMA">
    <img src="https://github.com/user-attachments/assets/48fef006-cc54-40b2-9102-04f03d0a200e" alt="VPN Lab Screenshot" width="200"/>
  </a>
</p>

# VPN-inside-Azure💻
This lab demonstrates how VPNs can alter perceived geolocation and mask public IP addresses by deploying and interacting with a Windows 10 Virtual Machine in Microsoft Azure. The objective is to understand how VPNs route internet traffic through remote servers and how this affects internet behavior and content localization.

It also introduces the concept of dual tunneling—using both a virtual machine and a VPN—which adds an extra layer of privacy and complexity. This setup makes it more difficult to trace the user's actual location or IP address, reinforcing secure browsing and identity protection for educational purposes.

# Environments and Technologies Used

- <a href="https://portal.azure.com">Microsoft Azure (Virtual Machines/Compute)
- <a href="https://support.microsoft.com/en-us/windows/how-to-use-remote-desktop-5fe128d5-8fb1-7a23-3b8a-41e636865e8c"> Remote Desktop 
- <a href="https://protonvpn.com/?srsltid=AfmBOoqUOS9Uj_d1yaxiPwv5WvtT5detrlxmfYIXiuNGx8E1rA6pyjDk">Proton VPN Free Version (Virtual Private Network)
- <a href="https://whatismyipaddress.com/">Whatismyipadress

# Operating Systems Used 

- Windows 10 (21H2)

# Overview of Deployment and Phases

- Phase 1
- Phase 2
- Phase 3
- Phase 4
- Phase 5
- Phase 6

  # Deployment and Phases

## Phase 1

Use [WhatIsMyIPAddress](https://whatismyipaddress.com/) to identify your current IP address. This will help you compare it later when connected to a VPN. It's also a good idea to write it down for reference. I would demonstrate myself but, I wouldn't want to accidentally leak my info to anyone.

## Phase 2

create a VPN account using [ProtonVPN](https://protonvpn.com/) before setting up your virtual machine. Be sure to use the free version of ProtonVPN. Also, write down your username and password so you can easily sign in once you're inside the virtual machine.

## Phase 3

Create a virtual machine and resource group in [Azure](https://portal.azure.com). You can name the VM and resource group whatever you like. Make sure to select Windows 10 Pro (22H2) as the operating system, and under the Size section, choose a configuration with 2 vCPUs and at least 8 GiB of RAM. Your VM settings should match or closely resemble mine.
![image](https://github.com/user-attachments/assets/c14be7a8-017e-4e8a-8932-bb618f01f3ce)
![image](https://github.com/user-attachments/assets/dee85fee-0480-484f-bf96-97b2ce626d1d)

## Phase 4

Connect to your VM using RDP (Remote Desktop Protocol). Open the Remote Desktop app by searching for it in the Windows search bar. When connecting, make sure to enter the public IP address of your virtual machine. Also, have your VM username and password saved in Notepad or written down, so you can log in without issues. The underlined red should go into the portion that is underlined green, click connect and boom your there. Also a pop up may come up just select yes and never show again.
![Screenshot 2025-05-18 194848](https://github.com/user-attachments/assets/8cc9cba3-bc1d-47eb-8874-efb795832db5)

## Phase 5

Once you're inside your virtual machine, open Microsoft Edge and download ProtonVPN. After installing it, log in to your account and connect to a server. The specific server location may vary—for example, I was assigned a U.S. server, but yours might be different. Below is an example of what the ProtonVPN app should look like once connected.
![Screenshot 2025-05-18 200505](https://github.com/user-attachments/assets/cb90b62d-77d7-4574-a5b5-65b8f2f2f8be)

## Phase 6

Open a new browser tab and go to [WhatIsMyIPAddress](https://whatismyipaddress.com/) to verify your new IP address while connected to the VPN on your virtual machine. You might see an IP from a different country—for example, mine showed a U.S. location (Miami) even though I'm in South Carolina. If you’re routed through another country, try visiting websites like Google or Disney—you might notice the language or content changes based on your virtual location, which is pretty interesting!ng.
![Screenshot 2025-05-18 200530](https://github.com/user-attachments/assets/d7e08c16-772c-4dd4-ba02-381821636e32)



