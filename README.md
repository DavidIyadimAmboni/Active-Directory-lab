# Active-Directory Homelab



<h1>Installing Active Directory on Windows Server on a Virtual
machine </h1>
This project demonstrates the step-by-step process of setting up Active Directory (AD) on Windows Server using VMware. The objective is to create a virtualized environment that emulates a real-world network scenario, enabling easier management and authentication of user accounts, computers, and resources.<br />

<h2>Video Demonstration</h2>

- ### [Installation and Setup of Active Directory](https://youtu.be/uE7lz4dbD74?si=3z_KaAZBnn5DBsng)
  
<h2>Environments and Technologies Used</h2>

- VMware (Virtual Machines)
-	Windows Server ISO File



<h2>Operating System Used </h2>

- Windows 10 (21H2)

# Lab Tutorial: Setting Up VPN in an Azure Virtual Machine

## Objective
The primary objective of this project is to establish a comprehensive understanding of how to implement Active Directory (AD) on a Windows Server within a virtualized environment using VMware. 

## Step-by-Step Guide

I. Installing Virtual Machine and setting up Windows Server
1. Download and Install VMware Workstation Pro from the link below.
https://www.vmware.com/products/desktop-hypervisor.html
2. Download Windows Server 2022 free license from the link below. Fill up and register for free
trial and Select English(United States) ISO downloads 64-bit edition.
https://info.microsoft.com/ww-landing-windows-server-2022.html
3. Open VMware Workstation Pro and click on Create a New Virtual Machine
4. Select the option "I will install the operating system later" and click Next
5. Select Microsoft Windows under Guest Operating System and select the version Windows
Server 2022 from the drop down box and click Next
6. Type in the name that you want for the virtual machine and click Next
7. Click Next for Specify Disk Capacity and click customize Hardware
8. Select New CD/DVD (SATA) and under Connection, select Use ISO image file and Browse to
where you have saved the Windows Server ISO that was downloaded earlier and click close.
9. Click Finish and Virtual Machine should now be created.
10. Right click the virtual machine and click Power ON
11. Click on the virtual machine and press any button to load the Windows Server.
12. Click on Next when the Windows Setup window opens with the Language to Install
13. Click on Install Now button
14. On the Windows Setup button, Select the second option "Windows Server 2022 Standard
Evaluation (Desktop Experience) and click Next
15. Check "I accept the license terms"
16. Select Custom: Install Windows only (advanced)
17. Click next on Drive Unallocated Space Window
18. Wait for the Server to finish installing
19. The Virtual Machine will restart on its own after installing and you can type in a password for
Admin
20. Windows Server is now ready and you should be able to login with the password you
provided

II. Installing Active Directory tools on the Windows Server
1. Log in to the Windows Server
2. Open Server Manager and on the top right, click on Manage
3. Select Add Roles and Features
4. Click Next on Before you begin window
5. Select Role-based or feature-based installation and click Next
6. Click Next for Server Selection
7. Select Active Directory Domain Services from the options and click on Add Features and
click Next
8. Keep clicking Next until you reach the confirmation page and click the Install button.
9. Wait for the Installation to finish and when it's finished, do not close the window yet
10. Click on Promote the server to a domain controller
11. Under Deployment Configuration window, select the Option Add a new forest and type in a
name in the Root domain name textbox (e.g eastcharmer.local) and click Next
12. Type the admin password and click Next and Next until you reach Prerequisites Check
Window
13. Once you see on top "All prerequisite checks passed successfully. " click the Install button
and wait for it to finish and the computer will restart
14. Log in to the Windows server and you will now see the new Domain name we created and
that means that Active Directory and Domain was successfully installed

## Understanding the Results

From this exercise, you can observe the following:

- When accessing the website from your actual PC without a VPN, it shows your original IP address and your city location.

- After connecting to the Azure virtual machine and accessing the website, a different IP address and the location of the virtual machine (e.g., Paris) are displayed.

- Finally, by connecting to the ProtonVPN server in Japan from within the virtual machine and accessing the website again, another IP address and the location of the VPN server (e.g., Tokyo, Japan) are shown.

This exercise demonstrates how VPNs work by encrypting and routing your internet traffic through remote servers, making it appear as if you are browsing from different locations. VPNs can enhance privacy, and security, and allow you to bypass geo-restrictions.
