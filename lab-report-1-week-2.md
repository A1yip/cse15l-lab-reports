# Week 2 Lab report
---
## Step 1: Installing Visual Studio Code
![e1](https://user-images.githubusercontent.com/103228609/162645693-9b5d2363-0ef8-40c7-9724-7fff17e1ab17.png)
* The first step towards remote access is installing Visual Studio Code which allows us to connect to a remote host.
* The most important method which we do so is through the terminal where we can input the commands necessary to connect remotely from our computer.

## Step 2: Remotely Connecting 
* To begin remotely connecting we have to enter the following command in the terminal: ssh cs15lsp22zz@ieng6.ucsd.edu where "zz" represents our course specific account
* After that the terminal will prompt us to verify the authenticy of the host we are connecting to which we type "yes" and then it will prompt us for our password for the course specfic account


![e2](https://user-images.githubusercontent.com/103228609/162646058-4d48b98e-5539-4650-8516-e0a1681138b8.png)
* When we do so, we should get this showing up on our terminal which means we successfully connected to the remote host.

## Step 3: Commands
![e3](https://user-images.githubusercontent.com/103228609/162646256-cb3c7f9c-64a1-492b-87c0-737d13f3daef.png)
* The command ls allows us to list the files within our current directory but notice how when we try to access the list of files for another persons account, our permission is denied
* There are also other commands such as "cd" which allows us to change our directory to make our search more specific and appending "..." to "cd" allows us to backtrack and go back directories

## Step 4: Moving files with "scp"
* The command "scp" allows us the copy files from our local host to a remote host which can be seen in this image
![e4](https://user-images.githubusercontent.com/103228609/162646561-ccff7921-3531-474d-bdf7-6845c321a279.png)
* The keys typed after the colon represent the directory we want to copy the file to, in this case bein the home directory.
![e5](https://user-images.githubusercontent.com/103228609/162646827-e0aa8f71-7648-4079-b072-ebe1b959306d.png)
* We can see that after copying the file to our remote host, when we access the list of files the file we just copied is there and when we run the java file, it prints out the specifications of the remote host rather than our local host.

## Step 5: SSH keys
* In order to avoid typing in our password everytime we wanted to access our remote host, we can create an ssh-keygen which allows us to save our password into our local system so that we can login without typing in our password.
![e6](https://user-images.githubusercontent.com/103228609/162647191-30f12ea2-149a-495d-b4d8-039ee702a3fe.png)
* As we can see when I tried logging into the remote host, the terminal did not prompt for my password input and just automatically connected me in when I typed the ssh command to access the remote host.
* This is because the password is saved in a separate file in the .ssh directory inside our local device and it inputs the password when its needed.

## Step 6: Optimized Remote Running
* Remote running can be optimized by separating command lines with semicolons and running on the same line as the command to remotely access
![e8](https://user-images.githubusercontent.com/103228609/162651027-fcc8f77e-2e84-45ed-aebc-e225efab0b38.png)
* As we can see here we are able to run those commands on the remote system immediatedly and in succession with a single line and it even closes out of the remote access after its finished
---
