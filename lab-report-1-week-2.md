# Toturial for incoming cse15L students
## Step 1: Installing VScode
1. Open the [VScode Official Website](https://code.visualstudio.com/) on your computer, choose the correct version that correspond to your computer and download.
![Image](vscode1.png)
2. After successfully dowload and install the VScode, it should look like this
![Image](vscode2.png)
---
## Step 2: Remotely Connecting
1. Go to [https://sdacs.ucsd.edu/~icc/index.php](https://sdacs.ucsd.edu/~icc/index.php) to look up for your cse15L sepcific account. You should reset your password to active this account.(**Remember don't change all of your passwords!**)
2. Open a terminal in your VScode then type ```ssh cs15lwi22ait@ieng6.ucsd.edu``` in your terminal. *ait* here is specific to my account, you should change ```ait``` with your own username for cse15L.
3. If it is your first login, you may asked whether you want to keep connecting. Answer **yes** for the question. If you don't see the question, just regard this step.
4. Now your computer is successfully connected to the remote server and it should look like this.
![Image](vscode3.png)
## Step 3: Trying Some Commands
You search some commands on the internet and type it into your terminal.
Here's the commands I tried:
```
ls
ls -a
cd
cd ~
pwd
```
Here's the result:
![Image](vscode4.png)
## Step 4: Moving Files with scp
1. Create an example java file WhereAmI.java
The code should like this:
```
class WhereAmI {
  public static void main(String[] args) {
    System.out.println(System.getProperty("os.name"));
    System.out.println(System.getProperty("user.name"));
    System.out.println(System.getProperty("user.home"));
    System.out.println(System.getProperty("user.dir"));
  }
}
```
2. Use javac and java to compile and run the java file on your computer and see the outcome:
![Image](vscode5.png)
3. Type ```scp WhereAmI.java cs15lwi22ait@ieng6.ucsd.edu:~/``` in your terminal, then login into your server and run javac and java command on your server to see what's happening:
![Image](vscode6.png)

## Step 5: Setting an SSH Key

## Step 6: Optimizing Remote Running
