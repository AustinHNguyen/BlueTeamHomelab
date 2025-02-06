# BlueTeamHomelab
Blue-team homelab built by Andrew and Austin Nguyen

Project: This repository is documentation of our homelab including the steps we took to implement features and build our homelab from the ground up. This project follows Corey Jones' Proxmox homelab series as a guide, but uses different hardware and different network setup.

Corey Jones' homelab series: https://medium.com/h7w/ultimate-cyber-security-home-lab-with-proxmox-part-1-setting-up-the-network-2f70c91606ff (Part 1)

Setup: The very first thing we did was install the Proxmox OS on our two computers using Ventoy. After Proxmox was installed, we connected both machines to an Archer AX1800 router which is connected to our modem and provides internet access. We then connected an ethernet cable from the router to a separate computer to access the Proxmox Virtual Environment similar to what is shown in the picture below except that there were no VMs at the time and no network setup. We created an additional OVS bridge and modified vmbr0-2 with ips and also vlan ports for vmbr2 (Ignore vmbr3, that is for a different project). 

![image](https://github.com/user-attachments/assets/31c93c22-5c24-489c-9981-1ef8481a8a31)

pfSense: pfSense acts as our firewall and DHCP server. It allows us to control and configure firewall settings for more security.
![image](https://github.com/user-attachments/assets/9ce531e8-b1c1-4a7d-b491-9a46d85ab625)
