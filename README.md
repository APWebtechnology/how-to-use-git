# How to use git
## Install git
First of all make sure that git is installed on your machine via following command.
```bash
$ git --version
git version 2.26.1.windows.1
```
If you don't have git, please [download](https://git-scm.com/download/win) and install it.
## Clone a repository
Find the repository url you want to clone, most of the times it will end with '.git'.\
Then in the directory where you want to download the repository, execute the following command.
```bash
$ git clone https://github.com/APWebtechnology/basic-template.git
Cloning into 'basic-template'...
remote: Enumerating objects: 6, done.
remote: Counting objects: 100% (6/6), done.
remote: Compressing objects: 100% (5/5), done.
remote: Total 6 (delta 0), reused 3 (delta 0), pack-reused 0
Receiving objects: 100% (6/6), done.
```
Now you will notice that a directory has been created with the same name as the repository.
## Check the files
Use the following command to start your 'File Explorer' and check out all the files.
```bash
$ start .
```
## Check the different commits
You can check all the different commits via the command prompt with the following command.\
But you can check it as well online via the repository.
```bash
$ git log
commit 2789bd10f84010ccea1951d763625e5c07bc57fd (HEAD -> master, origin/master, origin/HEAD)
Author: Nicolas Goris <nicolas.goris@flexso.com>
Date:   Sat Apr 18 16:26:36 2020 +0200

    Basic template

commit e3faae918a17a3881cc4322434f74f2b77b3aa60
Author: Nicolas <nicolasgoris@users.noreply.github.com>
Date:   Sat Apr 18 16:22:46 2020 +0200

    Initial commit
```
## Checking out a specific commit
You can check out all the files and their content via going to a specific commit, use the following command and use a correct commit id.
```bash
$ git checkout e3faae918a17a3881cc4322434f74f2b77b3aa60
Note: switching to 'e3faae918a17a3881cc4322434f74f2b77b3aa60'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at e3faae9 Initial commit
```
We can ignore the 'blabla' and just restart our 'File Explorer' and now we will see that the 'index.html' file is gone.\
That is because we are now looking at the state of the repository just after the first commit. At that time the 'index.html' file did not yet exist.
## Going back to current commit
Using the following command we will return to the current/latest commit in the repository.
```bash
$ git checkout master
Previous HEAD position was e3faae9 Initial commit
Switched to branch 'master'
Your branch is up to date with 'origin/master'.
```