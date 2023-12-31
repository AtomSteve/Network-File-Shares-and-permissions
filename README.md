<p align="center">
<img src="https://github.com/AtomSteve/Network-File-Shares-and-permissions/assets/147112183/a7962980-6bb1-4ec9-8954-bb6b989f1df5" width="400" height="350" />

<h2>Network-File-Share-and-permissons</h2>



</p>







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
-  ACCOUNTANT (leave for now)


</p>
<br />

![image](https://github.com/AtomSteve/Network-File-Shares-and-permissions/assets/147112183/fee525c7-0e78-4863-99ca-48b4d470d946)![image](https://github.com/AtomSteve/Network-File-Shares-and-permissions/assets/147112183/83121c8a-ec00-4e34-b422-99748e6ba01b)![image](https://github.com/AtomSteve/Network-File-Shares-and-permissions/assets/147112183/0f6bf26f-326f-4773-94c6-fa2f63e3f227)




</p>

<h2>Attempt to access file shares as a normal user</h2>

On DC-1 in the read folder create a document and save it there. On Client-1 go to start button and run \\dc-1 and you should see the folder you made on DC-1.  Notice that you can access only a few of them, access the read folder and open the document you made.  Notice you can only read not edit

</p>
<br />

![image](https://github.com/AtomSteve/Network-File-Shares-and-permissions/assets/147112183/27358940-277e-4be7-83e9-f9211e2fc73f)![image](https://github.com/AtomSteve/Network-File-Shares-and-permissions/assets/147112183/41a73cf3-21ef-4450-8a93-435be4569ea5)



</p>

<h2> Create an "ACCOUNTANTS" Security Group, assign permissons, an test access</h2>

In Active Directory in DC-1, under my domain create a Security group.  right click mydomain -> new -> Orginizational Unit -> call it SECURITY GROUP.  In the new Security group Add new group called ACCOUNTANTS and make the type security, after go to ACCOUNTANTS folder and go to properties and Add ACCOUNTANTS Security group and set it to read and write.   No one can access the ACCOUNTANTS folder, so go back to Security groups in Active directory go to members and Add as many people to the group as you need.  Once one of your user has access to the ACCOUNTANTS, have them sighn into Client-1.  You should be able to access the ACCOUNTANTS folder now.  Now you can share and restrict data from users 

</p>
<br />

![image](https://github.com/AtomSteve/Network-File-Shares-and-permissions/assets/147112183/cefd9511-bb1f-4e0f-80ec-8b6799b71e0e)![image](https://github.com/AtomSteve/Network-File-Shares-and-permissions/assets/147112183/00336bf8-ea64-4dea-a947-25231c3a06ea)![image](https://github.com/AtomSteve/Network-File-Shares-and-permissions/assets/147112183/3d048d00-7e51-440b-8b0a-d9f20250b0da)![image](https://github.com/AtomSteve/Network-File-Shares-and-permissions/assets/147112183/30c50197-32fc-41d8-b43f-21c78a020af5)![image](https://github.com/AtomSteve/Network-File-Shares-and-permissions/assets/147112183/b7aef976-83a9-4dc1-b329-fe0914a5aaa7)






