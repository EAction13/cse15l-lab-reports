# Week 1 Lab Report
## Installing VS Code
Go to https://code.visualstudio.com/ and download the file appropriate for your operating system.

![image](https://user-images.githubusercontent.com/122485081/211909937-fb38f784-9d34-4062-bda6-9337d152b361.png)

## Using Git Bash on Windows
First, install Git for windows from https://gitforwindows.org/.
Next, open VS Code and open up a terminal as shown in the image below.

![image](https://user-images.githubusercontent.com/122485081/211910261-0827dde6-0400-4291-90a5-3c70c60584b4.png)

Go to the + icon on the bottom right of the screen and select Git Bash.
This will open a Git Bash terminal.

![image](https://user-images.githubusercontent.com/122485081/211910881-6e72a634-8807-4632-8483-3cab30495b58.png)

## Remotely connecting
Open the Git Bash terminal in VS Code. Then use the following command to connect to the ieng6 server:
`$ ssh cs15lwi23***@ieng6.ucsd.edu` where *** is unique to your CSE15L account.

You can find your unique CSE15L account [here](https://sdacs.ucsd.edu/~icc/index.php). Look up your account using your username and PID (with a lowercase 'a'). Under the "additional accounts" header, click on the button representing your 15L account. You can then change your password by entering your curent password and the new password. Without clicking "check password," simply click inside the "confirm password" text box, and press enter.

Agree to continue connecting, and enter your password. Then you will be connected to the server.

![image](https://user-images.githubusercontent.com/122485081/211911943-a1ffee11-c86f-4cdd-a44b-8e03dc39e878.png)

## Trying some commands
These are the commands I tried.

First, I tried changing directory to the home directory with `$ cd ~`. Then I displayed the current directory with `$ pwd`. Unchanging from when the directory was displayed above, I was in /home/linux/ieng6/cs15lwi23/cs15lwi23aju, but this now confirmed that it was the home directory.

I then tried a few commands suggested on the course site. `$ ls -lat` gave what seemed to be a list of files with dates, while `ls -a` seemed to only show the files without extra data.
![image](https://user-images.githubusercontent.com/122485081/211912119-f7d5fb1d-535b-4761-9125-3a62e6aeb5c5.png)

Afterwards, I also tried to use ls to show another student's files by writing out the path to their directory, but my permission was denied.

It seems that each student is given their own home directory, and each student is unable to access the other students' directories.
