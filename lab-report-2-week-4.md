# Lab Report 2  
## by Michael Ma
1. Change 1 (By Michael Ma)
![Image](images/error1.png)     
[Failure Inducing Input](https://github.com/ucsd-cse15l-w22/markdown-parse/blob/2c9300a80518830d534650fc765f4731e4f1c2e9/test-file2.md)  
Symptom: 
The program went in infinite loop.     
The output is as the following screen shot.  
![Image](images/out1.png)     
The bug is caused by, if there texts after the last link, the indexOf method searching for open brackets would return -1, since there are no open brackets after the last link.However, the next indexof method, which search for close brackets, would not return -1, since it just wrap up to the beginning of the file, and search after -1. So a infinite loop would occur.   
Sympton is nothing will be printed until the stack memory were used up.  
The failuare inducing input have texts after the second link parentheses, which would cause the bug.  
Here we could fix this bug by adding a if statement to determine whether there is a open bracket after the start  index. If -1 is detected, it means there are no open parentheses exists after the current start index, so we just break the while loop.  

2. Change 2 
![Image](images/error2.png)   
[Failure Inducing Input](https://github.com/ucsd-cse15l-w22/markdown-parse/blob/2c9300a80518830d534650fc765f4731e4f1c2e9/test-file3.md)  
Symptom:   
The StringIndexOutOfBoundsException is thrown.  
The output is as the following screen shot.  
![Image](images/out2.png)     
The bug is caused by, if there are no () followed by [], the indexOf method would return -1 when searching for "(" and ")". So the substring method would take index as -1, which is not allowed. So the exception is thrown. 
The sympton is exception is thrown.  
The faluare unducing input have no () so the indexOf method would return -1, which cause the exception to be thrown.  
We could fix this problem by adding another if statement to determine whether the open parentheses exist. If not,  i.e.  the indexof method return -1, we would break, instead of calling the substring method.  

3. Change 3 (By Takuro Kitazawa)  
![Image](images/change3.png)   
[Failure Inducing Input](https://github.com/audreyfishy/markdown-parse/blob/a755c0298943680d8902cdeb2fa4a30957a3eace/breaking.md)  
Symptom:   
When there are no closing parentheses but have a open parentheses, the indexoutofbound exception would be thrown.  
The output is as the following screen shot.  
![Image](images/output3.png)     
The bug is caused by, if there are no closing parentheses , the indexOf method would return -1 when searching for ")". So the second paramenter of the substring method would take index as -1, which is not allowed. So the exception is thrown. (Really a same issue with the previous one)
The sympton is exception is thrown.  
The faluare unducing input have no ) so the indexOf method would return -1, which cause the exception to be thrown when calling the substring method.  


