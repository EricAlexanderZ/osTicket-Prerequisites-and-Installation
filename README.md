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

<br />

<h2>Installation Steps</h2>


<p>
First we must Install/Enable IIS in Windows Control Panel under the programs folder.
To get to this page you can hit control or cmd 'R' depending on if you're using RDP. You'll have a small 'Run' Window pop up on the left lower corner of your screen. Proceed to type "Control" hit ok and you should now see the Control Panel.
</p>

![Screen Shot 2024-04-04 at 9 22 12 AM](https://github.com/EricAlexanderZ/osTicket-Prerequisites-and-Installation/assets/99912710/41c3b575-e2a5-4120-a649-c9c9a9d1fbf8)

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
![Screen Shot 2024-04-04 at 9 23 01 AM](https://github.com/EricAlexanderZ/osTicket-Prerequisites-and-Installation/assets/99912710/8f720de3-1490-4090-b89b-01b5aa4cc8d9)
![Screen Shot 2024-04-04 at 9 23 21 AM](https://github.com/EricAlexanderZ/osTicket-Prerequisites-and-Installation/assets/99912710/65a411a9-bda6-4187-9a88-488964e27009)


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

![Screen Shot 2024-04-04 at 9 38 19 AM](https://github.com/EricAlexanderZ/osTicket-Prerequisites-and-Installation/assets/99912710/65fb9d7b-1cc1-4b41-a3cc-c7919c8ecb00)
![image](https://github.com/EricAlexanderZ/osTicket-Prerequisites-and-Installation/assets/99912710/c88e99d2-4d8d-4f08-a35d-1f5a1157be51)
![Screen Shot 2024-04-04 at 9 39 05 AM](https://github.com/EricAlexanderZ/osTicket-Prerequisites-and-Installation/assets/99912710/a54416d5-0cce-4324-8cdd-e8628d23ec45)
![Screen Shot 2024-04-04 at 9 41 43 AM](https://github.com/EricAlexanderZ/osTicket-Prerequisites-and-Installation/assets/99912710/5a7c01e6-2f49-4fae-b3d8-0edd9ce1b58a)
![Screen Shot 2024-04-04 at 9 42 10 AM](https://github.com/EricAlexanderZ/osTicket-Prerequisites-and-Installation/assets/99912710/57d90e3e-9b4c-426f-8e1c-77b0192ad80a)
![Screen Shot 2024-04-04 at 9 42 57 AM](https://github.com/EricAlexanderZ/osTicket-Prerequisites-and-Installation/assets/99912710/5e1a3707-e9ec-4ed6-aadb-60fbe6329c23)


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
![Screen Shot 2024-04-04 at 9 45 05 AM](https://github.com/EricAlexanderZ/osTicket-Prerequisites-and-Installation/assets/99912710/c493d19f-dfc2-4bfd-b14c-988a09a096fd)

<br />


<p>
Now Restart the IIS Server by clicking 'Restart' on the right side, This will refresh the server so that your changes get implemented ✅
</p>

![Restart IIS Server](https://github.com/EricAlexanderZ/osTicket-Prerequisites-and-Installation/assets/99912710/08e96c55-11f8-48e3-909e-723eb1478e45)

<br />


<p>
Next, Install osTicket v1.15.8
</p>
- Extract and drag the “upload” folder to c:\inetpub\wwwroot
- Within c:\inetpub\wwwroot, Rename the “upload” folder to “osTicket”

![Screen Shot 2024-04-04 at 9 49 40 AM](https://github.com/EricAlexanderZ/osTicket-Prerequisites-and-Installation/assets/99912710/d970a0b7-9f4f-4d3a-adcf-30617616b72f)
![Screen Shot 2024-04-04 at 9 51 33 AM](https://github.com/EricAlexanderZ/osTicket-Prerequisites-and-Installation/assets/99912710/b7d39f18-0237-4faf-beec-9d1670939591)



<br />


<p>
Now Restart the IIS Server by clicking 'Restart' on the right side, This will refresh the server so that your changes get implemented ✅ 
</p>

![Restart IIS Server](https://github.com/EricAlexanderZ/osTicket-Prerequisites-and-Installation/assets/99912710/17fdfe92-a91a-473c-a1e3-75be1c8763f7)


<br />


<p>
Go to Sites → Default → osTicket → On the right, click “Browse *:80” | Some extensions won't be enabled
So go back to IIS and follow the steps below: 
</p>

- Sites 
- Default 
- osTicket 
- Double-click PHP Manager 
- Click “Enable or disable an extension”
- Enable: php_imap.dll
- Enable: php_intl.dll
- Enable: php_opcache.dll
- Refresh the osTicket site in your browse, observe the changes

![Screen Shot 2024-04-04 at 9 58 51 AM](https://github.com/EricAlexanderZ/osTicket-Prerequisites-and-Installation/assets/99912710/df6be5d8-e608-4963-ac51-98ad27d23bd7)
![Screen Shot 2024-04-04 at 9 59 07 AM](https://github.com/EricAlexanderZ/osTicket-Prerequisites-and-Installation/assets/99912710/00b957d3-be1c-4325-aedd-4df126ae80bf)
![Screen Shot 2024-04-04 at 10 00 16 AM](https://github.com/EricAlexanderZ/osTicket-Prerequisites-and-Installation/assets/99912710/2bd37ca4-9e92-45a6-90dc-b669c78c3b07)
![Screen Shot 2024-04-04 at 10 01 40 AM](https://github.com/EricAlexanderZ/osTicket-Prerequisites-and-Installation/assets/99912710/86de32f9-d68f-462a-950f-6d36c5ef7901)



<br />


<p>
Next, Rename: ost-sampleconfig.php
From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php ❌
To: C:\inetpub\wwwroot\osTicket\include\ost-config.php ✅
</p>

![Screen Shot 2024-04-04 at 10 03 47 AM](https://github.com/EricAlexanderZ/osTicket-Prerequisites-and-Installation/assets/99912710/b8299ee8-e0d5-46f9-a05b-a4ff905b0606)


<br />


<p>
Now, Assign Permissions to: ost-config.php | Right click the file → select properties → Security → Advanced: Follow setps below ↓
</p>

- Disable inheritance -> Remove All
- New Permissions -> Everyone -> All

![Screen Shot 2024-04-04 at 10 04 30 AM](https://github.com/EricAlexanderZ/osTicket-Prerequisites-and-Installation/assets/99912710/b7297008-3e72-4cf2-8d67-bc172bb0e39e)
![Screen Shot 2024-04-04 at 10 04 53 AM](https://github.com/EricAlexanderZ/osTicket-Prerequisites-and-Installation/assets/99912710/e20223ec-3b88-4bbf-af68-abc4dc1ef019)
![Screen Shot 2024-04-04 at 10 05 05 AM](https://github.com/EricAlexanderZ/osTicket-Prerequisites-and-Installation/assets/99912710/e2b4774b-c9a7-47ef-a155-73a760fcffa4)
![Screen Shot 2024-04-04 at 10 05 17 AM](https://github.com/EricAlexanderZ/osTicket-Prerequisites-and-Installation/assets/99912710/98bfb654-1a67-4a1b-aafb-0506d1510aee)
![Screen Shot 2024-04-04 at 10 09 32 AM](https://github.com/EricAlexanderZ/osTicket-Prerequisites-and-Installation/assets/99912710/ac0ae3df-a62c-483e-a849-038572774b08)


<br />


<p>
Continue Setting up osTicket in the browser (click Continue) you should see the following on your screen ↓
</p>

![Screen Shot 2024-04-04 at 10 09 54 AM](https://github.com/EricAlexanderZ/osTicket-Prerequisites-and-Installation/assets/99912710/ed564aa9-a6f2-4911-8584-1e69288c5711)

- ↓ 🚨 Only add info up until here for now 🚨 ↓
![Screen Shot 2024-04-04 at 12 23 54 PM](https://github.com/EricAlexanderZ/osTicket-Prerequisites-and-Installation/assets/99912710/52dd2a33-d6a0-4311-82e8-20728586a9ff)


<br />


<p>
Download and Install HeidiSQL
</p>

- Open Heidi SQL
- Create a new session
- User will be 'root'
- Add and notedown password
- Connect to the session
- Create a database called “osTicket”

![Screen Shot 2024-04-04 at 12 25 54 PM](https://github.com/EricAlexanderZ/osTicket-Prerequisites-and-Installation/assets/99912710/d9870fa2-9673-4a84-ba05-093b78e332e7)
![Screen Shot 2024-04-04 at 12 27 36 PM](https://github.com/EricAlexanderZ/osTicket-Prerequisites-and-Installation/assets/99912710/59062dac-e5ff-431b-8340-849456a098ed)
![Screen Shot 2024-04-04 at 12 28 10 PM](https://github.com/EricAlexanderZ/osTicket-Prerequisites-and-Installation/assets/99912710/2da97ecd-2c52-494d-8c40-6e1813fe7891)


<br />


<p>
Continue Setting up osTicket in the browser
</p>

- MySQL Database: osTicket
- MySQL Username: root
- MySQL Password: ******* (password that you noted down)
- Click “Install Now”

![Screen Shot 2024-04-04 at 12 29 16 PM](https://github.com/EricAlexanderZ/osTicket-Prerequisites-and-Installation/assets/99912710/154daf46-602d-4bf1-8b6d-fe63c29e2efa)


<br />


<p>
Congratulations, hopefully it is installed with no errors! You should be able to see the following on your screen
</p>

![Screen Shot 2024-04-02 at 5 19 04 PM](https://github.com/EricAlexanderZ/osTicket-Prerequisites-and-Installation/assets/99912710/4c144fdd-f362-4ab3-a249-231a9909185b)


- One link is for your admin / help desk
- The other link is for your end users, the folks that are submitting tickets.

![Screen Shot 2024-04-02 at 5 26 57 PM](https://github.com/EricAlexanderZ/osTicket-Prerequisites-and-Installation/assets/99912710/6355fa66-f9c7-4bf9-a23f-3aa8c9385265)
![Screen Shot 2024-04-02 at 5 26 46 PM](https://github.com/EricAlexanderZ/osTicket-Prerequisites-and-Installation/assets/99912710/4b274d50-72cf-4952-9d04-215d70e84773)


<br />


<p>
FINALLY! last part of installation is → Clean up
</p>

- Delete the 'setup' folder in: C:\inetpub\wwwroot\osTicket\
- Set Permissions to “Read & execute only" in the ost-config.php file. Get there thread is:
C:\inetpub\wwwroot\osTicket\include\ost-config.php

![Screen Shot 2024-04-04 at 1 18 40 PM](https://github.com/EricAlexanderZ/osTicket-Prerequisites-and-Installation/assets/99912710/4dc898b6-a236-41ee-babb-34606041d322)
![Screen Shot 2024-04-04 at 10 04 30 AM](https://github.com/EricAlexanderZ/osTicket-Prerequisites-and-Installation/assets/99912710/d93c0742-6063-4bb5-865a-3e0fb888862f)
![Screen Shot 2024-04-04 at 10 04 53 AM](https://github.com/EricAlexanderZ/osTicket-Prerequisites-and-Installation/assets/99912710/b88bcbb3-f84e-4169-a783-409ea9908869)
![Screen Shot 2024-04-04 at 10 05 59 AM](https://github.com/EricAlexanderZ/osTicket-Prerequisites-and-Installation/assets/99912710/ed35e9d2-df10-4819-beef-08726f4da582)
![Screen Shot 2024-04-04 at 10 06 13 AM](https://github.com/EricAlexanderZ/osTicket-Prerequisites-and-Installation/assets/99912710/8328855c-7b4c-45ca-9866-c7fd13696015)


<br />


<p>
DONE! Check out the following tutorial on osTicket: Post Installation Configuration (https://github.com/EricAlexanderZ/osTicket-post-installation-configuration)
</p>
