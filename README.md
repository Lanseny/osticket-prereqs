<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This comprehensive tutorial provides detailed instructions on the prerequisites and step-by-step installation process of osTicket, an open-source help desk ticketing system. Designed to enhance customer support efficiency, osTicket allows organizations to streamline their ticketing processes, track and manage customer queries, and improve overall service delivery. By following this guide, you will learn how to prepare your environment, configure necessary components, and successfully deploy osTicket on your server. Whether you are an IT professional, a system administrator, or someone new to help desk solutions, this tutorial aims to equip you with the knowledge and tools needed to implement and customize osTicket to meet your specific needs.<br />

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
1. Visit  <a href="https://login.microsoftonline.com/organizations/oauth2/v2.0/authorize?redirect_uri=https%3A%2F%2Fportal.azure.com%2Fsignin%2Findex%2F&response_type=code%20id_token&scope=https%3A%2F%2Fmanagement.core.windows.net%2F%2Fuser_impersonation%20openid%20email%20profile&state=OpenIdConnect.AuthenticationProperties%3D5bUWkKP5KwqBSQnQZmgaWP1cZQmx5fUhpHMytCDdh2JTZpn1aJ_kThmS76rWgYHB8QxHJr-4RfRv9T1M1b3c9QYlqY6AFqaucjqsZGx_HY7g88LXPQHrL_yV1KrY_2a9I8yDSHtvY-XiE_pjzWyIBIRkolEQG6KOnKWa-Y9vZlwx3SS7VCW-irWFkHZajLYNzpPXGeaN1BafkySnWbQavrnnOpm0Scnl7zTPVNDBKi_-wkFZsN9ALE5okxI3Di17_8eBrPo2o6Hh6OK0scte0HJqOtSchedNiSOs533d2vwT_-oeABGcjmiTc-mv8OhwfFRKRVLmqBWj_InJpbHBGyMym_zHPUWikhMQ7ty7U04CNJBt5koEcGu8CpOCGKDu70iGn5GxlHz1J0gfltMl_FJbI-5A-ib1ZjUBi9lrXekA1KTE0DqDWhRMy76T2W82BI8d2TWAd8OJgqMbsYky34w1YRdqtTBv4pLgzipNxs9O1nhpVhoPMKeXc9BXtBmZ-LmADYD32UoOGVxcDEbfiLuUAs_AscIwiAWZZYRimkRMzw8r1LwTqhWCPMmrawFuzIk_3YIjyY2P_oL1JEV1nw&response_mode=form_post&nonce=638553091966138647.Y2IwMWY1ZmEtNWRjNy00OGEyLTgxYTMtYTM1NDAwMzNmZTQwOTQ1ZDhkNDgtNTE2MS00ZjI2LTk5MDgtZDliNTVkMWNhYzdi&client_id=c44b4083-3bb0-49c1-b47d-974e53cbdf3c&site_id=501430&client-request-id=146a9ba0-a004-4ec9-8e6d-51b7540a2458&x-client-SKU=ID_NET472&x-client-ver=7.5.0.0">"Portal.Azure.com"</a> and sign in or create an account 
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
<img src="https://miguelmenendez.pro/en/repository/osticket-bootstrap/osticket.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<p>
<h2>Step 5: Downloading osTicket</h2>
     </p>
1. Visit the [osTicket website](https://osticket.com/) and download the latest stable version of osTicket.
 </p>
2. Once you get your zip folder open File Explorer go to downloads and open up the zip folder
 </p>
3. Open a secound File Explorer and the open up "This Pc" --> "Windows(c:)" --> "intetpub" --> "wwwroot"
 </p>
4. Then drag the "Upload file" from your zip folder into "wwwroot"
 </p>
5. Go into "wwwroot" and rename the "Upload file" to "osTicket"
 </p>
6. Go back into IIS as an Administator click "restart" 
</p>
7. Go to sites in IIS -> Default -> osTicket -> Double ckick PHP manager
 - Click “Enable or disable an extension”
        </p>
          Enable: php_imap.dll
          </p>
          Enable: php_intl.dll
          </p>
          Enable: php_opcache.dll
</p>
8. Go back sites in IIS -> Default -> osTicket on the right, click “Browse *:80”
</p>
<br />

<p>
<img src="https://heera.it/wp-content/uploads/2013/07/iconfig-e1373233686608.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<p>
<h2>Step 6: ost-config.php</h2>
    </p>
1. Open File Explorer click "This Pc" --> "Windows(c:)" --> "intetpub" --> "wwwroot"
 </p>
2. Go to Newly Named file "osTicket"--> "include" 
 </p>
3. Scroll down and rename "ost-sample config.php" to "ost-config.php"
 </p>
4. Right Click, Open up "Properties" then click "Security"--> "Advance"--> "Disable Inheritance"-->"Remove all permissions from the object"
 </p>
5. Add a new Permission and then click "select a principal"
 </p>
6. Go to the "Enter the object name to Select" and type in Everyone and click "check name" to make a new principal
 </p>
7. Go to "Basic Permission" and check off all boxes
 </p>
</p>
<br />
<p>
<img src="https://i.ytimg.com/vi/dEvGaxOgqf0/maxresdefault.jpg" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<p>
<h2>Step 7: Continue Setting up osTicket in the browser</h2>
    </p>
1. Press Continue
</p>
2. Fill in the info for your "System Setting" and "Admin User"
</p>
3. download and install <a href="https://www.heidisql.com/installers/HeidiSQL_12.3.0.6589_Setup.exe">HeidiSQL</a>
</p>
  - Open Heidi SQL
  </p>
  - Click "new" and put in the username and password from when you were setting up mySQL server and "open"
  </p>
  - Create a database called “osTicket” by Right Clicking "Unnamed"--> "create new"--> "database"
  </p>
4. Now you can Fill in the info for "Database setting" from the osTicket browser and click "Install Now"   
<p>
<img src="https://cdn2.iconfinder.com/data/icons/data-analytics-statistics/68/Data_Cleaning-512.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<h2>Step 8: clean up</h2>
    </p>
1. Delete the "setup" by clicking "This Pc" --> "Windows(c:)" --> "intetpub" --> "wwwroot"--> "osTicket"--> "setup"
</p>
2. Set Permissions to “Read” only: "This Pc" --> "Windows(c:)" --> "intetpub" --> "wwwroot"--> "osTicket"--> "include"--> "ost-config.php"
</p>
   - Properties--> "Security"
   </p>
   - Click "Advance"--> "Edit" then go to Basic permissions and uncheck everything but "Read & execute" and "Read" then press ok and apply
 </p>
</p>
<br />

<h2>Conclusion:<h2>
</p>
That's it! You've successfully installed osTicket. You can now start using it to manage your support 
tickets.
