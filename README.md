<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Computer)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used</h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Create and Set Up Azure Virtual Machine (VM)
- Install IIS and Required Components 
- Configure IIS and PHP for osTicket
- Configure osTicket and MySQL Database
- Finalize Installation and Secure Setup

<h2>Installation Steps</h2>
</p>
<p>
<mark>Create and Set Up Azure Virtual Machine</mark>

- ### [YouTube:Setup Virtual Machine][(https://www.youtube.com/watch?v=rKVj3tpPpmo]

Purpose: Provides a dedicated environment to host osTicket.

Deploy a Windows 10 VM on Azure with 4 vCPUs to ensure smooth performance.
Set up login credentials for remote access.
Use Remote Desktop (RDP) to connect to the VM and begin installations.
</p>
<br />
<p>
  
<mark>Install IIS and Required Components</mark>

![image](https://github.com/user-attachments/assets/c0a67b31-ea84-43b0-aa5c-5f8b58d6a74e)


The purpose of this is that it sets up the web server and necessary software for osTicket.

Enable IIS (Internet Information Services) with CGI support to run PHP applications.
Install PHP Manager and Rewrite Module to manage PHP settings and enable URL rewriting.
Set up PHP 7.3.8 in C:\PHP for handling PHP-based scripts.
Install Visual C++ Redistributable and MySQL 5.5.62, which are required for the database.
</p>
<br />

![Install IIS image](https://github.com/user-attachments/assets/655db479-c8d2-44cf-8207-a6b16e20e02f)


![Install CGI](https://github.com/user-attachments/assets/883e8a75-9e43-4d16-9608-12c68e991cc7)


<mark>Configure IIS and PHP for osTicket</mark>

Open IIS as an administrator and register PHP (php-cgi.exe).
Restart IIS to apply changes.
Extract osTicket files into C:\inetpub\wwwroot\osTicket, making it accessible via the web server.
Reload IIS to recognize the new site and verify accessibility in a web browser.

https://github.com/user-attachments/assets/db657d6a-3dee-4b8f-96cb-82c670f6cd11

<p>
  
<mark>Configure osTicket and MySQL Database</mark>

https://github.com/user-attachments/assets/33760f65-f25c-41d8-bea1-446e4c803493

Purpose: To set up the database and configure osTicket’s backend.
Enable required PHP extensions (php_imap.dll, php_intl.dll, php_opcache.dll) for full functionality.
Rename and set permissions on ost-config.php to store osTicket settings securely.
Install HeidiSQL, a database management tool, and create a new MySQL database for osTicket.
<p>

<mark>Finalize Installation and Secure Setup</mark>

![image](https://github.com/user-attachments/assets/2769febd-c07c-4892-87b9-435547a4f2fb)

Purpose: Completes the installation and applies security measures.

Finish osTicket setup in the browser, linking it to the MySQL database.
Access the admin portal at http://localhost/osTicket/scp/login.php to manage tickets.
Secure the installation by deleting the setup directory and setting read-only permissions on ost-config.php to prevent unauthorized changes.
  
<br />
