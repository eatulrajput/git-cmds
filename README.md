# Git Tutorials

### About Git & GitHub

- Git is a software and GitHub is a service to host it online. It is a version control system which allows us to track changes in files and folders

- Git creates checkpoints for the changes you make while doing.
- It tracks the changes.

- It was not the only services which were used. There were proprietary softwares there before git.

# Roadmap to learn:
- Basics
- Daily Use
- Facing the problems
- Solving problems
- Learning more...

# Terminologies
### How to check the git version, type:
```bash
   git --version
   ```

- 'ls' to check the list of files contain in that file

### How to configure Git
- How to config git for the first time

```bash
   git config --global user.email "youremail@example.com"
   git config --global user.name "Your Name"
   ```

### How to check the configuration settings:
```bash
   git config --list
   ```

### How to start
- First check the status of file: It will tell you about the files status either about changes or about initalised for git or not
```bash
   git status
   ```

- Initialise git
```bash
   git init
   ```

### Git recommends Atomic Commit
1. Keep commits centric to one feature, one component or on fix. Focus on one thing.

2. Present or Past Message:
- Depends {Present Tense, Imperative}
- Give order to code base
- Don't Care

### How to check changes done yet
```bash
git log
```

### How to check logs in oneline
```bash
git log --oneline
```

#### .gitignore
`Git` has `.gitignore` file which contains the some important files.

#### .env
`.env`: This is a files where contains API secrets, API Key, Payment Gateway Code

These are the files which you will never want to commit in your repository and never want to add in your GitHub

`.gitignore` file contains files name which you don't want to show to others or `push` in your repository. These files can be `virtual environment files` or `node-modules` or `.env` etc.

#### .gitkeep
`.gitkeep` : Due to presence of this file, `git` will not track empty folders.

### How to push to repository
1. Use git add:  
```bash
git add file-name
```
2. Add a message to show what changes have been done:
```bash
git commit -m "Your message regarding changes done"
```
3. git push
```bash
git push
```

### Why Branches Are Useful:
- Isolation: You can work on a new feature or fix bugs without disrupting the main codebase.
- Collaboration: Teams can work on different branches, and changes can be integrated later.
- Experimentation: You can try out new ideas without the risk of breaking the main project.

### Types of Branches:

- Feature branches: For working on new features. 
- Bugfix branches: For fixing bugs.
- Hotfix branches: Used for quick fixes in the production code.
- Release branches: For preparing a new release, allowing you to focus on polishing the code.

Branches are one of the key components that make Git a powerful tool for version control.

### Git Branches
- In Git, a branch is a lightweight, movable pointer to a commit. Branches allow you to work on different versions of a project simultaneously without affecting the main codebase. Here's a breakdown of how they work:

### Key Concepts of Git Branches:

1. Default Branch (main or master):
- When you initialize a Git repository, Git creates a default branch, usually named `main` or `master`. This branch serves as the base of your project and often contains the production-ready code.

- To see the branches:
```bash
git branch
```

2. Creating New Branches:

- You can create new branches to work on features, bug fixes, or experiments. New branches are typically created from an existing branch, often from `main`, so that you can isolate your work and avoid disturbing the main codebase.

```bash
git branch feature-new-function
```
3. To switching between branch, here checkout will not create a branch if not exist:
```bash
git checkout feature-new-function
```


- Or, to create and switch to the new branch in one step:
```bash
git checkout -b feature-new-function
```
- Or with switch:
```bash
git switch feature-new-function
```
- switch moves to the branch it has asked for, if that branch not exist even then it creates that branch and switches to that new branch

```bash
git switch -c feature-new-function
```
- `-c` works as to create here.

4. Merging Branches:

- After completing work on a branch, you can merge the changes back into another branch, typically the main branch.
- Example of merging:
```bash
git checkout main
git merge feature-new-function
```
5. Branch Management:

- You can view all branches in a repository by running:
```bash
git branch
```
- To delete a branch that is no longer needed:
```bash
git branch -d feature-new-function
```
#### How to rename a current branch
```bash
git branch -m new_branch_name
```

#### How to rename another branch
```bash
git branch -m old_branch_name new_branch_name
```

<br>
The `git diff` command in Git shows the differences between various states of a repository. It is commonly used to compare changes between files, commits, branches, and more. Here's how git diff works and some common use cases:

### Basic Use of git diff

1. Show Unstaged Changes:
- If you want to see the changes in your working directory that haven't been staged (i.e., not added by git add), you can run:
```bash
git diff
```

2.Show Staged Changes:

- To see the changes that have been staged for the next commit (i.e., after using git add), but not yet committed, use:

```bash
git diff --staged
```
3. Compare Two Branches:

- You can compare the changes between two branches. For example, to compare feature-branch with main, you can run:

git diff main feature-branch

### Git stash
In Git, `git stash` is a useful command that temporarily saves your changes (both tracked and untracked files) without committing them, allowing you to switch branches or perform other tasks without losing your work. Once you're ready to return to those changes, you can "unstash" them and continue working where you left off.

1. Stashing Your Changes: When you're in the middle of working on something and need to switch branches or do something else, you can stash your changes with:
```bash
git stash
```

2. Naming the stash:
```bash
git stash save "Work in progress on X feature"
```
3. Want to see the stash list:
```bash
git stash list
```
4. Apply the stash:
```bash
git stash apply
``` 
### Git Tags
Tags are a way to mark a specific point in your repository.
#### How to create a tag
```bash
git tag <tag-name>
```
#### Create an annotated tag
```bash
git tag -a <tag-name> -m "Release 1.0"
```

#### List of all tag:
```bash
git tag
```

### git rebase
Git rebase is used to change the base of a branch

### git reflog
`git reflog` shows history of your commits and allows you to see the changes that you have made to your repository over time.
```bash
git reflog
```

If you accidently deleted a branch or made changes that are no longer visible in history, you can often recover them using reflog. First find the reference to the branch or changes existed, and then reset your branch to that reference.

```bash
git reflog <commit-hash>
git reset --hard <commit-hash>

