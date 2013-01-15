HelloWorld
==========
Welcome to CS 102 on GitHub! Here, you will find code repositories for all lectures, labs and programming assignments. 

This is our obligatory Hello World _public_ repository. If you only see this repository under the [CS 102 GitHub Organization Account](https://github.com/usc-csci102-spring2013) This means that you are yet to be designated as a member of this organization. This process starts by you. All you need to do is provide your GitHub account username to your TA/CP and you will be added within the first week of classes.

# Lab 01 – Excersises

## Git Setup
You need to setup git on every machine you plan to use for CS 102 this semester. This includes your own desktop/laptop(s) and the [course VM](http://ee-classes.usc.edu/cs101/cs102-vm.ova). The VM has git already installed. You do, however, still need to configure it.

### Download & Install Git
Start by downloading the latest [git](http://git-scm.com/) package from the official git website:
> http://git-scm.com/downloads

Installing the downloaded package should be straight forward.

### Configure Git
In this stage you tell git what your name and email are and your editor of choice. In Linux or MacOS, you should run the following commands in the terminal. In Windows, you need use the Git Bash application.
```shell
#Set your name and email
git config --global user.name "Tommy Trojan"
git config --global user.email "ttrojan@usc.edu"

#Pick your editor of choice to edit commit messages (not code)
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

This guide will walk you through generating an SSH keypair:
> https://help.github.com/articles/generating-ssh-keys


## GitHub Account
As discussed in the presentation, `git` is a distributed version control system. We will be using git extensively this semester in labs and in programming assignments. GitHub is a development ecosystem based around git. In CS 102, we will be using GitHub to host our git repositories and we will take advantage of other GitHub features such as the [issue tracker]( https://github.com/features/projects/issues) and [wiki]( https://github.com/features/projects/wikis).
