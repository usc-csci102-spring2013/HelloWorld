HelloWorld
==========
Welcome to CS 102 on GitHub! Here, you will find code repositories for all lectures, labs and programming assignments. 

This is our obligatory Hello World _public_ repository. If you only see this repository under the [CS 102 GitHub Organization Account](https://github.com/usc-csci102-spring2013) This means that you are yet to be designated as a member of this organization. This process starts by you. All you need to do is provide your GitHub account username to your TA/CP and you will be added within the first week of classes.

In this course, we will using the following VirtualBox Appliance as the reference system for grading:
> http://ee-classes.usc.edu/cs101/cs102-vm.ova

This is an Ubuntu 12.04 LTS VM. You can login using:
  + Username: `cs102`
  + Password: `memory`

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

1.In your [Profile Settings](https://github.com/settings/profile):
  + Put your real name in the name field. This is to ensure the TAs & CPs know who you are regardless of your username.
  + [Optional] Change your [avatar](http://gravatar.com/)

1.In your [SSH Key Settings](https://github.com/settings/ssh):
  + Click on **Add SSH Key**
  + Provide a **name** for the key, such as "CS102 VM Key"
  + Copy the contents of your `id_rsa.pub` file and paste them into the **key** field
  + Click **Add Key**

1.[Optional] You can add more emails to your GitHub account using the [Email Settings](https://github.com/settings/emails) page.

1.[Optional] Set your notification preferences on the [Notification Setttings](https://github.com/settings/notifications) page.

### Demo
  1. Show your TA/CP your [GitHub Contributions](https://github.com/blog/1360-introducing-contributions) page at https://github.com/username where `username` is your GitHub username.
  1. Show your TA/CP your [SSH Key](https://github.com/settings/ssh) settings page.

## HelloWorld Repsitory
- clone this repo
- check log

## FightOn Repsitory
- create your own repo
- update .gitignore
- push FightOn.cpp

## Git Reources
For more information about git, visit our [Git Resources](https://github.com/usc-csci102-spring2013/HelloWorld/blob/master/Git-Resources.md) document.