# Lab Report 3
## Week 6

## Copy Whole Directories with ```scp -r```
![Image](Week6LRSS1.png)

## Markdown-parse directory to ieng6
![Image](Week6LRSS2.png)
* Usaully adding files in a large directory to a remote server would be tedious as you would have to ```scp``` each one into the remote severe. Howver with certian commands yu can do this quiclky taign advatage of recursion. The command is ```scp -r . cs15lwi22@ieng6.ucsd.edu:~/markdown-parse``` (of course with your own user name) the ```-r ``` represents  the recursive lemtn of the program and the ```.``` repsresnt the current directory you want to copy over. 

## Running Newly Coppied Tests
![Image](Week6LRSS3.png)
* In this example you can see what it looks like when the recursion is running and copying everything to the remote server. If you look closely I try to compile the tests and it fails why might this be? If you guessed that it was i didnt complie using the lib that contians the Junit necessities you would be correct. In the next example you will see how this done correctly using right comannds.(```javac -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar MarkdownParseTest.java```, ```//java -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar org.junit.runner.JUnitCore MarkdownParseTest```)

## Combining ```scp```, ```;```, and ```ssh``` for Optimization 
![Image](Week6LRSS5.png)
![Image](Week6LRSS4.png)
* In this next example we see a way to optimize this whole process doing int in one line. Using this lien of code ( ```scp -r . cs15lwi22zzz@ieng6.ucsd.edu:~/markdown-parse; ssh cs15lwi22acm@ieng6.ucsd.edu; javac -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar MarkdownParseTest.java; java -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar org.junit.runner.JUnitCore MarkdownParseTest```) we are able to submit the directoy recursively then automatically compile it and run it passign the test cases. the key to this is using the ```;``` as it allows for mutiple comands in one line.

[Back To Home Page](https://jrhowell123.github.io/cse15l-lab-reports/)