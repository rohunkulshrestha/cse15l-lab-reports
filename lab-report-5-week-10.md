# Week 10 Lab Report
Rohun Kulshrestha

***

## Test One ##
For the first test, I chose file 512 by manually looking at the different files and their contents. Then I ran a couple that might produce different outputs, which led me to finding [512.md](512.md).

When I ran the test using my MarkdownParse, this was the output that was produced:

![image](testmain.PNG)

Versus when I ran the test using the provided MarkdownParse:

![image](testother.PNG)

As you can see, the two outputs are different, but I beilieve that the output produced by the provided MarkdownParse code is the expected output. The problem in my MarkdownParse may be occuring after the program is done finding the closed bracket. If you look back at the test, there is an additional closed bracket, which may be causing the program to produce this incorrect output. 

![image](codeOne.JPG)

As of now, the program really only accounts for one closed bracket; thus, the additional closed bracket is causing the program to produce the output we are seeing.




