<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket Ticketing System Installation</h1>
This tutorial demonstrates the installation of the open-source ticketing system osTicket.

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Installation Steps</h2>

Within the Microsoft Azure portal, search for virtual machines in the search bar. Click on virtual machines. Click Create and select Azure Virtual Machine.
</br>
<p>
<img width="722" height="551" alt="Screenshot 2026-01-08 233312" src="https://github.com/user-attachments/assets/10c820cf-073b-4614-bd58-d3c4a60ffc4d" />
</p>
Under Resource Group, select create new and name the resource group osTicket. Name the virtual machine osTicket-vm. Place the virtual machine in the East US 2 region. Select a Windows 10 image within images. Make the username labuser and the password osTicketPassword1!. Click on next:disks.
</br>
<p>
<img width="1021" height="819" alt="Screenshot 2026-01-08 233906" src="https://github.com/user-attachments/assets/1e3234c6-0b08-41dc-976e-7d52398485d5" />
</p>
Click on review+create.
</br>
<p>
<img width="762" height="718" alt="Screenshot 2026-01-08 234120" src="https://github.com/user-attachments/assets/9da626e3-8d6c-4168-8455-f548c7d12b19" />
</p>
Click on create.
</br>
<p>
<img width="742" height="434" alt="Screenshot 2026-01-08 234443" src="https://github.com/user-attachments/assets/c3fd4c59-b95d-46cb-b45d-4d73aaca7254" />
</p>
Navigate back to virtual machines using the search bar. Copy the public IP address for the osTicket virtual machine.
</br>
<p>
<img width="1327" height="101" alt="Screenshot 2026-01-08 234742" src="https://github.com/user-attachments/assets/791bb4cb-3775-4fac-8ffe-322e1c4b034e" />
</p>
Open the Microsoft Remote Desktop application. Click the plus symbol and choose add PC. Paste the IP address into the PC name and make the friendly name osTicket. Then click add to create the connection. 
</br>
<p>
<img width="428" height="489" alt="Screenshot 2026-01-08 235044" src="https://github.com/user-attachments/assets/0ca18702-44de-47cf-b429-dc1c1e02e781" />
</p>
Click on the osTicket connection and enter the username as labuser and the password as osTicketPassword1!.
</br>
<p>
<img width="400" height="139" alt="Screenshot 2026-01-08 235337" src="https://github.com/user-attachments/assets/bdc625d8-29de-47ab-9925-63638e174ec4" />
</p>
Open Microsoft Edge inside the virtual machine. Download the osTicket-Installation-Files.zip
</br>
<p>
<img width="743" height="380" alt="Screenshot 2026-01-09 001736" src="https://github.com/user-attachments/assets/2e9126b4-23d7-473b-ae8b-786003e39ebf" />
</p>
Open the Downloads Folder within File Explorer. Drag the zip file onto the Desktop. Right click the file and select extract all. Extract the file onto the Desktop.
</br>
<p>
<img width="561" height="403" alt="Screenshot 2026-01-09 002320" src="https://github.com/user-attachments/assets/4b9250e2-867c-4b27-b946-3defc02dc8b8" />
</p>
Search for control panel in the search bar next to the Windows icon. Open control panel. Click uninstall a program. Click turn Windows features on or off. Check the box next to Internet Information Services. Expand Worldwide Web Service and Application Development Features and check the box next to CGI. 
</br>
<p>
<img width="376" height="303" alt="Screenshot 2026-01-09 003001" src="https://github.com/user-attachments/assets/3e28362e-4429-4e60-82e4-e866cee1f221" />
</p>
<p>
<img width="379" height="312" alt="Screenshot 2026-01-09 002948" src="https://github.com/user-attachments/assets/6a276f24-2c9a-4f94-a6cd-cc80dd95eea7" />
</p>
Open the osTicket Installation Files folder on the Desktop. Double-click the PHPManagerforIIS file. Click next and then agree and next. PHP Manager for IIS is now installed.
</br>
<p>
<img width="459" height="370" alt="Screenshot 2026-01-09 003701" src="https://github.com/user-attachments/assets/888b7a1a-e6c9-4b8a-9cb2-ef40e6733f05" />
</p>
Double-click the rewrite_amd64_en-US.msi file in the osTicket Installation Files folder. Accept the terms and click install.
</br>
<p>
<img width="453" height="350" alt="Screenshot 2026-01-09 004108" src="https://github.com/user-attachments/assets/a7564540-cf66-4416-97a5-373e4f40748b" />
</p>
Click on File Explorer and expand the C: drive. Make a new folder called PHP. 
</br>
<p>
<img width="611" height="578" alt="Screenshot 2026-01-09 004417" src="https://github.com/user-attachments/assets/b247d6b1-e629-41d3-acc8-6e2722df31c6" />
</p>
Within the osTicket Installation Files folder, right-click the php-7.3.8-nts-Win32-VC15-x86.zip file and select extract all. Click on browse and select the C:\PHP folder. Click on select.
</br>
<p>
<img width="552" height="395" alt="Screenshot 2026-01-09 232541" src="https://github.com/user-attachments/assets/1cc639d1-d272-48aa-8425-745978a140c4" />
</p>
Extract the files.
</br>
<p>
<img width="616" height="577" alt="Screenshot 2026-01-09 232735" src="https://github.com/user-attachments/assets/bb1edd9b-f1a0-4d72-bd45-6c2fd55546fe" />
</p>
Inside the osTicket Installation Files folder, double-click the VC_redist.x86.exe file. Select agree and then install.
</br>
<p>
<img width="439" height="273" alt="Screenshot 2026-01-09 233117" src="https://github.com/user-attachments/assets/51d07054-b504-4431-9e65-e33f56efe778" />
</p>
Inside the osTicket Installation Files folder, double-click the mysql-5.5.62-win32.msi file. Click on next. Accept the terms and then click next. Select typical installation. Click on install.
</br>
<p>
<img width="450" height="352" alt="Screenshot 2026-01-09 233609" src="https://github.com/user-attachments/assets/c6f16ad6-0676-4ec4-b3b7-2633b33aa730" />
</p>
Click on Launch the MySQL Instance Configuration Wizard. Click on finish. Click on next. Choose standard configuration and click next. Click next again in Windows options. For project purposes, make the root password root. Click on next.
</br>
<p>
<img width="456" height="348" alt="Screenshot 2026-01-09 234220" src="https://github.com/user-attachments/assets/d6c4cf33-2de7-46df-a389-a82c311df573" />
</p>
Search iis in the search bar in Windows and right-click and open Internet Information Services Manager as an Administrator.
</br>
<p>
<img width="701" height="551" alt="Screenshot 2026-01-09 234448" src="https://github.com/user-attachments/assets/0bca3c53-6568-4d2c-8c93-7d627992fef3" />
</p>
Double-click PHP Manager. Select Register New PHP Version. Click on the three dot button and browse to C:\PHP\php-cgi.exe. Click on OK.
</br>
<p>
<img width="464" height="196" alt="Screenshot 2026-01-09 234852" src="https://github.com/user-attachments/assets/bfbd7d21-6b86-4b75-a786-1096a9634380" />
</p>
Right-click osticket-vm on the left and click Stop. Click on Start.
</br>
<p>
<img width="312" height="169" alt="Screenshot 2026-01-09 235109" src="https://github.com/user-attachments/assets/fb4eb692-75b8-4466-9a93-72b66d357fd9" />
</p>
Inside the osTicket Installation Files folder, right-click the osTicket-v1.15.8.zip file and select extract all. Click extract.
</br>
<p>
<img width="548" height="392" alt="Screenshot 2026-01-10 230924" src="https://github.com/user-attachments/assets/9ba3e462-efc8-485b-a162-7809107ecaa8" />
</p>
Open the extracted folder. Copy the upload folder into C:\inetpub\wwwroot.
</br>
<p>
<img width="615" height="580" alt="Screenshot 2026-01-10 231217" src="https://github.com/user-attachments/assets/6cf4c09e-c2fb-44e1-9993-dda69ad5fa6f" />
</p>
Right-click the upload folder and select rename. Make the name osTicket.
</br>
<p>
<img width="621" height="583" alt="Screenshot 2026-01-10 231359" src="https://github.com/user-attachments/assets/9b749887-1589-4981-99ab-645e8bafa816" />
</p>
Open Internet Information Services. Right-click the osticket-vm server and select stop. Right-click and select start.
</br>
<p>
<img width="270" height="156" alt="Screenshot 2026-01-10 231633" src="https://github.com/user-attachments/assets/81c19782-d59a-434f-97fd-947a5a9afec3" />
</p>
<p>
<img width="252" height="149" alt="Screenshot 2026-01-10 231730" src="https://github.com/user-attachments/assets/def4a8ed-ae3e-4292-b180-341302f5a950" />
</p>
Inside of IIS, expand Sites and Default Web Site. Click the osTicket folder. Click browse:80 on the right. osTicket should load successfully.
</br>
<p>
<img width="765" height="689" alt="Screenshot 2026-01-10 232031" src="https://github.com/user-attachments/assets/daf70754-fedb-4348-8ad2-8db9875faa38" />
</p>
Inside of IIS, expand Sites and Default Web Site. Click the osTicket folder. Double-click PHP Manager. Select enable or disable an extension below PHP Extensions.
</br>
<p>
<img width="520" height="512" alt="Screenshot 2026-01-10 232559" src="https://github.com/user-attachments/assets/44771bad-1516-4305-a8dc-43c8177524aa" />
</p>
Double-click php_imap.dll, php_intl.dll and php_opcache.dll and select Enable for each.
</br>
<p>
<img width="562" height="412" alt="Screenshot 2026-01-10 232842" src="https://github.com/user-attachments/assets/4235a956-c700-4ac1-b01e-c1f47f619e98" />
</p>
Refresh the browser which has the osTicket site open. Some of the extensions will change.
</br>
<p>
<img width="789" height="682" alt="Screenshot 2026-01-10 233127" src="https://github.com/user-attachments/assets/44e16d78-c099-451e-9575-1d32d11093ca" />
</p>
Open File Explorer and open C:\inetpub\wwwroot. Open the osTicket folder. Open the include folder. Right-click the ost-sampleconfig.php file and rename it to ost-config.php.
</br>
<p>
<img width="609" height="536" alt="Screenshot 2026-01-10 233541" src="https://github.com/user-attachments/assets/94b2072c-dfb4-48d7-bc78-04d9b2f6d6ef" />
</p>
Right-click ost-config.php and select Properties. Click the Security tab. Click Advanced. Click Disable inheritance and Remove all inherited permissions from this object.
</br>
<p>
<img width="479" height="248" alt="Screenshot 2026-01-10 233815" src="https://github.com/user-attachments/assets/c9762c99-1298-44d7-bf8e-8cad68271e0c" />
</p>
Click add. Click Select a principal. Type everyone in the blank field and click check names. Click OK.
</br>
<p>
<img width="416" height="226" alt="Screenshot 2026-01-10 234037" src="https://github.com/user-attachments/assets/0e03c900-7de8-427b-b977-0361cf9844f5" />
</p>
Click Full-control and click OK.
</br>
<p>
<img width="845" height="544" alt="Screenshot 2026-01-10 234227" src="https://github.com/user-attachments/assets/40a6857b-6d5b-4d23-bebe-2ad297e5431d" />
</p>
Click apply and OK.
</br>
<p>
<img width="702" height="473" alt="Screenshot 2026-01-10 234341" src="https://github.com/user-attachments/assets/1681cc87-461a-4b04-89ec-9779674ed429" />
</p>
In the browser containing the osTicket site, click Continue. Make the name Tanner's Help Desk. Assign an email address. Name the admin user Tanner Van Newkirk and make the email address different from the previous email address. Make the username adminuser and the password Password1.
</br>
<p>
<img width="493" height="445" alt="Screenshot 2026-01-10 234819" src="https://github.com/user-attachments/assets/f45972e6-55b8-4c74-a68e-2a3605c683cc" />
</p>
Open the osTicket Installation Files folder within File Explorer. Double-click the HeidiSQL Setup application. Click accept, then click next. Click next three times consecutively. Click Install.
</br>
<p>
<img width="548" height="424" alt="Screenshot 2026-01-10 235400" src="https://github.com/user-attachments/assets/2dd7d803-8fcd-4c56-b81e-5ad713ba514c" />
</p>
Click on Finish. Click on Skip. Click on New on the bottom left corner. Make the password root and click Open.
</br>
<p>
<img width="618" height="408" alt="Screenshot 2026-01-10 235658" src="https://github.com/user-attachments/assets/4672c718-3e5e-4cb7-9097-d0018f748f4d" />
</p>
Right-click the Unnamed folder. Mouse over Create New and click Database. Make the name osTicket. Click OK.
</br>
<p>
<img width="288" height="232" alt="Screenshot 2026-01-10 235924" src="https://github.com/user-attachments/assets/b1738a10-ebe0-449f-8bd0-a02c95023baf" />
</p>
Inside the browser with osTicket, make the MySQL Database name osTicket. Make the username root and the password root. Click Install now.
</br>
<p>
<img width="757" height="609" alt="Screenshot 2026-01-11 003528" src="https://github.com/user-attachments/assets/9fa3faff-72fb-453c-816e-e5c995f9d13a" />
</p>
<p>
<img width="828" height="748" alt="Screenshot 2026-01-11 003633" src="https://github.com/user-attachments/assets/597c4275-63c4-4ffd-9e00-7edcd340197a" />
</p>



















