<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.  This tutorial assumes a Windows 10 VM has already been created.  <a href="https://github.com/JPac45/Creating-VMs-within-Azure">CLICK HERE</a> for the VM Creation Tutorial.  We will also need to install on the VM a few files. To get started click here for <a href="https://drive.google.com/drive/u/2/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6">INSTALLATION FILES.</a><br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines)
- Remote Desktop
- Internet Information Services (IIS)
- MySQL

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Installation Steps</h2>
Enabling <b>IIS</b> on Windows 10 VM

- Go to Control Panel > Programs > Turn Windows Features On or OFF
- Click and Expand Internet Information Services (IIS) > Click and Expand World Wide Web Services > Click and Expand Application Development Features > Check CGI 
- Click and Expand Common HTTP Features > Check all boxes > Click OK
  
<p>
<img src="https://i.imgur.com/9aLsrDd.gif"/>
</p>
<p>
</p>
<br />
<b>PHP Manager for IIS</b> install

- Go to the Installation Files and download and Install PHP Manager for ISS

<p>
<img src="https://i.imgur.com/FR3qXXX.png"/>
</p>
<p>
</p>
<br />
<b>Rewrite Module</b> install

- Go to the Installation Files and download and Rewrite Module

<p>
<img src="https://i.imgur.com/yMwZjqs.png"/>
</p>
<p>
</p>
<br />
<b>Create the Directory C:\PHP </b>

- Open File Explorer > This PC > Windows (C:) Drive > Right-click to add New Folder> label it "PHP"

<p>
<img src="https://i.imgur.com/FBuudVR.png"/>
</p>
<p>
</p>
<br />
<b>Download and Install PHP 7.3.8 zip file </b>

- Unzip PHP 7.3.8 (PHP 7.3.8-nt-Win32-VC15-x86.zip) into C:\PHP from the installation files.
- Double-click on PHP 7.3.8 > Right-click to Extract All > Click browse > This PC > Windows (C:) > Click PHP > Extract

<p>
<img src="https://i.imgur.com/XW6eYTU.gif"/>
</p>
<p>
</p>
<br />
<b>Download and Install VC_redist.x86.exe</b>
<p>
<p> 
<img src="https://i.imgur.com/RbZ2JGd.png"/>
</p>
<p>
</p>
<br />
<b>Download and Install MySQL 5.5.62</b>

- Double-click on MySQL > Click Next > Click Next > Select Typical > Click Install
- After install, Check box for Launch the MySQL Instance Configuration Wizard > Click Finish > Click Next > Select Standard Configuration > Click Next > Select Install as Windows Service > Click Next > Create a password i.e. Username: ROOT  Password: Password1 > Click Next > Click Execute > Click Finish

<p>
<img src="https://i.imgur.com/c4RCYnk.gif"/>
</p>
<p>
</p>
<br />
<b>Register PHP from within ISS</b>

- Open IIS as adminstrator > Double-click on PHP Manager > Click Register new PHP version > Click Browse > Select Php-cgi > Click OK
- Restart IIS

<p>
<img src="https://i.imgur.com/ZmfRxwL.gif"/>
</p>
<p>
</p>
<br />
<b>Install osTicket v1.15.8</b>

- Download osTicket from the installation files
- Extract and copy "upload" folder to C:\inetpub\wwwroot
- Within C:\inetpub\wwwroot, Rename "upload" to "osTicket"

<p>
<img src="https://i.imgur.com/Nwvd9Zf.gif"/>
</p>
<p>
</p>
<br />


- Restart IIS
- Goto Default Web Site > osTicket > on the right, Click "Browse *80"
- An osTicket webpage should open after clicking "Browse *80"

<p>
<img src="https://i.imgur.com/KKx3wpb.gif"/>
</p>
<p>
</p>
<br />


- NOTE: On the webpage, some extensions are disabled with a red X. You must enable these. To enable php extensions go back to ISS > Default Web Site > osTicket > Double-click on php manager > Click on php extensions > Enable the disabled extensions > Restart the server.


<p>
<img src="https://i.imgur.com/YmEXwuA.png"/>
</p>
<p>
</p>
<br />
<b>Rename ost-sampleconfig.php</b>

- Rename C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
- To C:\inetpub\wwwroot\osTicket\include\ost-config.php

<p>
<img src="https://i.imgur.com/Nwvd9Zf.gif"/>
</p>
<p>
</p>
<p>
</p>
<br />
<b>Install HeidiSQL</b>

- Download osTicket from the installation files
- Extract and copy "upload" folder to C:\inetpub\wwwroot
- Within C:\inetpub\wwwroot, Rename "upload" to "osTicket"

<p>
<img src="https://i.imgur.com/Nwvd9Zf.gif"/>
</p>
<p>
</p>
<br />
<h2>Configuration Steps</h2>ABOVE LAST

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<h2>Configuration Steps</h2>

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

<h2>Video Reference Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com/watch?v=dEvGaxOgqf0)

