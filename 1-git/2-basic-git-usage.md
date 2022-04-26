# Basic Git Usage

## Installing Git
---

You can download git for windows from the [git website](https://git-scm.com/).

On Linux you can simply type
```
sudo apt-get install git
```
in the terminal.

Once you have git installed, open a terminal and type
```
git version
```
to see if git is working. If you see something like
```
git version 2.20.1
```
then git is installed and working.

## Creating, Cloning or Forking a Repository
---

To create a new repository for a project that's not using git, go to the directory containing the project and type
```
git init
```
to initialize a new repository. You can then add all the files in the repository to git by typing
```
git add .
```
to tell git to track all the files. The `.` simply means all files in the directory. You can also exclude files or add them individually but that is beyond our scope at the moment.

If you want to add the new repository to a service like [GitLab](https://gitlab.com/) or [GitHub](https://github.com/) you could now create a new project on your preferred Git*Something* and then type
```
git remote add origin replace-with-url-of-remote-repository
```
to tell the local repository to now reflect the one on the server. However, I would recommend first creating the new project in you favorite git service and then using the clone instruction from below to initialize it on you computer.

To clone the repository of a project that's already using git, go to the directory you want to clone the project to and type
```
git clone replace-with-the-url-of-the-project
```
to clone the project present at the URL provided.

To fork a git repository, go to the directory you want to fork the project to and type
```
git fork replace-with-the-url-of-the-project
```
this creates a separate copy of the project for you to work on.

Use **init** when starting a new project, **clone** when working on a project as a team or from a new computer and **fork** if you want to copy a project and work on it separately.

## Git Workflow
---
Once you have a repository your day-to-day workflow will likely consist of: checking for changes, making changes and then committing those changes.

### **Check for Changes**

If you are working on a project with others you can type
```
git fetch
```
to check for changes. You can then use
```
git status
```
to see if any changes were found. If there are changes you can get them by typing
```
git pull
```
to update your files. That's it, now you can work on the latest version of the project.

### **To branch or not to branch**

Before you start working you will need to decide on what branch of the project you want to work on. Generally speaking you should never work on the master branch. If you want to implement a new feature, fix a bug or try something out then type
```
git branch name-of-new-branch
```
to create a new branch. You can now switch to the branch you created, or to an already existing one if you didn't need to create a new branch by typing
```
git checkout name-of-branch
```
to start working on the branch. Remember that if you don't checkout the branch you created you will stay on the master branch. You can type
```
git status
```
at any point to see what branch you are on.

### **Make Changes**

Once you are on the right branch and have made the changes you wanted you can add them by typing
```
git add .
```
to add all changed files. You can then type
```
git commit -m "A message to tell others and yourself what you did"
```
to commit your changes, making them official. The part in parenthesis is called the commit message and is an important part of git. This helps you and other see at a high level what you changed in your commit. You can read how to write a good commit message on [this website](https://chris.beams.io/posts/git-commit/).

Now if you are working by yourself and on a local repository you can leave it at that. However, mostly you will be pushing your changes to a server for your team, or yourself from another computer, to use. You can type
```
git push origin name-of-branch-you-worked-on
```
to push your changes to the correct branch on the server. You can use the `-u` option to remember the branch so that you don't always have to type it. For example if you are working on a new release you might be on the branch `next_version` and type
```
git push -u origin next_version
```
to tell git to push to the `next_version` branch by default. Now you can simply type
```
git push
```
the next time you have changes to upload.

### **Merge**

At one point you will be done working on your branch and will want to merge it with the master branch or with another branch. You can do this by checking out the branch you want to merge your branch with and then typing
```
git merge your_branch_name
```
to merge your branch with the one you are currently on. So if you want to merge say `next_version` with `master` you will first type
```
git checkout master
```
to switch to the master branch and then type
```
git merge next_version
```
to merge `next_version` with the `master` branch.

Now there is no more `next_version` branch and all your changes have been incorporated into the master branch.

## That's All Folks
---
That's the very bare basics to get you working on a git project. I left out a lot of information but we are just scratching the surface and there's a lot to come still. For now you can use *Basic Git in a Nutshell* as a cheat sheet while doing the *Basic Git Practice* assignments.