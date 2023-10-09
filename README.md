<p align="center">
<img src="https://github.com/AtomSteve/Network-File-Shares-and-permissions/assets/147112183/a7962980-6bb1-4ec9-8954-bb6b989f1df5" width="200" height="400" />





</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />






<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Configuration Objectives</h2>

-  Create sample files and share with various permissons
-  Attempt to access file shares as a normal user
-  Create an "ACCOUNTANTS" Security Group, assign permissons, an test access


<h2>Creating sample files and share with various permissons</h2>

From our Active directory that we already created and log into it (DC-1).  Do the same with Client-2.  On DC-1 go to the C:\ drive and create the following folders.  After creating right click them and go to properties -> sharing -> and Add domain users and set it according to the folder name 
-  read-access domain users read only
-  write-access domain users read/right
-  no-access -domain admin read/right


</p>
<br />

![image](https://github.com/AtomSteve/Network-File-Shares-and-permissions/assets/147112183/fee525c7-0e78-4863-99ca-48b4d470d946)![image](https://github.com/AtomSteve/Network-File-Shares-and-permissions/assets/147112183/83121c8a-ec00-4e34-b422-99748e6ba01b)![image](https://github.com/AtomSteve/Network-File-Shares-and-permissions/assets/147112183/0f6bf26f-326f-4773-94c6-fa2f63e3f227)




</p>

<h2>Attempt to access file shares as a normal user</h2>

On DC-1 in the read folder create a document and save it there. On Client-1 go to start button and run \\dc-1 and you should see the folder you made on DC-1.  Notice that you can access only a few of them, access the read folder and open the document you made.  Notice you can only read not edit

</p>
<br />

![image](https://github.com/AtomSteve/Network-File-Shares-and-permissions/assets/147112183/27358940-277e-4be7-83e9-f9211e2fc73f)![image](https://github.com/AtomSteve/Network-File-Shares-and-permissions/assets/147112183/41a73cf3-21ef-4450-8a93-435be4569ea5)





