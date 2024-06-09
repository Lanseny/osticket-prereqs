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
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 1: Download osTicket
1. Visit the [osTicket website](https://osticket.com/) and download the latest stable version of osTicket.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 2: Extract Files
    </p>
1. Extract the downloaded osTicket ZIP file into your web server's document root directory.
  </p>
2. Rename the extracted directory to something meaningful (e.g., "osticket").
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 3: Set Permissions
    </p>
1. Ensure proper file permissions. osTicket requires write permissions to specific directories for configuration purposes. Typically, the "uploads" and "include" directories need write permissions.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 4: Create Database
    </p>
1. Log in to your database management system (e.g., MySQL) and create a new database for osTicket.
  </p>
2. Create a new database user and grant it all privileges on the newly created database.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 5: Configuration
    </p>
1. Navigate to the "include" directory within your osTicket installation.
  </p>
2. Locate the `ost-sampleconfig.php` file and rename it to `ost-config.php`.
</p>
3. Open `ost-config.php` in a text editor and fill in the database connection details and other settings as per your setup.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 6: Install Dependencies
    </p>
1. Open a terminal or command prompt and navigate to your osTicket directory.
  </p>
2. Run `composer install` to install dependencies.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 7: Web Installation
    </p>
1. Open your web browser and navigate to your osTicket installation URL.
  </p>
2. Follow the on-screen instructions to complete the installation process.
  </p>
3. Provide the requested information, including database details, administrator account credentials, and email settings.

</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 8: Finalization
    </p>
1. After the installation is complete, delete the `setup` directory from your osTicket installation for security purposes.
  </p>
2. Log in to the osTicket admin panel using the credentials you provided during installation.
  </p>
3. Configure email settings, ticket queues, and other preferences according to your requirements.
</p>
<br />

Conclusion:
</p>
That's it! You've successfully installed osTicket. You can now start using it to manage your support 
tickets.
