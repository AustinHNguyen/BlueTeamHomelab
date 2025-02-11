# BlueTeamHomelab
Blue-team homelab built by Andrew and Austin Nguyen

<h3>Project:</h3> This repository is documentation of our homelab including the steps we took to implement features and build our homelab from the ground up. This project follows Corey Jones' Proxmox homelab series as a guide, but uses different hardware and different network setup.

Corey Jones' homelab series: https://medium.com/h7w/ultimate-cyber-security-home-lab-with-proxmox-part-1-setting-up-the-network-2f70c91606ff (Part 1)

<h3>Building:</h3> The very first thing we did was install the Proxmox OS on our two computers using Ventoy. After Proxmox was installed, we connected both machines to an Archer AX1800 router which is connected to our modem and provides internet access. We then connected an ethernet cable from the router to a separate computer to access the Proxmox Virtual Environment similar to what is shown in the picture below except that there were no VMs at the time and no network setup. We created an additional OVS bridge and modified vmbr0-2 with ips and also vlan ports for vmbr2 (Ignore vmbr3, that is for a different project). 

![image](https://github.com/user-attachments/assets/31c93c22-5c24-489c-9981-1ef8481a8a31)

pfSense: pfSense acts as our firewall and DHCP server. It allows us to control and configure firewall settings for more security.
![image](https://github.com/user-attachments/assets/9ce531e8-b1c1-4a7d-b491-9a46d85ab625)
The image above shows the ip ranges of the different VLANs

pfSense configurations:
Interface Assignments: 

![image](https://github.com/user-attachments/assets/c1a4d38e-e26a-416b-8b6a-ede2671c06ca)

LAN Rules: 

![image](https://github.com/user-attachments/assets/af2dcaa7-4cd5-4151-aa0b-50c64c6cb1b3)

DHCP Server enabled: 

VXLAN zone and VXNet created: 

![image](https://github.com/user-attachments/assets/99626f0d-dbcd-4b38-9e8a-4d8810c7b90b)
![image](https://github.com/user-attachments/assets/e34ccacf-be7a-4a71-8523-eeb16e97ffd8)

All Virtual Machines added and configured (Right side shows Windows 10 hardware configurations):

![image](https://github.com/user-attachments/assets/6e3fed58-b8e9-4dad-80b0-6b94a6daf4ae)
Note: Wazuh Agent was installed on the Windows 10 machine

Windows Server hardware configurations:

![image](https://github.com/user-attachments/assets/fe8cd100-f3f0-4ac0-aac1-37d240f49ba4)


Kali machine hardware configurations: 

![image](https://github.com/user-attachments/assets/30298857-487f-4334-a2d6-b924159fd7ce)

Docker and Portainer installed for vulnerable webapp testing:
![image](https://github.com/user-attachments/assets/817651c5-adc1-449f-beff-9172e000e025)
![image](https://github.com/user-attachments/assets/47d62d4d-4c51-4863-9f82-b481534f797f)

That is all for now for our homelab. We will be using this homelab in several future projects to further our knowledge and practice real-world skills. This will be expanded in the future as well to fit our educational needs.
