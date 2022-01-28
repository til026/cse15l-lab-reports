# MarkdownParseTest
## Code Change 1: Fix when no bracket or parenthesis 
![Image](change1.png)
Here's the test leading the change:[failure inducing input 1](https://github.com/til026/cse15l-lab-reports/edit/main/failure-inducing-input1.md)

Running the original file outputs this:
![Image](output1.png)

Bug in original file is that it will breakdown if there's no bracket or parenthesis as the method ```indexof()``` will output ```-1``` in the while loop.

I created a testfile that doesn't contain any bracket or parenthesis but with only a title, it correctly shows the symptom that throw a ```StringIndexOutOfBoundsException```.

The adding line allows me to break the while loop without ```StringIndexOutOfBoundsException``` if there's no bracket and parenthesis.

After changing the code, the output is ```[]```, correct.
## Code Change 2: Fix printing images and non-link with text between brackets and parenthesis
![Image](change2.png)
Here's the test leading the change: [failure inducing input 2](https://github.com/til026/cse15l-lab-reports/edit/main/failure-inducing-input2.md)

Running the original file outputs this:
![Image](output2.png)

Bug in last version of file is that it cannot distinguish image from links, and it cannot distinguish those fake links with some texts between ```]``` and ```(```.

I created a testfile that contains a image and a fake link with some texts in between 
```]``` and ```(```, it prints the false output as I expected. 

After changing the code, the output is ```[]```, correct.
## Code Change 3: Fix link with "]" in link's name
![Image](change3.png)
Here's the test leading the change: [failure inducing input 3](https://github.com/til026/cse15l-lab-reports/edit/main/failure-inducing-input3.md)

Running the original file outputs this:
![Image](output3.png)

Bug in last version of file is that it will misunderstand a link with ```]``` in the link's name as a fake link, thus not printing it.

I created a testfile that contains a real link ```[canvas[]link](www.canvas.com)``` which will be regarded as a fake link thus not being printed. It prints the false output ```[]``` as I expected.

After changing the code, the output is ```[www.canvas.com]```, correct.
