# Lab Report 1
## Step 1

Make sure to install Visual Studio Code. Go to this link: [VS Code Download](https://code.visualstudio.com/download) and download the correct
version based on your operating system. I already have VS Code downlaoded, however, after the download, install and open VS Code, and you'll have
something that looks like this below.

![VS Code Screenshot](VS Code Screenshot.png)

## Step 2

The next step is to remotley connect to our server. The first thing to do is install OpenSSH here: [Install OpenSSH](https://learn.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse?tabs=gui) If you are running on Mac like me, theres no need to install OpenSSH and you can proceed. Open Visual Studio Code and type `ssh cs15lfa22ba@ieng6.ucsd.edu`. 
You will get a message since it is your first time connecting to the server so just type `Yes` and hit Enter. After some time, you will get a screen that looks like this below.
![Remote Connection Screenshot](Remote Connection Screenshot.png)

## Step 3

Next, try some commands. While logged into the ssh server try the command `cp /home/linux/ieng6/cs15lafa22/public/hello.txt ~/`, then right after print out the contents of hello.txt by entering the command `cat /home/linux/ieng6/cs15lfa22/public/hello.txt` After this, you will get something in your terminal that looks like this below.
![Commands Screenshot](Commands Screenshot.png)

## Step 4
