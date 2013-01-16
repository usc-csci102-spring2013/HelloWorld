HelloWorld
==========
Welcome to CS 102 on GitHub! Here, you will find code repositories for all lectures, labs and programming assignments. 

This is our obligatory Hello World _public_ repository. If you only see this repository under the [CS 102 GitHub Organization Account](https://github.com/usc-csci102-spring2013) This means that you are yet to be designated as a member of this organization. This process starts by you. All you need to do is provide your GitHub account username to your TA/CP and you will be added within the first week of classes.

In this course, we will using the following VirtualBox Appliance as the reference system for grading:
> http://ee-classes.usc.edu/cs101/cs102-vm.ova

This is an Ubuntu 12.04 LTS VM. You can login using:
  + Username: `cs102`
  + Password: `memory`

# Lab 01 – Exercises

## Git Setup
You need to setup git on every machine you plan to use for CS 102 this semester. This includes your own desktop/laptop(s) and the [course VM](http://ee-classes.usc.edu/cs101/cs102-vm.ova). The VM has git already installed. You do, however, still need to configure it.

### Download & Install Git
Start by downloading the latest [git](http://git-scm.com/) package from the official git website:
> http://git-scm.com/downloads

Installing the downloaded package should be straight forward.

If you are using `aludra.usc.edu`, run the following set of commands to install git on your account:
```shell
cp ~/.cshrc ~/.cshrc.backup
echo "" >> ~/.cshrc
echo "# Git Setup" >> ~/.cshrc
echo "source /usr/usc/git/default/setup.csh" >> ~/.cshrc
source ~/.cshrc
```

To your installtion on aludra or any other system, run the following command in the terminal (_use Git Bash in Windows and make sure you open a new terminal window in Mac_):
```shell
git --version
```
which should give you the current version of git installed on your system.

### Configure Git
In this stage you tell git what your name and email are and your editor of choice. In Linux or MacOS, you should run the following commands in the terminal. In Windows, you need use the Git Bash application.
```shell
#Set your name and email
git config --global user.name "Tommy Trojan"
git config --global user.email "ttrojan@usc.edu"

#Pick your editor of choice to edit commit messages (not code)
# Note that you should pick an editor that is installed on your machine
git config --global core.editor emacs

#Lets get pretty colored output!
git config --global color.ui auto
```

Due to different operating systems treating the end of line `('\n')` character differently, you can make git normalize the line feed for you based on your OS:
+ Linux & MacOS

```shell
#LF Normalization (Linux & MacOS)
git config --global core.autocrlf input
```
+ Windows

```shell
#LF Normalization (Windows)
git config --global core.autocrlf true
```

### SSH Key-based Authentication
By default, git communicates with servers using the git protocol that works over [SSH](http://en.wikipedia.org/wiki/Secure_Shell). Therefore, it is advised to generate [SSH keys](http://en.wikipedia.org/wiki/Secure_Shell#Key_management) for authentication purposes.

This guide will walk you through generating an SSH keypair. You need to follow Steps *1* and *3* only. Step 2 is only needed if you have keys already generated. This page auto-detects your operating system, so make sure your are following the correct instructions. Keep in mind that step 2 is only needed if you have an existing key pair:
> https://help.github.com/articles/generating-ssh-keys

You will need the contents of the `id_rsa.pub` in the following part of the assignment.

### Demo
Show your TA/CP the output of the following commands:
```shell
#List local git configuration options
git config --list
```
and
```shell
#Show the contents of the default SSH public key
cat ~/.ssh/id_rsa.pub
```


## GitHub Account
As discussed in the presentation, `git` is a distributed version control system. We will be using git extensively this semester in labs and in programming assignments. GitHub is a development ecosystem based around git. In CS 102, we will be using GitHub to host our git repositories and we will take advantage of other GitHub features such as the [issue tracker]( https://github.com/features/projects/issues) and [wiki]( https://github.com/features/projects/wikis).

### Creating Your Account
If you already have a GitHub account and you wish to use it for this course, you can skip to following section.

We start by visiting GitHub's sign-up page. You are free to choose your username and email. It does not necessarily need to match your USCNet account. Your email, however, needs the email you used in your git configuration.
> https://github.com/signup/free

You will be sent an email to verify your email address. Do that before proceeding.

### Update Your Profile
You need to update your profile to include your name and SSH public key. There are also some optional settings you can change such as your avatar (profile picture) and [email](https://github.com/blog/1214-notification-email-improvements) [notifications](https://github.com/blog/1204-notifications-stars).

In your [Profile Settings](https://github.com/settings/profile):
  + Put your real name in the name field. This is to ensure the TAs & CPs know who you are regardless of your username.
  + [Optional] Change your [avatar](http://gravatar.com/)

In your [SSH Key Settings](https://github.com/settings/ssh):
  + Click on **Add SSH Key**
  + Provide a **name** for the key, such as "CS102 VM Key"
  + Copy the contents of your `id_rsa.pub` file and paste them into the **key** field
  + Click **Add Key**

[Optional] You can add more emails to your GitHub account using the [Email Settings](https://github.com/settings/emails) page.

[Optional] Set your notification preferences on the [Notification Settings](https://github.com/settings/notifications) page.

### Demo
  1. Show your TA/CP your [GitHub Contributions](https://github.com/blog/1360-introducing-contributions) page at https://github.com/username where `username` is your GitHub username.
  1. Show your TA/CP your [SSH Key](https://github.com/settings/ssh) settings page.

## HelloWorld Repository
The most basic use of git is to checkout a code repository to your local machine. That is called **cloning** a repository. To clone this repository, you run the following command:
```shell
cd
git clone git@github.com:usc-csci102-spring2013/HelloWorld.git
cd HelloWorld
```
This will create a copy of the [HelloWorld](https://github.com/usc-csci102-spring2013/HelloWorld) repository on your machine in a directory named `HelloWorld`. Unlike other version control systems such as subversion, you now have a complete copy of the whole repository including its history.

### Basic Operations
To make sure your repository is up to date with the version on the server, you `pull` the most recent changes to your local copy:
```shell
git pull
```

If you want to check the commit history of this repository, you just type:
```shell
git log
```
This lists the commit history in reverse chronological order. You navigate this screen using the `SPACE`, `ENTER` or arrow keys. To quit press `q`.

You can check the history of a specific file using `git log`:
```shell
git log HelloWorld.cpp
```
You can do the same on GitHub by clicking the [HelloWorld.cpp](https://github.com/usc-csci102-spring2013/HelloWorld/blob/master/HelloWorld.cpp) file and pressing the History button


## FightOn Repsitory
Now, lets create our own repositry and using git to keep track of our code.
Create a _public_ repository called `FightOn` using GitHub:
>https://github.com/new

  - Add a optional description
  - This should be a *public* respository
  - [x] Initialize this repository with a README
  - Do not add a `.gitignore` file.

Make sure you are not inside the HelloWorld repository on your local machine:
```shell
cd
pwd
```
Then, clone the repository to your own machine using the *SSH-based* URL, i.e. the one starting with `git@github.com/...`.

Create a C++ file called `FightOn.cpp` using your editor of choice, e.g. emacs, vi or gedit.
  - Write a HelloWorld-style program the prints `Fight On!`.
  - Compile your code using the `g++` compiler: `g++ FightOn.cpp`
  - Run it to make sure it works

Now, that you have a fully functioning program, you should add it to your repository and push it to GitHub. To find out the current state of your repository, you check its `status`:
```shell
git status
```
This will show that you have two *untracked* files: `FightOn.cpp` and `a.out`. Since it is bad practice to push binary files to your repository, we are only going to add the FightOn program:
```shell
git add FightOn.cpp
```
Now, check the status and try to read through the whole message and see if it makes sense:
```shell
git status
```
At this stage, your `FightOn.cpp` file is added and ready to be committed. When you `commit` a file or a collection of files you are recording the changes to the repository:
```shell
git commit -m "Created the FightOn HelloWorld-like application"
```
The text after the `-m` is actually a mandatory message that git adds as part of the commit. If you don't supply a message via the commandline, an editor will automatically open prompting you enter a message.

If you refresh your FightOn repository webpage on GitHub, you will notice that it does not yet have your `FightOn.cpp`. The reason being that although you committed the file locally, you have yet to push the changes to the server. You do that by:
```shell
git push
```

Finally, lets do a `git status` again. You will notice that `a.out` is still listed as an untracked file. To ignore unwanted files such as log files or executables, we create a special file called `.gitignore` (note the leading dot) and we list all the unwanted files (one per line).

So, create a `.gitignore` file and list the `a.out` file in it then do a `git status`! Don't forget to push your `.gitignore` to your repository. 

## Demo
1. Show your TA/CP your FightOn repository on GitHub which should include:
    + `FightOn.cpp`
    + `.gitignore`
1. Go to the [GitHub Account Registration](https://docs.google.com/a/usc.edu/spreadsheet/viewform?formkey=dFNpLTJnVHJ4LUxicm5RSi1TczNSQmc6MQ) form:
    + Fill the form
    + Show your TA/CP the confirmation page.



## Git Reources
For more information about git, visit our [Git Resources](https://github.com/usc-csci102-spring2013/HelloWorld/blob/master/Git-Resources.md) document.
