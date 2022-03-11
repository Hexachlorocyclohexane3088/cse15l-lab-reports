# Lab Report 5  
## by Michael Ma
**Different Bugs**  
Link to [My markdown-parse repository](https://github.com/Hexachlorocyclohexane3088/markdown-parse1) 

So first we create a directory and clone my repo and the given repo, using same strategy we did in lab9.   

## Run the Tests   
In which repo the script is given. Here markdown-parse is the given repo, while markdown-parse1 is my own repo.  
Add a line `echo $file` in `script.sh`(using vim), like we did in lab9, so that it is easier for us to find which test an output is correspond to.  
Enter the directory and run `make` and `bash script.sh > results.txt`, after a while we got the output storing in a new file named "results.txt".  
Then we go back to the home directory to move test files and the script to our repo.  
```
cd ~  
#copy test-files  
cp -r report10/markdown-parse/test-files report10/markdown-parse1/  
#copy script.sh  
cp -r report10/markdown-parse/script.sh report10/markdown-parse1/  
```
Enter the  markdown-parse1 (my repo), and run `make` and `bash script.sh > results.txt`.  
Now the tests have been run in my repo as well.  
## Compare the results  
Go back to home directory and use the `diff` to compare results:  
```
diff markdown-parse/results.txt markdown-parse1/results.txt > diff.txt 
```
The result is then stored in a txt file with name `diff.txt`:  
![image](images/repo5_result1.png)
![image](images/repo5_result2.png)
![image](images/repo5_result3.png)
We would like to examine the first two differences:  
![image](images/repo5_twoDiff.png)
## First test 
The corresponding to file `201.md`(we could look for that using `cat`). 
The content in `201.md` is 

We could use [the CommonMark demo site](https://spec.commonmark.org/dingus/) to determine the correct output. 
We could figure out that nothing is parsed, so the correct output should be 
```
[]
```
The given 

## Thank you for reading!  
![Image](https://ucsdnews.ucsd.edu/news_uploads/Resized_Geisel_Library_08.31.jpg)   