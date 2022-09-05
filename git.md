# Introduction

## Link

<a href="#git commands">All Git Commands</a>

### How Git Works?

- 3 Main States of Artifact (AKA file):

|  States  |                                    Description                                    |
| :------: | :-------------------------------------------------------------------------------: |
| Modified |                The artifact goes through change made by the user.                 |
|  Staged  | The user/developer adds the artifact to Git index or staging area. <br> `git add` |
|  Commit  |     The artifact gets safely stored in local Git database. <br> `git commit`      |

- 3 Sections of a Git Project

|     Sections      |                              Description                               |
| :---------------: | :--------------------------------------------------------------------: |
| Working Directory |            This is the root directory of your Git project.             |
|   Staging Area    | Also called **index**, this is where all related changes are built up. |
|    Commit Area    |    This is where all artifacts are stacked safely in Git Database.     |

### Configure author and email address

- `git config --global user.name "Leon"`
- `git config --global user.email "leonlow@email.com"`

### Creating File

- Using git bash
  `echo "first file" >> filename.txt`

- Using vi editor

```
vi filename.txt
"TYPE `I` to insert contents"
"TYPE FILE CONTENTS"
"ESCAPE KEY"
:wq
```

### What is GitHub

- It is a Git repository with a web interface.
- GitHub has both free and paid plans.
- Need to create user account.
- Documentation, bug tracking, etc.
- Largest repository in the world.

### What is Fork and how to do it?

- Creating a project from another existing project.
- Encourages project advancement & collaboration.
- Encourages outside contribution.
- Forks can be updated.

### Inspecting

- `git status`: tells us the status of the working directory and staging area.
- `git log`: displays committed snapshots or commit history.

### Git Branching

- "Git Branch" represents an independent line of development.
- Request for a new working directory, staging area and project history.
- We create a branch when we want to develop a new feature or do a bug fix.
- Unstable code is never commited to main or production code base.
- A new branch get it's own working directory, index or staging area and commit history.

- `master` branch
- If you set to another branch, the commit history will be inherited into that branch.
- `development` branch: continuously moving forward.
- `release` branch: for documentation and bug fixes. temporary supporting branch.
- `feature` branch: created so that development and production branch remains undisturbed. merges back to development branch once feature is completed.

|                 Git Branching                  |                   Description                    |
| :--------------------------------------------: | :----------------------------------------------: |
|                  `git branch`                  |              To check the branches               |
|                `git branch -a`                 |  List all branches including local and remote.   |
|           `git branch <branch_name>`           |              To create a new branch              |
|          `git checkout <branch_name>`          |          To set to this current branch           |
| `git checkout -b <new_branch> <parent_branch>` | Create a new branch linked to the parent branch. |
|         `git branch <branch_name> -d`          |              To delete a git branch              |

<h1 id="git commands">Git Commands</h1>

|           Git Commands            |                          Description                           |
| :-------------------------------: | :------------------------------------------------------------: |
|            `git init`             |   Initialize an empty git repository. Create `.git` folder.    |
|            `git add .`            |            add all files in the working directory.             |
|           `git status`            |    Shows the status of working directory and staging area.     |
|          `git status -s`          |      (NOT RECOMMENDED) shows a shorter status. s = short       |
|   `git rm --cached <filename>`    |                      To unstage the file.                      |
| `git restore --staged <filename>` | To unstage the file (if changes were made in the commit stage. |
|  `git commit -m "first commit"`   |  Commit the files in the staging area, i.e., after `git add`   |
|         `git clone <url>`         |         Clone the repository onto local host machine.          |

## Other Git Commands

|                       Git Commands                        |                                   Description                                    |
| :-------------------------------------------------------: | :------------------------------------------------------------------------------: |
|                           `pwd`                           |                             Shows current directory                              |
|                    `mkdir <filename>`                     |                    Create a folder in the current directory.                     |
|                        `git help`                         |                              List of Git commands.                               |
|                       `git help -a`                       |                             List of Git sub-commands                             |
|                       `git help -g`                       |                  List of Git guides. E.g., `git help glossary`                   |
|               `git config --global --list`                |                             Check current username.                              |
|          `git config --global user.name "Leon"`           |                              Set current username.                               |
|    `git config --global user.email "leonlow@email.com`    |                                Set current email.                                |
|                     `vi ~/.gitconfig`                     |              To check all the recent configurations. `:q` to quit.               |
|                          `ls -l`                          |                      To check all the files in the folder.                       |
|                         `ls -al`                          |                      List all files including hidden files.                      |
|                           `ls`                            |                          Shows all files in the folder.                          |
|            `echo "first file" >> filename.txt`            |  Creating a file in the current folder and adding the text "first file" inside.  |
|                    `touch <filename>`                     |                      Creating a file in the current folder.                      |
|                      `vi <filename>`                      |                              Create file using VIM.                              |
|                    `cat filename.txt`                     |                          Show the content in that file.                          |
|                        `git init`                         |             Initialize an empty git repository. Create `.git` folder             |
| `cp C:/Users/leon/Downloads/initializr-verekia-4.0.zip .` |                        Copy file into current directory.                         |
|            `unzip initializr-verekia-4.0.zip`             |                                  Unzip the file                                  |
|              `rm initializr-verekia-4.0.zip`              |                                 Remove the file                                  |
|         `mv initializr/ myRepoFromExistingSource`         |                             Rename a folder or file.                             |
|                         `git log`                         |                 displays committed snapshots or commit history.                  |
|                    `git log --oneline`                    |                         Shorter form of commit history.                          |
|                   `git log <filename>`                    |                View only the commit history of a particular file.                |
|           ` git log 159dfd0..531a7a7 --oneline`           | View commit history of a set of files. (since...until, does not include "since") |
|                 `git log -n 3 --oneline`                  |                             View the last 3 commits.                             |
|                       `git branch`                        |                              To check the branches                               |
|                `git branch <branch name>`                 |                              To create a new branch                              |
