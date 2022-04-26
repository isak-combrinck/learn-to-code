# Basic Git in a Nutshell

## Daily Workflow

### **Check for and get changes**

Check for changes using
```
git fetch
```
then display them using
```
git status
```
and get them, if there are any, using
```
git pull
```

### **Know what branch you're on**

See if you are on the branch you want to be on using
```
git status
```
if not switch to another branch using
```
git checkout another_branch
```
or create a new one using
```
git branch a-new-branch-name
```
and then remember to switch to it before making changes. Once you are on the right branch, go crazy.

### **Add your changes to git**

When you are done add your changes using
```
git add .
```
then commit them, remembering to write a meaningful commit message, using
```
git commit -m "A meaningful message"
```
to make the changes final. Now you can upload your changes to a server, if you're using one, by using
```
git push origin branch_name
```
to send the changes to the server.

## Setting up a Project

Use
```
git init
```
to create a new local repository.

Use
```
git clone replace-with-the-url-of-the-project
```
to copy an existing repository to your computer to work on.

Use
```
git fork replace-with-the-url-of-the-project
```
to create a copy of an existing repository.

Use **init** when starting a new project, **clone** when working on a project as a team or from a new computer and **fork** if you want to copy a project and work on it separately.