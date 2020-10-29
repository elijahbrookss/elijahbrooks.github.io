---
layout: post
title: Git Merges and Branches
subtitle: Understanding git merges and branching
cover-img: /assets/img/gitlogo.gif
thumbnail-img: /assets/img/git-banner.jpg
share-img: /assets/img/git-banner.jpg
tags: [git, merge, branches]
readtime: true
---

Git is an essential tool for any software engineer. Git is a distributed version-control system for tracking changes in source code during software development. One of the most confusing and arguably the most important part of git is using branches and merging. Git merging and branches is a huge help to collaborating on big software projects, so understanding branches and merges opens up a world of clean and effective collaboration for big projects. I'm going to walk you through the basics of understanding git, so the next time you have a collaboration, your project can be safe, effective, and clean.

### Git Branches

Imagine you're working on a project with a group of people and you were assigned the task of creating a cascade sheet for the home page. How could you submit your data to the main project? Sure you could copy and paste the whole project and change the '.css' file, but what if you wanted to just change one line in the '.css' file, while your partner changed another? Discussing with your partner and trying to patch together the lines would be tedious and time consuming.

Luckily, git has something called branches which handles the work for us. Instead of cloning the entire project so you make your edits with the file, what a branch allows us to do is create a new version of the main, or master, branch and add our own changes to it. This new branch is separate from the master branch and allows us to make our own changes without effecting the master branch. Amazing isn't it?

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
Now let's go ahead and make our edits to the '.css' file. We started off with just a basic background color.

![css_image](/assets/img/css(1).png)

Now let's change the background_position.

![css_image](/assets/img/css(2).png)

We're finished with our edits. Now it's time to merge our branch to the master branch.

### Merging Branches

We can see that we're on the new_branch now. Any changes we make in this branch won't alter the master branch. But what if we're done editing our branch and want to put the changes on the master branch? That's where merging comes into play. To merge we first need to migrate towards the master branch.
```ruby
git checkout master
```
Once we're in the master branch now we can run the command:
```ruby
git merge new_branch
```
And voila, if you check the explorer, you'll see that our '.css' file has been added with the changes made.

![css_image](/assets/img/css(2).png)


 There's still one more thing we need to do though. If you run the command to look at all of our branches, you'll notice that the "new_branch" is still there. Since we've merged our changes over there's no need for it. Let's remove it. To delete branches **that have been merged**, run the command:
```ruby
git branch -d new_branch
```
Now if we print out all of our branches we see that new_branch is gone now.
```ruby
*master
```
Our merge has been completed. What if, however, we were right in the middle of making a change but decided that we're not going to do that change anymore? Let's say we have a branch named "active_record_databases." But, our boss just told us that he doesn't want to use active_record anymore. Well then, we'll need to delete the branch from the repository. To delete branches from the repository that **haven't been merged yet** run the command:
```ruby
git branch -D active_record_databases
```
Now if we list out all of our databases, we see that active_record_databases isn't there anymore.
```ruby
*master
```
Git offers many more amazing features and there's much more we can do with merging branches. Here's some useful commands for branching and merging.

git branch feature -- creates a new branch
git branch -a --shows all branches
git checkout feature -- switches over to branch
git branch -d feature --deletes braanch if merged
git branch -D feature --deletes branch if not merged
git checkout -b feature -- creates a new branch and switches over to branch

| Command | Description |
| :------ |:------|
|git branch branch_name| creates a new branch|
|git branch -a| lists all the branches|
|git branch| lists all the branches|
|git checkout branch_name| navigates to a branch|
|get checkout -b branch_name| creates and navigates to a new branch|
|git branch -d branch_name| deletes the branch if merged |
|git branch -D branch_name| deletes the branch |
|git merge branch_name| merges the branch |

**More Information**

  [Basic git commands: add, commit, push](https://davidmolina2810.github.io/programming-prose/2020-10-27-git-your-work-flow-on-with-git/)
  [Understanding Branches](https://blog.thoughtram.io/git/rebase-book/2015/02/10/understanding-branches-in-git.html)
  [Merging and Merge Conflicts](https://www.youtube.com/watch?v=__cR7uPBOIk)
