# CSE 15L Lab 1 Report

Welcome to CSE 15L. In this tutorial, you will learn how to install VSCode, how to remotely connect to a remote computer and some useful bash commands. 

## Step 1: Installing Visual Studio Code
First, go to [the official VSCode website](https://code.visualstudio.com/) and download the installer that corresponds to your operating system

<img src="lab1_pic1.png"
     alt="Markdown Monster icon"
     style="float: left; margin-right: 10px;" />
     
     
Once the installation is over, you will be greeted with a page that looks similar to the following screenshot. Note that depending on your system settings, the background color/fonts may be vary

<img src="lab1_pic2.png"
     alt="Markdown Monster icon"
     style="float: left; margin-right: 10px;" />

## Step 2: Setting up bash and connecting remotely using ssh (secure shell)
First, make sure that you have git installed. In Windows, a quick way of checking is by pressing Win + R to open the run tab and then typing in cmd to open the command prompt. Once the command prompt is open, type in git and hit enter.  If a list of commands shows up, it means that git is most likely installed in your computer. If you get anything along the lines of *'git' is not recognized as an internal or external command, operable program or batch file*, then you will have to install git. <br />

<img src="lab1_pic3.png"
     alt="Markdown Monster icon"
     style="float: left; margin-right: 10px;" /> <br />

  <br />
<img src="lab1_pic4.png"
     alt="Markdown Monster icon"
     style="float: left; margin-right: 10px;" /> <br />
     
To install git, go to [this page](https://gitforwindows.org/) to download the installer. <br />
 
 
Once git is installed in your computer, follow [this StacKOverflow post on how to use bash in the VSCode terminal.](https://gitforwindows.org/)
Now that bash is setup, you are ready to remote connect. Input ```ssh cs15lsp23zz@ieng6.ucsd.edu``` in the terminal, where the *zz* are replaced by the letters of your course account ([go to the account lookup page to setup your account](https://sdacs.ucsd.edu/~icc/index.php)). 
After this, you will be asked to input a password. This is the same password you chose when you setup your CSE 15L account <br />

<img src="lab1_pic5.png"
     alt="Markdown Monster icon"
     style="float: left; margin-right: 10px;" /> <br />
     
If all goes well after you input the password, you would see something similar to this in the terminal <br />
<img src="lab1_pic6.png"
     alt="Markdown Monster icon"
     style="float: left; margin-right: 10px;" /> <br />
This means that you are now remotely connected! <br />

## Step 3: Running a few commands
Here are a few interesting commands to try out. For a comprehensive list, consider looking [at this website](https://www.freecodecamp.org/news/bash-scripting-tutorial-linux-shell-script-and-command-line-for-beginners/) <br />

1) pwd. Shows the current working directory <br />
<img src="lab1_pic7.png"
     alt="Markdown Monster icon"
     style="float: left; margin-right: 10px;" /> <br />
     
2) ls. Lists the contents of the current directory <br />
<img src="lab1_pic8.png"
     alt="Markdown Monster icon"
     style="float: left; margin-right: 10px;" /> <br />
     
3) mkdir <your directory's name>. Create a new directory <br />
<img src="lab1_pic9.png"
     alt="Markdown Monster icon"
     style="float: left; margin-right: 10px;" /> <br />
     
4) cd <your directory's name>. Change directory <br />
<img src="lab1_pic10.png"
     alt="Markdown Monster icon"
     style="float: left; margin-right: 10px;" /> <br />
