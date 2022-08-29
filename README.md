# Git Dojo

## About Git
Git is a [`version control system`](https://en.wikipedia.org/wiki/Version_control), initially created by [Linus Torvalds](https://en.wikipedia.org/wiki/Linus_Torvalds) in 2005 to facilitate development of the Linux kernel. Since then, it's become nearly omnipresent.

## Initialize a new repo
* `git init`
  * if you have `>= 2.28` (`git --version` to check) you can change the default branch name
    * pass `-b main`/`--initial-branch=main` to initialize the new repo with `main` as the default branch
    * use [`git config`](#configuring-git) `--global init.defaultBranch main`
There's nothing special about `main`, it's just what most people use. (Some people use `trunk`.)

## Remotes
Remotes are places where your code lives. Most of the time, this will be on github, but it _doesn't have to be_. Other options include [gitlab](https://about.gitlab.com/); you can even host your own git server.
* `git remote -v` will show you a list of remotes
* `git remote add <name> <url>` will add a remote
  * `name` is how you identify the remote to git, when you e.g. [`pull`](#pulling-and-pushing) or [`push`](#pulling-and-pushing)
* `git remote set-url <name> <url>` will update the url of a remote by name
* `git remote remove <name>` will remove a repo by name
Much like most people use `main` for the default branch, it's conventional to call your primary/default remote `origin`.
