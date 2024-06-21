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

1. Web Server:  Microsoft IIS.
2. PHP: Ensure PHP 7.2+ is installed with required extensions.
3. Database: A database server like MySQL ensure it's properly installed and configured.
4. Composer: A dependency manager for PHP. Install it on your system.
5. Web Browser: Any modern web browser for accessing the osTicket web interface.
<h2>Installation Steps</h2>
<p>
<img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSxGtvf6cQyiq7Qxr3FwN_5l_uYaBbpflk3ew&s" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<p>
<h2>Step 1: Creating a Virtual Machine Through Microsoft Azure</h2>
    </p>
1. Visit "Portal.Azure.com" and sign in or create an account 
</p>
2. Create a Resource Group
</p>
3. Then create a Virtual machine(VR) within the Resource Group that was already created 
</p>
4. Find your VR public IP address and put it into to Remote Desktop on your PC/Mac to open the VR
</p>
<br />

<p>
<img src="https://static1.howtogeekimages.com/wordpress/wp-content/uploads/2014/07/new-IIS-hero.png?q=50&fit=contain&w=1140&h=&dpr=1.5" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<h2>Step 2: Installing / Enabling IIS in Windows With CGI and Common HTTP Features</h2>
    </p>
1. Search for Windows Features
</p>
2. Find Internet "Information Services" and check off on it
</p>
3. Expand Internet "Information Services" and check off "World Wide Web Services"
</p>
4. Expand "World Wide Web Services" and check "Application Development Features"
</p>
5. Expand "Application Development Features" and check "CGI"
</p>
6. Then check off "Common HTTP Features" and Expand it and make sure everything is checked off
</p>
7. Press "OK" then Verify by opening up to a Web Browser and typing up "127.0.0.1"
</p>
    (THE IMAGE SHOWEN FOR STEP 2 SHOULD BE THE VERIFICATON FOR INSTALLING IIS)
</p>
<br />

<p>
<img src="https://st3.depositphotos.com/3001967/18684/i/450/depositphotos_186840910-stock-photo-download-progress-almost-done-dialog.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<h2>Step 3: Downloading and Installing Files</h2>
    </p>
1. Download and install <a href="https://drive.google.com/file/d/1RHsNd4eWIOwaNpj3JW4vzzmzNUH86wY_/view?usp=share_link">PHP Manager for IIS</a>
</p>
2. Download and install <a href="https://drive.google.com/file/d/1tIK9GZBKj1JyUP87eewxgdNqn9pZmVmY/view?usp=share_link">Rewrite Module</a>
</p>
3. Create the directory C:\PHP
    </p>
    - open Files explore
  </p>
    - double-click "This PC"
  </p>
    - then double-click "Windows(C):"
  </p>
    - Create a New File and rename it PHP
  </p>
4. Download and install <a href="https://drive.google.com/file/d/1snNMtLdCOpMtkCyD4mvl9yOOmvVIp9fP/view?usp=share_link">PHP 7.3.8</a>(php-7.3.8-nts-Win32-VC15-x86.zip) 
     </p>
    - right-click "extract all" and browser to unzip contents into the created file PHP Folder
  </p>
5. Download and install <a href="https://drive.google.com/file/d/1s1OsGF3-ioO0_9LYizPRiVuIkb3lFJgH/view?usp=share_link">VC_redist.x86.exe.</a>
</p>
6. Download and install <a href="https://drive.google.com/file/d/1_OWh9p7VQLcrB0q_V7qT8yHl0xo5gv7z/view?usp=share_link">MySQL 5.5.62 </a>(mysql-5.5.62-win32.msi)
    - Typical Setup ->
    </p>
    - launch configuration wizard (after install) ->
    </p>
    - standard configuration ->
    </p>
    - create a new root password
</p>
<br />
<p>
<img src="https://azure.microsoft.com/svghandler/app-configuration/?width=600&height=315" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<p>
<h2>Step 4: Configuriations in IIS</h2>
    </p>
1. Search "IIS" and Right click and Run as Administator 
    </p>
2. Doulble click PHP Manager
    </p>
  - then click on register new PHP verison
    </p>
  - click "..." go to "Windows(C):"
    </p>
  - click PHP folder and then "open php-cgi"
     </p>
  - go back to "VM-osticket HOME" portal and click "restart"
</p>
<br />
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<h2>Step 5: Downloading osTicket</h2>
    </p>
1. Visit the [osTicket website](https://osticket.com/) and download the latest stable version of osTicket.
</p>
<br />
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<h2>Step 3: Download osTicket</h2>
    </p>
1. Visit the [osTicket website](https://osticket.com/) and download the latest stable version of osTicket.
</p>
<br />



<h2>Conclusion:<h2>
</p>
That's it! You've successfully installed osTicket. You can now start using it to manage your support 
tickets.
