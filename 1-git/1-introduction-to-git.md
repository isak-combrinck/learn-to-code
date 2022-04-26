# Introduction to Git
[Git Website](https://git-scm.com/)

### **What is a version control system?**

Version control systems (VCS) help you keep track of changes made to a project as you work on it. The idea is that you can see all the changes made to your project, who made them and why they were made. This is especially useful for programming projects as it allows you to keep an overview of changes made to the codebase. Another important aspect of VCS is that they allow you to roll back changes and return to a previous version of your project.

Without a VCS, staying on top of a programming project is a hard task, especially once you have multiple versions. Let's say you are working on a programming project. While implementing a new feature you discover a bug in the last release. Now without a VCS you would go back to the release version and fix the bug, assuming that you saved it somewhere. Once you have the bug fixed you would need to somehow fix it for the version implementing the new feature as well.

If you are well organized this might not seem too bad to you. But what happens once you start working with other people? What if Danny is also working on a new feature? How do you get your bugfix out to him so that his version doesn't bring the bug back?

As you can see, it's easy to end up with a lot of copies of your project  and even easier to loose track of what is different between them.

This where a VCS comes in. A VCS keeps track of all the changes to your project and allows you to jump between different versions of your project without losing changes. It essentially keeps track of all of the different versions on your project in one folder. No copy-pasting your entire project before you make a change and no need to remember what you changed.

### **What is git and why is it different?**

Git is the standard version control system for the programming industry. It was originally developed by Linus Torvalds (who also developed Linux) to make working on programming projects with a lot of developers easier. Git allows you to work on multiple versions of your project at the same time, so you can develop a new version and fix bugs in the last version simultaneously.

While git is awesome, it's also complex and learning it is a lot like learning a programming language. The reason we learn git is because it makes your life as a programmer a lot easier, even if it might add a little complexity to it.

A git project is a folder with a special `.git` folder in it. The differences between versions of your project are stored in this folder and when you switch between versions git changes the actual contents of the your folder. This means that every time you switch between versions, the content fo your project folder also changes to reflect the state of the version you switched to.

When you want to implement a new feature in a git project you make something called a `branch`. This basically makes a copy of your project that you can work on without effecting the main project. Now if you run into problems with the new branch you created, let's call it `next_version`, and want to go back to the last stable version, all you have to do is switch back to the `main` branch.

However, once you get back on the `main` branch you don't fix the bug on it. First you create another branch, let's say `bugfix_a`, and then fix the bug on that branch. Now once the bug is fixed you can simply merge `bugfix_a` with `main` and with `next_version`. Now the bug is fixed in your main project and the in the next version but you only had to fix it once. As you can see this saves you a lot of time and makes switching between different versions of your project easy.

Now let's learn some *Basic Git Usage* in the next lesson.