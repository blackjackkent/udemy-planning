# Version Control with Git - In Plain Language

## Introduction

Hi! I'm Rosalind Wills, and welcome to my course -- Version Control with Git in Plain Language. I've been working as a software developer for over ten years, specializing in Javascript, C#, and Java; I have a master's degree in software engineering and a bachelor's in English. Not only do I love programming, but I love talking about it, helping other people to understand how to get started and give life to their ideas in apps and programs.

Learning programming can sometimes seem like a daunting task. There's so many languages to choose from, so many ways to architect and structure your code, and so many tutorials out there, all assuming different levels of knowledge. In this course series, I will describe major programming concepts from the ground up, giving you a framework to build on as you dive deeper into the world of software development.

The subject for this course is version control. Version control is an important concept in software development, although you've probably encountered it in other contexts as well. Have you ever used the "View History" feature in Google Drive? Clicking through the list on the side of the screen, you can see the exact state your document was in at various points in the past, and restore that state with a click. Or perhaps you've taken a backup of a file or folder on your hard drive before you make changes to the files in it, so you can restore the old version if you need to.

This, in essence, is exactly what version control is all about. Version control software like Git, Mercurial, Subversion, and others are all focused on one thing -- maintaining past copies of your code or other files, so they can be restored if you make a mistake or want to change back to something you did in the past.

The version control system we'll be talking about today (and the most popular one among most developers) is called Git. Git has been around in software development for a long time. It was originally designed by Linux Torvalds while he was developing the Linux operating system, back in 2005. Since then it has exploded in popularity because of its power, flexibility, reliability, and ease of use particularly among teams with more than one person working on the same set of code.

All that said -- Git can be a little hard to get your head around when you first start trying to use it. So let's go over some concepts first.

## Concepts

What is Git and how does it work? It's a big question, but there are some basic concepts that will be very helpful to understand before you start trying to use the system.

### Repository Snapshots

The central concept behind Git is the repository. The word "repository" just means a container, something that holds other things, and in Git it is the overarching container for all your files. When you first start a new software project, you will have a folder on your hard drive where all your code files will go. You tell Git to initialize that base folder as your repository in order to begin using version control.

From that point forward, Git will (whenever you tell it to) be able to take a snapshot of the exact state of all files anywhere inside that folder (at any level). And once you've taken a snapshot -- called a commit, in Git -- you can instantly, at any point, set your folder to that exact state again, just by telling git to activate that commit.

This, in a nutshell, is the central value that git provides. There's lots of other great things Git can do, but they all grow out of this one central tenet -- that the current state of your file system can be snapshotted, stored, and restored when needed.

### Distributed Behavior

Git, unlike many popular version control systems, is known as a "distributed version control system". This means that it can operate entirely independently of any remote server. When you have a Git repository on your local computer, you have the entire history of your current files on your computer as well, rather than having the history stored remotely and only a particular version on your local machine. 

This is a major differentiator between Git and VC systems like Subversion, and it allows you to navigate very quickly between versions of your code if you need to.

(Technically, it's a little more complicated than this; it would be more accurate to say that you have the entire history of your current *branch* stored locally, which might not be the entire history of your codebase, but we will go into that in more detail later on when we talk about branching and working with a team. For now, the concept is still the same -- Git stores all the information about your current copy of the code and its history locally, so you don't have to maintain a version control server and your file manipulation can be very fast.)

### Git Makes It Hard To Mess Up

Almost everything that you do with Git is focused on adding more information to the system. Whether you're tracking a new file in a snapshot
