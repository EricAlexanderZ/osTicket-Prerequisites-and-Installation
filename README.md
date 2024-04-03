<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Install/Enable IIS in Windows Control Panel under "Programs"
- Download & Install PHP Manager for IIS
- Download & Install the Rewrite Module
- Create a Directory in C:\ named PHP
- Download PHP 7.3.8 and Extract Zip files into C:\PHP
- Download & Install VC_redist.x86.exe.
- Download & Install MySQL 5.5.62
- Open IIS as an Administrator
- Register PHP from within IIS
- Restart IIS (basically to refresh the server due to changes that were implemented)
- Install osTicket v1.15.8
- Restart IIS (basically to refresh the server due to changes that were implemented)
- In IIS Go to Sites ➡️ Default ➡️ osTicket & on the right side of screen, click “Browse *:80”
- Enable some of the ❌'S in IIS: Sites ➡️ Default ➡️ osTicket ➡️ PHP Manager ➡️ Enable extensions
  php_imap.dll ✅
  php_intl.dll ✅
  php_opcache.dll ✅
- Refresh the osTicket site in your browser, & observe the changes in the ❌'s
- Rename: ost-sampleconfig.php
❌ From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
✅  To: C:\inetpub\wwwroot\osTicket\include\ost-config.php

- Assign Permissions: ost-config.php
✔️ Disable inheritance ➡️ Remove All
✔️ New Permissions ➡️ Everyone ➡️ All

- Continue Setting up osTicket in the browser (click continue)
- Name Helpdesk
- Default email (receives email from customers)

- Download & Install HeidiSQL
- Open Heidi SQL ➡️ Create a new session ➡️ Username by default is: root ➡️ Create your password
- Connect to the session
- Create a database called “osTicket”:  right click "unnamed" on top left ➡️ New session 

- Continue Setting up osTicket in the browser
- MySQL Database: osTicket
- MySQL Username: root
- MySQL Password: ******
- Click “Install Now!”


- Clean up
- Delete: "setup folder" ➡️ C:\inetpub\wwwroot\osTicket\
- Set Permissions to “Read & Execute” only on ost-config.php: ➡️ C:\inetpub\wwwroot\osTicket\include\ost-config.php

- Browse to your help desk login page: http://localhost/osTicket/scp/login.php ✅
- End Users osTicket URL: http://localhost/osTicket/ ✅


<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/chyaFyl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/chyaFyl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
