# ieng6 tutorial for cse15l  
![Image](https://ucsdnews.ucsd.edu/news_uploads/Resized_Geisel_Library_08.31.jpg)   

---  
## Step 1: Installing VScode  
* Go to the Visual Studio Code website [https://code.visualstudio.com/](https://code.visualstudio.com/) to install VScode on your computer.   

![Image](https://raw.githubusercontent.com/Hexachlorocyclohexane3088/cse15l-lab-reports/main/step1.png)   

---  
## Step 2: Remotely Connecting  
* If you're on Windows: install [OpenSSH](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse)  
* Then, look up your course-specific account for CSE15L here: [https://sdacs.ucsd.edu/~icc/index.php](https://sdacs.ucsd.edu/~icc/index.php)  (You need to change your local password for the first time.)  
![Image]()  

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
![image]()  
* Now you have seccessfully login to ieng6!


---  

## Step 3: Trying Some Commands  


---  

## Step 4: Moving Files with `scp`  


---  

## Step 5: Setting an SSH Key  


---  

## Step 6: Optimizing Remote Running  


---  

