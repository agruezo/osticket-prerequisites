<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<!-- <h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com) -->

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Create Virtual Machine in Azure
- Install Web Platform Installer
- Install osTicket v1.15.8
- Install HeidiSQL

<h2>Installation Steps</h2>
<h3 align="center">Connect to your Virtual Machine with Remote Desktop</h3>
<br />
<br />
<h3 align="center">Install / Enable IIS in Windows</h3>
<br />
<br />
<h3 align="center">Install Web Platform Installer</h3>
<p>
  Open after installation:
</p>
<br />
<p>
  Add MySQL 5.5 (it will ask for credentials to be created later)
</p>
<p>
  Name: root
</p>
<p>
  Password: Password1:
</p>
<br />
<p>
  Add All simple versions of x86 PHP up until 7.3:
</p>
  Fix any failures if required 
Install PHP Version 7.3.8 (or any other version if necessary, archives)
Install PHP Manager 1.5.0 for IIS 10 (folder you unzipped on the desktop)
Install Microsoft Visual C++ 2009 Redistributable Package
<br />
<br />
<h3 align="center">Install osTicket v1.15.8</h3>
Download osTicket (download from within lab files: link)
Extract and copy the “upload” folder INTO c:\inetpub\wwwroot
Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”
<br />
<br />
<h3 align="center">Reload IIS (Open IIS, Stop and Start the server)</h3>
Go to sites -> Default -> osTicket
On the right, click “Browse *:80”
<br />
<br />
<h3 align="center">Enable Extensions in IIS: Note that some extensions are not enabled</h3>
Go back to IIS, sites -> Default -> osTicket
Double-click PHP Manager
Click “Enable or disable an extension”
Enable: php_imap.dll
Enable: php_intl.dll
Enable: php_opcache.dll
<br />
<br />
<h3 align="center">Refresh the osTicket site in your browser, observe the changes</h3>
<br />
<br />
<h3 align="center">Rename</h3>
From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
	To: C:\inetpub\wwwroot\osTicket\include\ost-config.php
<br />
<br />
<h3 align="center">Assign Permissions: ost-config.php</h3>
Disable inheritance -> Remove All
New Permissions -> Everyone -> All
<br />
<br />
<h3 align="center">Continue Setting up osTicket in the browser (click Continue)</h3>
Name Helpdesk
Default email (receives email from customers)
<br />
<br />
<h3 align="center">Download and Install HeidiSQL (download from within lab files: link)</h3>
Create a new session, root/Password1
Connect to the session
Create a database called “osTicket”
<br />
<br />
<h3 align="center">Continue Setting up osticket in the browser</h3>
<br />
<br />
<h3 align="center">MySQL Database: osTicket</h3>
MySQL Username: root
MySQL Password: Password1
<br />
<br />
<h3 align="center">Click “Install Now!”</h3>
<br />
<br />
<h3 align="center">Congratulations, hopefully it is installed with no errors!</h3>
<br />
<br />
<h3 align="center">Clean up</h3>
Delete: C:\inetpub\wwwroot\osTicket\setup
Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php
<br />
<br />
<h3 align="center">Login to the osTicket Admin Panel (http://localhost/osTicket/scp/login.php)</h3>
<br />
<br />
<!-- <p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
 -->
