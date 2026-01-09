<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket Ticketing System Installation and Configuration</h1>
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


