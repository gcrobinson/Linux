# File Permissions in Linux
<br />
<h2>Description</h2> 

The research team at my organization needs to update the file permissions between _**user**_, _**group**_, and _**other**_ because the permissions do not reflect the level of authorization that should be given for certain files and directories within the _projects_ directory. Updating permissions in the file system helps to keep systems secure. I perfomed the following tasks:

<br />

 <h2>Check file and directory details</h2>
Here is how I used linux commands to determine the existing permissions set for a specific directory in the file system. 

<p align="center">
  <br />
<img src= "https://i.imgur.com/fNSPNvi.png[/img]" alt="ls -la command"/>

Here I used the **ls -la** command which lists all the contents in the _projects_ directory including hidden files.  The first column output with the 10-character strings shows all permissions. Next is one directory named ***drafts*** indicated by the _d_ character string, one hidden file under the name ***.project_x.txt*** indicated by the **"."** symbol, and five other project files. 

<br />

<h2>Change file permissions</h2>
The organization determined that 
_shouldn't have _write_ access to any of their files. I determined project_k.txt must have the write access removed for other 
<br />
<p align="center">
  <br />
<img src= "https://i.imgur.com/8NuhF24.png[/img]" alt="chmod code write permissions removed from other"/>

 The chmod command changes the permissions on files and directories. The first argument indicates what permissions should be changed, and the second argument specifies the file or directory. In this example, I removed write permissions from other for the project_k.txt file. After this, I used ls -la to review the updates I made.


 <br />
<p align="center">
  <br />
<h2>Incident report analysis:</h2>
<p align="center">
<img src="https://i.imgur.com/QyKLcQA.png[/img]" alt="incident report analysis"/>

<p align="center">
    <img src="https://i.imgur.com/VskWBIt.png[/img]" alt="incident report analysis"/>
<br />
<br />
