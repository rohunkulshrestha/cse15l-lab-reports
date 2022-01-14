# Logging into ieng6 #
Rohun Kulshrestha
***
## Step One: Instaling VSCode ##
Download Visual Stuido Code from this [Link](https://code.visualstudio.com) and install it to your computer. When it is finished installing, open it and start setting it up by downloading any extension packs you think you might need. Some examples include:
* Java Packs
* Themes
* GitHub Packs

Once setup, your screen might look like this:

![Image](VSCodepic.PNG)
From here you can open a folder to begin working on files by clicking the icon next to the "Open Editor" header.
***
## Step Two: Working Remotely ##
In order to move files from your computer to a server, the first thing we will need to do is install OpenSSH [here](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse). Once downloaded, open Visual Studio (if not already open) and create a new terminal (reference image for help).

![Image](VSCodepic2.PNG)
Once opened, go to [this link](https://sdacs.ucsd.edu/~icc/index.php) to look up your course-specific account for CSE15L. Then, go back to the terminal and enter this command to connect to the server:
```
ssh cs15lwi22zzz@ieng6.ucsd.edu
```
> NOTE: you would type your three letters in your account instead of "zzz"
 
 You may also be prompted with a message regarding security if this is the first time you are connecting. Just type "yes" to continue. If you are asked this again while connecting to the same server, there could be cause for concern. But for now there should be nothing to worry about. From there, you should be seeing a screen *similar* to the one below.

 ![Image](remotepic.PNG)
 ***
## Step Three: Trying Some Commands ##
Once set up in the server, try running some of these commands that provide some interesting information :
* cd ~
* cd
* ls -lat
* ls -a
* type "exit" to log out of the remote server or 'CTRL + D'

An example of the 'ls -lat' command

![Image](comman.PNG)
***
## Step Four: Moving Files with SCP ##
Now we will try sending over a copy of a file from our computer to a remote computer using the "SCP" command. This command will alwyas be ran on the client - the computer not logged into ieng6. To test this command out, begin by creating a new file on your computer called "WhereAmI.java" and past the following code into it:
```
class WhereAmI {
  public static void main(String[] args) 
  {
    System.out.println(System.getProperty("os.name"));
    System.out.println(System.getProperty("user.name"));
    System.out.println(System.getProperty("user.home"));
    System.out.println(System.getProperty("user.dir"));
  }
}
```
run it using the "Javac" and "Java" commands and note the output.
Now we will copy it to the server using this command:
```
scp WhereAmI.java cs15lwi22zzz@ieng6.ucsd.edu:~/
```
remember to replace "zzz" with your course-specific letters
>NOTE: You may be prompted to enter your password

Once copied to the server, log into ieng6 using the steps from above and type in the "ls" command. You should see the file there in the directory similar to the picture below.

![Image](scp.PNG)
 Now, once again, run the "Javac" and "Java" commands on the server and note the difference in the output. You have succesfully copied a file to the server, congrats!
 ***
 ## Step Five: Setting an SSH Key
 