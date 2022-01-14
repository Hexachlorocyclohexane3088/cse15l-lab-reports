# ieng6 tutorial for cse15l  
## by Michael Ma
![Image](https://ucsdnews.ucsd.edu/news_uploads/Resized_Geisel_Library_08.31.jpg)   
## Step 1: Installing VScode
---   
* Go to the Visual Studio Code website [https://code.visualstudio.com/](https://code.visualstudio.com/) to install VScode on your computer.   

![Image](https://raw.githubusercontent.com/Hexachlorocyclohexane3088/cse15l-lab-reports/main/step1.png)  

## Step 2: Remotely Connecting  
---  

* If you're on Windows: install [OpenSSH](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse)  
* Then, look up your course-specific account for CSE15L here: [https://sdacs.ucsd.edu/~icc/index.php](https://sdacs.ucsd.edu/~icc/index.php)  (You need to change your local password for the first time.)  
![Image](images/findPassword.png )  

* Open the terminal in VScode (to do this, Ctrl or Command + `, or use the Terminal → New Terminal menu option), type in the following command (ignore the dollar sign).  

```
 $ ssh cs15lwi22zz@ieng6.ucsd.edu
```
*Note: you need to change the* `zz` *with corresponding letters of your own account.*  

* Some wired message will appear the first time you login like this:  
```
⤇ ssh cs15lwi22zz@ieng6.ucsd.edu
The authenticity of host 'ieng6.ucsd.edu (128.54.70.227)' can't be established.
RSA key fingerprint is SHA256:ksruYwhnYH+sySHnHAtLUHngrPEyZTDl/1x99wUQcec.
Are you sure you want to continue connecting (yes/no/[fingerprint])? 
```
Just type `yes`, you will be fine. If everything went well, you will see the following message:  
![image](images/Step2_login_success.png )  
* Now you have seccessfully login to ieng6!

## Step 3: Trying Some Commands  
---  


You cannot open folders (or directories) by double clicking corresponding icons, like on your own computer, in ieng6. But you can access, upload, and download files by using commands. 

Now try the following commands, could you figuring out their functions? If you got stuck, you might find the answer [here](https://hackr.io/blog/basic-linux-commands).  

Please try:  

* `ls`  
* `ls -a`  
* `ls -lat`  
* `ls <directory>`  (`<directory>` is `/home/linux/ieng6/cs15lwi22/cs15lwi22zz`, replace `zz` with corresponding letters of your own account).  
* `cd`  
* `cd <directory>`  
*Discuss with your peers: could you ls the directory if you change your account letter to something else?* 
* `cp /home/linux/ieng6/cs15lwi22/public/hello.txt ~/`  
* `cat /home/linux/ieng6/cs15lwi22/public/hello.txt` 

To log out, you can use  `Ctrl + D` or run `exit`. 

## Step 4: Moving Files with `scp`  
---  
* Create a simple java file on your local desktop, like this:  





## Step 5: Setting an SSH Key  


---  

## Step 6: Optimizing Remote Running  


---  

