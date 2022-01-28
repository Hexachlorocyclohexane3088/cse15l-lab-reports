# Lab Report 2  
## by Michael Ma
1. Change 1 (By Michael Ma)
![Image](images/Michael.png)     
[Failure Inducing Input](https://github.com/ucsd-cse15l-w22/markdown-parse/blob/2c9300a80518830d534650fc765f4731e4f1c2e9/test-file2.md)  
Symptom: 
The program went in infinite loop.     
The output is as the following screen shot.  
![Image](images/MichaelOutPut.png)     
The bug is caused by, if there were nested parentheses and only one bracket the indexOf method would always search from the same position (the index of the closing bracket).    
Sympton is nothing will be printed and the program would not stop util we press ctrl+c to terminate the program manually.  
The failuare inducing input have only one bracket and two nested parentheses, which would cause the bug.  

2. Change 2 (By Michael Ma)
![Image](images/change2.png)   
[Failure Inducing Input](https://github.com/Hexachlorocyclohexane3088/markdown-parse1/blob/74ce7e545fce5ec3802c8443ed0abb155291626d/aNewFile.md)  
Symptom:   
When there are no () followed by [], the indexoutofbound exception would be thrown.  
The output is as the following screen shot.  
![Image](images/OUTPUT2.png)     
The bug is caused by, if there are no () followed by [], the indexOf method would return -1 when searching for "(" or ")". So the substring method would take index as -1, which is not allowed. So the exception is thrown. 
The sympton is exception is thrown.  
The faluare unducing input have no () so the indexOf method would return -1, which cause the exception to be thrown.  

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


