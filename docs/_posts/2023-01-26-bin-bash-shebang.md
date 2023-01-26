---
layout: post
title:  "Bin Bash and the Whole Shebang"
categories: learning
author: lakruzz
links:
  repo: kea-dev/bin-bash-shebang
  slides: 
---

The _shell_ is where you can peak into the kernel of the Operating System. It's a terminal but it's also an entire programming language; shell scripting. Did you know, that on Linux all it takes to make to make a file executable is a _Shebang:_ _`#!`_. A whole new world opens up when you know Linux and the shell. Let's automate stuff!
{: .kicker}

I assume you are reading this post, because you are attending a class with [me](https://www.linkedin.com/in/lakruzz/){: target="_blank"} on KEA. If that is indeed the case, then I will allow myself to assume that you have accounts on both [GitHub 🔐](https://github.com/signup?source=login){: target="_blank"} and [Google 🔐](https://account.google.com/){: target="_blank"}. If you don't have these accounts already; please go and sign up before class (free tier accounts are fine on both platforms).

# The Tech Stack
We will be exploring the following technologies:

- Linux
- Bash (a.k.a _shell_, _terminal_, _command-line_, _script_)
- Docker
- GitHub CodeSpaces and by extension VS Code

# Learning goals
- Understand the purpose and design of an Operating System.
- Get access to Linux - where ever you are.
- Master the most basic shell commands.
- Master basic language structures in shell scripting.
- Understand Command Line Interfaces (CLI) including a basic understanding of both POSIX and package managers.
- Automate stuff you do often - using shell scripts, extensions, aliases.

# Flipped Classroom
Listed below are the resources you are expected to absorb (suck it up!) _before_ we meet in class.

You are encouraged to practice _active reading_ (or _- listening_, _- watching_, _- installing_). While you absorb; Scribble notes, questions, challenges, perspectives, links, references, drawings, feed-back as you go through the resources. Also consider sharing some of these scribbles and questions with peers and instructors _before_ we meet in class. Use this learning module's dedicated [💬 discussions](https://github.com/{{ page.links.repo }}/discussions/categories/q-a){: target="_blank"} on GitHub. 

If you are curious to get a glimpse into some of the activities we will be doing during class you can browse the `README.md` of the [{{ page.links.repo }}](https://github.com/{{ page.links.repo }}){: target="_blank"} repository on GitHub or the [_issues_](https://github.com/{{ page.links.repo }}/issues?q=is%3Aopen+is%3Aissue+label%3Atemplate){: target="_blank"} of the same repository.

## What is an Operating System?
📚 [What is an operating system?](https://edu.gcfglobal.org/en/computerbasics/understanding-operating-systems/1/){: target="_blank"}<br/>
⏳ [10:00]

Read the article - and watch the video (which is also embedded in the same post)

<iframe width="560" height="315" src="https://www.youtube.com/embed/fkGCLIQx1MI" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## Install VS Code
💾 [Download and install](https://code.visualstudio.com/download){: target="_blank"}<br/>
⏳ [10:00]

VS Code is an Open Source <span title="Integrated Development Environment" style="cursor:pointer;color:grey;">IDE</span> developed by Microsoft. and we will used it going forward. Skip this if you already have it installed. But if you do need to install it then be aware that you download the installer that is right for your OS and CPU.

## Install Docker Desktop
💾 [Download and install](https://www.docker.com/products/docker-desktop/){: target="_blank"}<br/>
⏳ [10:00]

Docker is a container technology. It enables you do _build_ or _pull_ _images_ and then run them in _containers_. It's a technology that relies on features in the _Linux kernel_ so it only runs on Linux. But by installing _Docker Desktop_ you can make the same technology available even on Windows and Mac PCs through the means of a Virtual Machine - running Linux. It's not as complicated as it sounds (well actually it is - but it works well, so you don't see the complexity).

If you already have it installed then your fine. But if you do need to install it then be aware that you download the installer that is right for your OS and even CPU

## How To Run Linux Code on Windows with WSL 2 & VS Code
📺 [YouTube Video](https://www.youtube.com/watch?v=bRW5r7TK6KM){: target="_blank"}<br/>
⏳ 14:00]

Please watch this video - _even if you are not on a Windows PC - it's still relevant_. 

### MacOS is not Linux
If you own a Mac - and you are familiar with the _terminal_ them you might think that it's running Linux underneath. But MacOS is not Linux (the same way _"GNU is not Unix"_ - geeky pun - I'll explain it in class). 

Mac does looks a lot like Linux though. Apple's _distro_ is called _Darwin_ and it's not even a real distro - but it's the equivalent of one: It's built in the same was as-if it was a distro; Bits and parts of core features and nice utilities on the side and on top. But the kernel is Darwin, which is based on a _FreeBSD_ kernel - and although it too is Open Source and it too is emulating UNIX - it's not Linux.

### Windows is not Linux
While MacOS looks enough like Linux not to cause any serious problems it's different with Windows. Windows is not Linux in the same way a fish is not a bicycle - they do not resemble each other - at all! This turned out to be a genuine problem for Windows in the longer run. The success of Linux - a superior OS available for free - meant that Microsoft would have to fall in line - like Apple did when they launched MacOS X - their Darwin based OS.

The world want Linux! Especially now, since the container revolution caused by Docker. Windows solved it in a different way - they worked together with Canonical, the company  behind the Linux distro called _Ubuntu_. And they manage to scoop in a _Windows Subsystem for Linux:_ WSL. It's available on Windows 10+ and contrary to Darwin it's running on a _genuine Linux kernel_. It defaults to Ubuntu - but you can pick another distro if you want. 

Now watch the video.

<iframe width="560" height="315" src="https://www.youtube.com/embed/bRW5r7TK6KM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## Wikipedia on "Linux"
📚 [Wikipedia](https://en.wikipedia.org/wiki/Linux){: target="_blank"}<br/>
⏳[25:00]<br/>

Time to take a deep dive into some Linux background. I'll send you towards the Wikipedia article on Linux - It may hit you as heavy stuff - it's roughly a 25 min read but it probably introduces so many new terms that you may well have smoke coming out of you ears before you reach then end. But please try to read it through. And make notes while you read!

## Find you own information
🔍 Search the internet for terms like ["what is an operating system"](https://www.google.com/search?q=what+is+an+operating+system){: target="_blank"} or ["Linux kernel explained"](https://www.google.com/search?q=linux+kernel+explained){: target="_blank"}<br/>
⏱️ [20:00]<br/>

Time box this to 20 mins; What can you find of good materials for someone at your own level fighting to understand Operating systems in general, Linux distributions and the Linux kernel in particular. Make notes. Be prepared to share your good findings.

# Additional resources

## Linux Foundation - 101 tutorial
👩‍🎓 [The LFS 101 _Introduction to Linux_ course](https://learning.edx.org/course/course-v1:LinuxFoundationX+LFS101x+2T2021/home)<br/>
⏳ [4:00:00]

This is the official Linux Foundation self-training material for a Linux Practitioner Certification. It requires that you register (it's free though).

## Linux Crash Course  
📺 [YouTube video](https://www.youtube.com/watch?v=ROjZy1WbCIA){: target="_blank"}<br/>
⏳  [2:45]
<iframe width="560" height="315" src="https://www.youtube.com/embed/ROjZy1WbCIA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

Honestly - I gotta admit, that I didn't actually watch this particular video myself (yet). But I just wanted to make the point, that there are _many_ of this type of videos out there - and you would be surprised how much you can pick up in ≈3 hours!

## Shell commands
📒 [A ledger of all commands](https://www.geeksforgeeks.org/linux-commands/?ref=lbp){: target="_blank"}<br/>
⏳ 👀

...Well, maybe not _all_ but definitely _many_.

📒 [Basic shell commands](https://www.geeksforgeeks.org/basic-shell-commands-in-linux/){: target="_blank"}<br/>
📒 [Basic scripting](https://www.geeksforgeeks.org/basic-operators-in-shell-scripting/){: target="_blank"}<br/>
⏳ 👀
