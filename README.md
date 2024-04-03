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
First we must Install/Enable IIS in Windows Control Panel under the programs folder.
To get to this page you can hit control or cmd 'R' depending on if you're using RDP. You'll have a small 'Run' Window pop up on the left lower corner of your screen. Proceed to type "Control" hit ok and you should now see the Control Panel.
</p>

![image](https://github.com/EricAlexanderZ/osTicket-Prerequisites-and-Installation/assets/99912710/96316e28-512e-40c8-bcd1-7d3d91cafaad)


<br />


<p>
Next, click Turn windows features on or off. You should have this window popup check off the following:
</p>

- IIS✔️
- World Wide Web Services✔️ 
- Application Dev. Feat.✔️ 
- Common HTTP Feat.✔️
<p>
Once those are checked off you can then click the '+' icon next to Application Dev. Feat. for the drop menu to show. Ensure to check off CGI✔️. Next, click the '+' icon beside Common HTTP Feat. and ensure all the boxes are checked off.✔️
</p>

![image](https://github.com/EricAlexanderZ/osTicket-Prerequisites-and-Installation/assets/99912710/816ca4d6-c52d-45df-bedb-86f4f3c3060d)


<br />


<p>
You can test IIS to ensure you've got it up and running by simply opening a browser and typing 127.0.0.1 and if you see an the same image popup on your screen, that means you did everything correctly. 
</p>

![image](https://github.com/EricAlexanderZ/osTicket-Prerequisites-and-Installation/assets/99912710/3f89e59c-5d48-4163-b020-691d90b7abf0)


<br />


<p>
Create a new folder in the C:\ drive and name it 'PHP' ➡️ Then download and Install all of the following in this order and follow the steps:
</p>

- PHP Manager V1.5.0msi
- Rewrite_amd64_en-US.msi
- PHP 7.3.8 ➡️ Right click and Extract the files into C:\PHP  
- Download and Install VC_redist.x86.exe.
- Download and Install MySQL 5.5.62 ➡️ Click Typical Setup ➡️ Launch Configuration Wizard & install ➡️ Select Standard Configuration ➡️ Set a password and note it down.

![image](https://github.com/EricAlexanderZ/osTicket-Prerequisites-and-Installation/assets/99912710/c88e99d2-4d8d-4f08-a35d-1f5a1157be51)


<br />


<p>
Now in the bottom left windows search bar type 'IIS' ➡️ Right click ➡️ Run as administrator
</p>

![image](https://github.com/EricAlexanderZ/osTicket-Prerequisites-and-Installation/assets/99912710/0895dfb4-1faf-4ec9-9d53-724dbac2cf2c)


<br />


<p>
Now register PHP within IIS, Click Register new PHP version ➡️ Click on the '...' ➡️ Look for C:\PHP ➡️ Click Ok
</p>

![image](https://github.com/EricAlexanderZ/osTicket-Prerequisites-and-Installation/assets/99912710/c08b5039-6042-4cf8-ae58-2ca56144a790)


<br />
