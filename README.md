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
<p>
	<img src="https://i.imgur.com/DJmEXEB.png" height="75%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<br />
<br />
<h3 align="center">Install / Enable IIS in Windows</h3>
<br />
<p>
	<img src="https://i.imgur.com/DJmEXEB.png" height="75%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<br />
<br />
<h3 align="center">Install Web Platform Installer</h3>
<br />
<p>
  Open after installation:
</p>
<p>
	<img src="https://i.imgur.com/DJmEXEB.png" height="75%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<br />
<p>
  Add MySQL 5.5 (it will ask for credentials to be created later).
</p>
<p>
  Name: root
</p>
<p>
  Password: Password1:
</p>
<p>
	<img src="https://i.imgur.com/DJmEXEB.png" height="75%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<p>
  Add All simple versions of x86 PHP up until 7.3:
</p>
<p>
	<img src="https://i.imgur.com/DJmEXEB.png" height="75%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<p>
  Fix any failures if required. 
</p>
<p>
  Install PHP Version 7.3.8 (or any other version if necessary, archives).
</p>
<p>
  Install PHP Manager 1.5.0 for IIS 10 (folder you unzipped on the desktop).
</p>
<p>
  Install Microsoft Visual C++ 2009 Redistributable Package:
</p>
<p>
	<img src="https://i.imgur.com/DJmEXEB.png" height="75%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<br />
<br />
<h3 align="center">Install osTicket v1.15.8</h3>
<br />
<p>
  Download osTicket (download from within lab files: link).
</p>
<p>
	Extract and copy the “upload” folder INTO c:\inetpub\wwwroot.
</p>
	Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”:
</p>
<p>
	<img src="https://i.imgur.com/DJmEXEB.png" height="75%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<br />
<br />
<h3 align="center">Reload IIS (Open IIS, Stop and Start the server)</h3>
<br />
<p>
	Go to sites -> Default -> osTicket:
</p>
<p>
	<img src="https://i.imgur.com/DJmEXEB.png" height="75%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<p>
	On the right, click “Browse *:80”:
</p>
<p>
	<img src="https://i.imgur.com/DJmEXEB.png" height="75%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<br />
<br />
<h3 align="center">Enable Extensions in IIS: Note that some extensions are not enabled</h3>
<br />
<p>
	Go back to IIS, sites -> Default -> osTicket:
</p>
<p>
	<img src="https://i.imgur.com/DJmEXEB.png" height="75%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<p>
	Double-click PHP Manager:
</p>
<p>
	<img src="https://i.imgur.com/DJmEXEB.png" height="75%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<p>
	Click “Enable or disable an extension”.
</p>
<p>
	Enable: php_imap.dll.
</p>
<p>
	Enable: php_intl.dll.
</p>
<p>
	Enable: php_opcache.dll:
</p>
<p>
	<img src="https://i.imgur.com/DJmEXEB.png" height="75%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<br />
<br />
<h3 align="center">Refresh the osTicket site in your browser, observe the changes</h3>
<br />
<p>
	<img src="https://i.imgur.com/DJmEXEB.png" height="75%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<br />
<br />
<h3 align="center">Rename</h3>
<br />
<p>
	From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php.
</p>
<p>
	To: C:\inetpub\wwwroot\osTicket\include\ost-config.php:
</p>
<p>
	<img src="https://i.imgur.com/DJmEXEB.png" height="75%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<br />
<br />
<h3 align="center">Assign Permissions: ost-config.php</h3>
<br />
<p>
	Disable inheritance -> Remove All:
</p>
<p>
	<img src="https://i.imgur.com/DJmEXEB.png" height="75%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<p>
	New Permissions -> Everyone -> All:
</p>
<p>
	<img src="https://i.imgur.com/DJmEXEB.png" height="75%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<br />
<br />
<h3 align="center">Continue Setting up osTicket in the browser (click Continue)</h3>
<br />
<p>
	Name Helpdesk.
</p>
<p>
	Default email (receives email from customers):
</p>
<p>
	<img src="https://i.imgur.com/DJmEXEB.png" height="75%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<br />
<br />
<h3 align="center">Download and Install HeidiSQL (download from within lab files: link)</h3>
<br />
<p>
	Create a new session, root/Password1:
</p>
<p>
	<img src="https://i.imgur.com/DJmEXEB.png" height="75%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<p>
	Connect to the session:
</p>
<p>
	<img src="https://i.imgur.com/DJmEXEB.png" height="75%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<p>
	Create a database called “osTicket”:
</p>
<p>
	<img src="https://i.imgur.com/DJmEXEB.png" height="75%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<br />
<br />
<h3 align="center">Continue Setting up osticket in the browser</h3>
<br />
<br />
<br />
<p>MySQL Database: osTicket</p>
<p>
	MySQL Username: root
</p>
<p>
	MySQL Password: Password1:
</p>
<p>
	<img src="https://i.imgur.com/DJmEXEB.png" height="75%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<p>Click “Install Now!”</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Congratulations, hopefully it is installed with no errors!</hp>
<p>
	<img src="https://i.imgur.com/DJmEXEB.png" height="75%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<br />
<br />
<h3 align="center">Clean up</h3>
<br />
<p>
	Delete: C:\inetpub\wwwroot\osTicket\setup:
</p>
<p>
	<img src="https://i.imgur.com/DJmEXEB.png" height="75%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<p>
	Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php:
</p>
<p>
	<img src="https://i.imgur.com/DJmEXEB.png" height="75%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<br />
<br />
<h3 align="center">Login to the osTicket Admin Panel (http://localhost/osTicket/scp/login.php)</h3>
<br />
<p>
	<img src="https://i.imgur.com/DJmEXEB.png" height="75%" width="100%" alt="Disk Sanitization Steps"/>
</p>
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
