# Lab Report 4  
## by Michael Ma
**Code Review**  
Link to [My markdown-parse repository](https://github.com/Hexachlorocyclohexane3088/markdown-parse1) and a link to [the one we reviewed](https://github.com/aajc/markdown-parse)  
Code used for testing: (Commenting off the tests methods that are not using each time before run the test)
![code used for testing](images/testcode.png)
Unfortunately none of the tests passed.  
## Snippet 1
```
`[a link`](url.com)

[another link](`google.com)`

[`cod[e`](google.com)

[`code]`](ucsd.edu)
```
**Excepted ouput:**  
```
["`google.com","google.com","ucsd.edu"]
```
**Other group output:**  
![image](images/otheroutput_1.png)  
**My out put:**   
![image](images/myoutput_1.png)  
It is not possible to fix my program within 10 lines. 
There are two aspected we need to fix: find the "](" instead of just "]", and the problem of code block. 
We could fix the code block by adding something like that: 
```
int codeStart = markdown.indexOf("`", currentIndex);
if (codeStart < nextOpenBracket && codeStart != -1) {
    int codeEnd = markdown.indexOf("`", codeStart + 1);
    currentIndex = codeEnd + 1;
    continue;
}
```
So the first invalid link would be disgarded. But it would still cause the last link "ucsd.edu" to be dismissed, since we need additional work  to do to match "](", which is not likely to be complete in 10 lines.  
## Snippet 2
```
[a [nested link](a.com)](b.com)

[a nested parenthesized url](a.com(()))

[some escaped \[ brackets \]](example.com)
```
**Excepted ouput:**  
```
["a.com","a.com(())","example.com"]
```
**Other group output:**  
![image](images/otheroutput_2.png)  
**My out put:**  
![image](images/myoutput_2.png) 
This is also not possible to fix the bug within 10 lines.  
We need to deal with two bugs: nested "()" and still, matching ")[".  
Only to fix the first bug, we could add a method: 
```
public static int findClose(String markdown, int start) {
    if (markdown.indexOf(")", start) == -1) {
        return -1;
    }
    int cnt = 1;
    int curr = start;
    while (cnt > 0) {
        curr++;
        if (curr >= markdown.length()) {
            break;
        }
        if (markdown.charAt(curr) == ')') {
            cnt--;
        }
        if (markdown.charAt(curr) == '(') {
            cnt++;
        }
    }
    return curr;
}
```
And change the closeParen to be: 
```
int closeParen = findClose(markdown,openParen);
```
So the "a.com(())" would be parsed correctly.   
But "example.com" could not be parsed until we fix the ")[" and nested bracket problem (here we only deal with nested parenthese). 10 lines is not possible.  
## Snippet 3
```
[this title text is really long and takes up more than 
one line

and has some line breaks](
    https://www.twitter.com
)

[this title text is really long and takes up more than 
one line](
    https://ucsd-cse15l-w22.github.io/
)


[this link doesn't have a closing parenthesis](github.com

And there's still some more text after that.

[this link doesn't have a closing parenthesis for a while](https://cse.ucsd.edu/



)

And then there's more text
```
**Excepted ouput:**  
```
["https://ucsd-cse15l-w22.github.io/"]
```
**Other group output:**  
![image](images/otheroutput_3.png)    
**My out put:**  
![image](images/myoutput_3.png)  
It is also not possible to fix within 10 lines, since we need to deal with at least four works: 
1. when there exist new line in brackets, continue; 
2. when there are one new line in the back of the link, eliminate the new line;
3. when there are more than one new lines in the back of the link, continue;
4. fix the infinite loop of missing ")". 


## Thank you for reading!  
![Image](https://ucsdnews.ucsd.edu/news_uploads/Resized_Geisel_Library_08.31.jpg)   