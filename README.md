# Git Tutorials

### About Git & GitHub

- Git is a software and GitHub is a service to host it online.

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

### gitignore
`Git` has `.gitignore` file which contains the some important files.

#### .env
`.env`: This is a files where contains API secrets, API Key, Payment Gateway Code

These are the files which you will never want to commit in your repository and never want to add in your GitHub

`.gitignore` file contains files name which you don't want to show to others or `push` in your repository. These files can be `virtual environment files` or `node-modules` or `.env` etc.