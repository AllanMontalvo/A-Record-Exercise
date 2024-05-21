<h1>A-Record Exercise</h1>
This tutorial outlines the creation of an A-Record.<br />

<h2>Prerequisite</h2>
In this project, you should have created a server and a client connected within the same network. If you have not done so, please use this link to take you to <a href="https://github.com/AllanMontalvo/Virtualbox-Active-Directory">Configuring On-premises Active Directory</a> to create your small network and begin this project.


<h2>Environments and Technologies Used</h2>

**Technologies and Servies**
- Oracle VM VirtualBox
- DNS Manager
- Command Prompt

**Environment/Operating System**
- Windows Server 2022
- Windows 10

<h2>High-Level Deployment and Configuration Steps</h2>

**Step 1: Ping an A-Record**
- Log in to Client-1 as an admin (mydomain\jane.admin)
- Open cmd prompt and ping “mainframe”
- Type nslookup “mainframe” and will fail.
<p>
  <img src="https://github.com/AllanMontalvo/A-Record-Exercise/assets/135927674/af1aada6-ac67-4005-84e4-fea96ea868c1" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

**Step 2: Create an A-Record**
- Log into DC-1 as domain admin (mydomain\jane.admin).
- Open Server Manager and open DNS under Tools.
- On the left column select DC-1, then Forward Lookup Zones, then mydomain.net.
- Right-click the left column and select “New Host (A or AAA).
- Create the name “mainframe” and your IP address be server (10.1.10.2).
<p> 
  <img src="https://github.com/AllanMontalvo/A-Record-Exercise/assets/135927674/8ebdb4b7-bec0-4aa6-b392-0e480e2d4a20" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

**Step 3: Verify A-Record**
- In Client-1, open cmd prompt.
- Type "ping mainframe"
<p>
  <img src="https://github.com/AllanMontalvo/A-Record-Exercise/assets/135927674/f2ba9622-79d8-4ebb-b57b-d6891ba8a513" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>


<h2>Final Notes</h2>
In conclusion, this project outlines the creation and implementation of an A-Record (Address Record). This exercise has underscored the importance of directing users to the correct location using memorable domain names instead of numerical IP addresses. For instance, remembering and accurately typing an IP address like 20.203.50.157 can be challenging for users. However, by creating an A-Record named "Project A" that points to this IP address, users can easily recall and access the resource. This project has demonstrated how A-Records enhance user experience and streamline web navigation.
