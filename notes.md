# Introduction
## Github
### Repositories
You can create a repository on GitHub or by using the `git init` command on Git Bash. You can then clone it to your local environment using the `git clone` command and copying the url to your repository.
###Making Changes
There are three main commands in the console that you will use when working on your project.
* `git pull` will pull the repository's changes from GitHub
* `git commit` will commit any changes made to the code
* `git push` will push changes to GitHub
The first time you push changes to GitHub, it will ask you how you want to identify yourself.
A few other useful commands include:
* `git fetch` will get the latest information on GitHub without changing the local repository.
* `git status` will check the differences between the clones and will let you know if you are missing a commit.
###Handling merge conflicts
Typically, you can avoid merge conflicts by pulling the code and pushing it often. Merge conflicts occur if at least one line in the code differs between commits. You simulated a merge conflict in conflictTest.md. 
In testing the merge conflict, you can run the `git fetch` and the `git status` commands to check the differences.
```sh
➜  git fetch
➜  git status
Your branch and 'origin/main' have diverged,
and have 1 and 1 different commits each, respectively.
  (use "git pull" to merge the remote branch into yours)
```
This will show that cloned repositories have diverged from each other. This is fine unless the exact same line was changed between commits. When you run the `pull` command, you will see this:
```sh
➜ git pull
Auto-merging conflictTest.md
CONFLICT (content): Merge conflict in conflictTest.md
Automatic merge failed; fix conflicts and then commit the result.
```
When you open up VSCode, you will see something like this
```
I will use this file to test merging conflicts.

<<<<<<< HEAD
Example: Conflict change made in development environment
=======
Conflict change made in GitHub
>>>>>>> b9f4c53c91eff509993d7291e60148f903827de0
```
To fix the merge conflict, you will use the file editor to keep the changes that you want to make from each commit and then push the result.
```
I will use this file to test merging conflicts.

Example: Conflict change made in development environment and in in GitHub
```
Use the `commit` command and the `push` command to push the changes.
```sh
➜  git commit -am "merge(notes) combined both edits"
➜  git push
Enumerating objects: 10, done.
Counting objects: 100% (10/10), done.
Delta compression using up to 12 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 701 bytes | 701.00 KiB/s, done.
Total 6 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/camilv12/startup.git
   a5acfe0..9bd6fdd  main -> main
```
