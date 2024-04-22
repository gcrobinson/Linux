# File Permissions in Linux
<br />
<h2>Description</h2> 

The research team at my organization needs to update the file permissions between _**user**_, _**group**_, and _**other**_ because the permissions do not reflect the level of authorization that should be given for certain files and directories within the _projects_ directory. Updating permissions in the file system helps to keep systems secure. 
<p align="center">
  <br />
<img src= "https://i.imgur.com/qNYsnMl.png[/img]" alt="projects directory"/>
 <br />
First I navigated to the projects directory and then I perfomed the following tasks:

<br />

 <h2>Check file and directory details</h2>
Here is how I used linux commands to determine the existing permissions set for a specific directory in the file system. 

<p align="center">
  <br />
<img src= "https://i.imgur.com/ToZegDn.png[/img]" alt="ls -la command"/>

Here I used the **ls -la** command which lists all the contents in the _projects_ directory including hidden files.  The first column output with the 10-character strings shows all permissions. Next is one directory named ***drafts*** indicated by the _d_ character string, one hidden file under the name ***.project_x.txt*** indicated by the **"."** symbol, and five other project files. 

<br />

<h2>Change file permissions</h2>
The organization determined that other shouldn't have write access to any of their files. I determined project_k.txt must have the write access removed for other.
<br />

<p align="center">
  <br />
<img src= "https://i.imgur.com/CZj7zMA.png[/img]" alt="chmod code write permissions removed from other"/>

 The ***chmod*** command changes the permissions on files and directories. The first argument indicates what permissions should be changed, and the second argument specifies the file or directory. In this example, I removed _write_ permissions from _other_ for the project_k.txt file. After this, I used **ls -l** to review the updates I made.

<br />

<h2>Change file permissions on a hidden file</h2>

The research team at my organization recently archived project_x.txt. They do not want anyone to have write access to this project, but the user and group should have read access. Here the archived file has a (.) symbol to indicate it is a private file.

<br />

<p align="center">
<img src="https://i.imgur.com/H4YiHIP.png[/img]" alt="removing and adding permissions from group and user"/>
 
 The first two lines of the screenshot display the commands I entered, and the other lines display the output of the second command. I removed write permissions from the user with **u-w**. Then, I removed write permissions from the group with **g-w**, and added read permissions to the group with **g+r**. 

 <br />
 
<h2>Change directory permissions</h2>

My organization only wants the researcher2 user to have access to the drafts directory and its contents. This means that no one other than researcher2 should have execute (x) permissions.
 
<p align="center">
<img src=https://i.imgur.com/6GCHFkw.png[/img]" alt="removing and adding permissions from group and user"/>
 
Line 4 is the directory, _drafts_, with restricted permissions. Here you can see that only researcher2 now has execute permissions.  It was previously determined that the group had execute permissions, so I used the **chmod** and **(-)** commands to remove them. The _researcher2_ user already had execute permissions, so they did not need to be added.

<h3>Summary</h3> 
I changed multiple permissions to match the level of authorization my organization wanted for files and directories in the projects directory. The first step in this was using ls -la to check the permissions for the directory. This informed my decisions in the following steps. I then used the chmod command multiple times to change the permissions on files and directories.
