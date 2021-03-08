# Git-commands
Git is an open source distributed version control system. 
It handles perfectly everything ranging from small to large projects with speed
and efficiecy. 

## Why use Git?
1. It helps developers to easiy manage versions of their codes.
2. Easy collaboration on a project
3. Keeps the history of who made which change to what
4. Helps users make merges of branched repos.
5. It fast and modern too


## Getting Started with Git
### Installing git on Linux
Those using RPM-based distribution such as RHEL or CentOS can use ``dnf`` 
```
sudo dnf install git-all
```
If you're using Debian-based distribution such as Ubuntu or Kali, use ``apt``
```
sudo apt install git-all
```
### Installing git on Mac
There are many ways to install Git on Mac. Your best bet is to install the Xcode Command Line Tools. Try the command below if you are using Mavericks (10.9) or above.
```
git --version
```
If you don't already have Git installed it will prompt you to install it. You can install a more update version of Git but using the installer at the Git website, at [https://git-scm.com/download/mac](https://git-scm.com/download/mac).

### Installing git on Windows
The official Git built for windows is available for download on the Git website [https://git-scm.com/download/win](https://git-scm.com/download/win).
You can get more information from [https://gitforwindows.org](https://gitforwindows.org).
For an automated installation use the [Git Chocolatey package](https://chocolatey.org/packages/git) which is a community maintained.

## Your Identity
We first need to set our identity the first time we install Git, because git uses this information for every Git commit.
```
git config --global user.name "John Doe"
git config --global user.email johndoe@example.com
```
The ``--global`` option means Git will always use that information for everything you do on that system. You can remove ``--global`` option you want to override this with different email and name on a specific project.

You can view all your Git settings and their location with the command below:
```
git config --list --show-origin
```

## Getting Help
There are three ways to get help for any command when using Git.
```
git help <verb>
git <verb> --help
man git-<verb>
```
For instance, if you want help for the ``git config`` you can use the command below:
```
git help config
```
You can get a concise help output with the ``-h`` option, as in:
```
git commit -h
usage: git commit [<options>] [--] <pathspec>...

    -q, --quiet           suppress summary after successful commit
    -v, --verbose         show diff in commit message template

Commit message options
    -F, --file <file>     read message from file
    --author <author>     override author for commit
    --date <date>         override date for commit
    -m, --message <message>
                          commit message
    -c, --reedit-message <commit>
                          reuse and edit message from specified commit
    -C, --reuse-message <commit>
                          reuse message from specified commit
    --fixup <commit>      use autosquash formatted message to fixup specified commit
    --squash <commit>     use autosquash formatted message to squash specified commit
    --reset-author        the commit is authored by me now (used with -C/-c/--amend)
    -s, --signoff         add a Signed-off-by trailer
    -t, --template <file>
                          use specified template file
    -e, --edit            force edit of commit
    --cleanup <mode>      how to strip spaces and #comments from message
    --status              include status in commit message template
    -S, --gpg-sign[=<key-id>]
                          GPG sign commit
 ```
 ## Git Repository
 You can obtain Git repository in either these two ways:
 1. You can convert a local directory into a Git repository
 2. You can clone an existing Git repository

### Initialize a Repository
```
git init
```
### Cloning an Existing Repository
```
git clone https:github.com/sofori006/git-commands
```
### Checking the Status of Your Files
```
git status
```
### Tracking New Files
```
git add README
```
### Viewing Your Staged and Unstaged Changes
```
git status
git diff
```
### Skipping the Staging Area
```
git commit -a -m 'Add new benchmarks'
```

### Removing Files
```
git rm PROJECTS.md
```
### Viewing the Commit History
```
git log
git log --stat
```
### Undoing Things
```
git commit -m 'Initial commit'
git add forgotten_file
git commit --amend
```
### Showing Your Remotes
```
git clone https:github.com/sofori006/git-commands
cd git-commands
git remote
git remote -v
```
### Adding Remote Repositories
``` 
git remote add pb https:github.com/sofori006/git-commands
```
### Pushing to Your Remotes
```
git push origin master
```
### Inspecting a Remote
```
git remote show origin
```
### Renaming and Removing Remotes
```
git remote rename pb paul
```
### Creating a New Branch
```
git branch testing
```
### Switching Branches
```
git checkout testing
```
### Basic Branching and Merging
```
git checkout master
git merge testing
```
