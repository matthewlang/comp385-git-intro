# COMP385: Git Intro

This initial project will walk you through checking out a project, making a
branch, and creating a pull request on GitHub.

## Getting started

First, you should set up your local environment with your GitHub credentials
following [these
instructions](https://docs.github.com/en/free-pro-team@latest/github/using-git/caching-your-github-credentials-in-git).

Then, clone this repository. You can find the URL for your repository on the
GitHub repository page when you click the "Code" button.

```
$ git clone <repository url>
```

The first time you do this, it will ask you for your username and password for
GitHub.

## Working in a branch

You will do your development in _branches_. This allows you to have work in
progress that is not checked in to the main repository. You should read about
the development flow using Git
[here](https://guides.github.com/introduction/flow/).

```
$ git status  # notice you are in the "main" branch
$ git checkout -b <branch name>  # create and check out a branch
$ git status  # notice you are now in a new branch
$ git branch list  # you should now see two branches
```

You can switch between branches by checking them out:

```
$ git branch list
$ git checkout <other branch>
```

## Making changes

In your branch, you can edit, add, and delete files. When you have completed a
chunk of work, you should commit your work.

First, add the files that you want to commit:

```
$ git add <file>
```

Then, create the _commit_, including a short message describing the changes that
were made. These messages should be meaningful.

```
$ git commit -m "<message>"
```

There's a shortcut if you want to add all of the modified files in your project
to a commit. Use the `-a` flag to specify all changed files:

```
$ git commit -am "<message>"
```

Finally, you can _push_ your changes to GitHub.

```
$ git push -u origin <branch>
```

## Working on different machines

You can use your GitHub project to work on different machines, if required.
Make sure that all of your changes have been pushed and simply clone the
repository to the new machine. 

When you've pushed your changes from one clone, you will need to do a `git pull`
to pull the changes you made to the other clone.

## Creating a pull request

Now, when you are finished working, you can create a pull request (PR).

You can do this via the URL that is displayed to you have running `git push` or
by navigating to the branch on GitHub and selecting to create a pull request.

PRs on GitHub are the mechanism through which developers on a project review and
approve others' code changes. In this class, it will be how I review and grade
your code.

## This assignment

Create a PR against your repository for this assignment that changes my name to
yours in `hello.go`. __Do not merge your PR.__
