# Lab Report 1

## Step 1: Installing VSCode

In order to do this lab, you first need to install VSCode onto your computer, and additionally install Git if you are using Windows.

1. Install [VsCode](https://code.visualstudio.com/download)
![Image](images/LR1Image1.PNG)

2. Download [Git](https://gitforwindows.org/) for Windows if on a Windows machine
3. Open a VSCode window

## Step 2: Remotely Connecting

After installation, you need to remotely connect to the UCSD ieng6 server using your lab email

1. Go to [https://sdacs.ucsd.edu/~icc/index.php](https://sdacs.ucsd.edu/~icc/index.php) in order to look up your lab email information, and if it is your first time you must activate your account by resetting your password. 
2. Once your email password is changed, open VSCode.
3. On the top, click Terminal -> New Terminal and then type in `ssh cs15lwi23(your course specific letters here like aa)@ieng6.ucsd.edu`. You will be prompted to enter your password (When you type in your password, it will look like nothing is being inputted, but it is actually just invisible for security purposes)
![Image](images/LR1Image2.png)

## Step 3: Trying Some Commands

Once you are connected, you can try out some commands in the command line. I learned that using `ls -lat` will list all the files according to date. I also learned that 
-lat actually means combining flags like -l and -t.

1. Explore your current directory by typing `ls`, or `ls -F`, or `ls -a`
2. Try out other commands such as `mkdir`, `cd`, `pwd`.
3. Try combining some commands such as using `ls -lat`
![Image](images/LR1Image3.png)
