---
layout: post
title: Git Merges and Branches
subtitle: Understanding git merges and branching
cover-img: /assets/img/git-banner.jpg
thumbnail-img: /assets/img/git-banner.jpg
share-img: /assets/img/path.jpg
tags: [git, merge, branches]
---

Git is an essential tool for any software engineer. Git is a distributed version-control system for tracking changes in source code during software development. One of the most confusing and arguably the most important part of git is using branches and merging. Git merging and branches is a huge help to collaborating on big software projects, so understanding branches and merges opens up a world of clean and effective collaboration for big projects. I'm going to walk you through the basics of understanding git, so the next time you have a collaboration, your project can be safe, effective, and clean.

**Git Branches**

Imagine you're working on a project with a group of people and you were assigned the task of creating a cascade sheet for the home page. How could you submit your data to the main project? Sure you could copy and paste the whole project and change the '.css' file, but what if you wanted to just change one line in the '.css' file, while your partner changed another? Discussing with your partner and trying to patch together the lines would be tedious and time consuming. Luckily, git has something called branches which handles the work for us. Instead of cloning the entire project so you can play with the file, what a branch allows us to do is create a new version of the main, or master, branch and add our own changes to it. This new branch is separate from the master branch and allows us to make our own changes without effecting the master branch. Amazing isn't it?

Creating a new branch is simple:
```ruby
git branch new_branch
```
This creates a new branch named new_branch for our repository. If you'd like to see all the branches run the command:
```ruby
git branch
#or we could do
git branch -a
```
Output:
```ruby
new_branch
*master
```
As you can see there's two branches that's been listed. The master branch is the main branch and the new_branch is the branch we've just created. We can depict which branch we're on by looking at the  asterisk character. Since the asterisk is in front of master, then we know we're on the master branch. To switch branches we can run the command:
```ruby
git checkout new_branch
```
Now if we list out all of our branches:
```ruby
git branch

*new_branch
master
```
We can see that we're on the new_branch now. Any changes we make in this branch won't alter the master branch. But what if we're done editing our branch and want to put the changes on the master branch? That's where merging comes into play. To merge we first need to migrate towards the master branch.
```ruby
git checkout master
```
Once we're in the master branch now we can run the command:
```ruby
git merge new_branch
```
And voila, if you check the explorer, you'll see that our '.css' file has been added with the changes made. Amazing!

Git offers many more amazing features and there's much more we can do with merging branches. If you'd like more information about git checkout the available resource links.
