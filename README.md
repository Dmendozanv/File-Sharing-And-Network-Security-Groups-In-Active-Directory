<h1>File Sharing and Network Security Groups In Active Directory</h1>
In this tutorial, we create files with certain permissions that can be shared between certain users. We create a new network group that can also access certain files.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Windows 2022 Server
  
<h2>Setup</h2>

Create two Virtual Machines, with one of them being the Domain Controller (DC-1) and the other being (Client-1). The DC-1 VM will be on a Windows 2022 Server and the Client-1 will be on Windows 10. (See Active Directory Repository).
<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/VDFzoJX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/238yZQW.png" height="80%" width="80%"/>
</p>
<p>
First, create four different files in DC-1 "read-access", "write-access", "no-access", and "accountants". Then for each file go into properties and sharing to add each permission to the selected files as well as the groups that have these certain access.
</p>
<br />

<p>
<img src="https://i.imgur.com/ebS8r41.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now if you go into Client-1 and try and access accountant file as "jane-admin" you will notice that the action is blocked because they are not a part of this security group. However, if you try and access the admin file you can see that you do have access to that one because jane_admin is part of the admin group.
</p>
<br />

<p>
<img src="https://i.imgur.com/MfNAJzV.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/rLYtPU3.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/XLzIPzL.png" height="600%" width="60%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/jOk5ype.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Now create an ACCOUNTANT Network Group in Active Directory and add a random user into that group. You can now access this file when you log in to Client-1 as that user.
</p>
<br />

<h2>Final Thoughts</h2>

<p>Now you can see how to add different access to different files when sharing under a Domain Controller. You can also create Network Groups within Active Directory and organize users into those groups. </p>
