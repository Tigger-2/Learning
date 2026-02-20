# Git Learning Guide

## Introduction

Git is a distributed version control system that allows you to track changes in your code, collaborate with other developers, and manage different versions of your project. Whether you're working on a personal project or collaborating with a large team, understanding Git is essential for modern software development.

### Why Git Matters

- **Version Control**: Keep a complete history of your project changes with the ability to revert to any previous state
- **Collaboration**: Work seamlessly with other developers by tracking who made what changes and when
- **Branching & Merging**: Develop features independently without affecting the main codebase
- **Code Review**: Use pull requests to review code before it's merged into the main project
- **Backup & Recovery**: Your code is stored in multiple locations, protecting against data loss

### Key Concepts

- **Repository**: A folder containing your project files and Git history
- **Commit**: A snapshot of your changes with a message describing what changed
- **Branch**: An independent line of development where you can work on features separately
- **Remote**: A version of your repository hosted on a server (like GitHub, GitLab, Bitbucket)
- **Staging Area**: A place to prepare changes before committing them

---

## Common Git Commands Quick Reference

| Command | Usage | When to Use |
|---------|-------|------------|
| `git init` | Initialize a new Git repository in the current directory | When starting a new project |
| `git clone <url>` | Create a local copy of a remote repository | When downloading an existing project from GitHub/GitLab |
| `git status` | Show the current state of the repository (modified, staged, untracked files) | Frequently, to see what changes you've made |
| `git add <file>` | Stage a specific file for commit | Before committing, to include specific changes |
| `git add .` | Stage all modified and new files for commit | When you want to commit all current changes |
| `git commit -m "message"` | Create a snapshot of staged changes with a descriptive message | After staging changes, to save them to history |
| `git commit -am "message"` | Stage and commit all modified files in one command | For quick commits of tracked files (skips staging step) |
| `git log` | Display the commit history with details (author, date, message) | To review project history and find specific commits |
| `git log --oneline` | Show commit history in a condensed format | For a quick overview of recent commits |
| `git diff` | Show differences between unstaged changes and the last commit | To review what you've changed before committing |
| `git diff --staged` | Show differences between staged changes and the last commit | To review staged changes before committing |
| `git branch` | List all local branches in the repository | To see what branches exist locally |
| `git branch <branch-name>` | Create a new branch with the specified name | When starting work on a new feature |
| `git branch -d <branch-name>` | Delete a local branch | After merging a feature, to clean up branches |
| `git checkout <branch-name>` | Switch to an existing branch | When moving to a different branch to work |
| `git checkout -b <branch-name>` | Create and switch to a new branch in one command | Quick way to start a new feature branch |
| `git switch <branch-name>` | Modern alternative to checkout for switching branches | Same as checkout; newer, more explicit syntax |
| `git switch -c <branch-name>` | Modern alternative to checkout -b | Create and switch to new branch with newer syntax |
| `git merge <branch-name>` | Merge another branch into the current branch | When combining feature branch changes into main/develop |
| `git rebase <branch-name>` | Reapply commits from current branch onto another branch | To maintain a linear history instead of merge commits |
| `git pull` | Fetch and merge remote changes into the current branch | To get latest updates from the remote repository |
| `git pull --rebase` | Fetch remote changes and rebase instead of merge | To avoid merge commits and keep history clean |
| `git fetch` | Download objects and refs from the remote repository (no merge) | To see what others have committed without merging |
| `git push` | Upload local commits to the remote repository | When you're ready to share your changes |
| `git push -u origin <branch-name>` | Push a new branch to remote and set upstream tracking | When pushing a branch for the first time |
| `git push origin <branch-name>` | Push a specific branch to the remote repository | To update a branch on the remote |
| `git remote -v` | Show all remote repositories with their URLs | To verify which remote repositories are configured |
| `git remote add <name> <url>` | Add a new remote repository | When configuring access to a GitHub/GitLab repository |
| `git stash` | Temporarily save uncommitted changes without committing them | When you need to switch branches but aren't ready to commit |
| `git stash pop` | Restore previously stashed changes | After switching branches, to reapply saved changes |
| `git stash list` | Show all stashed changesets | To see what changes you've temporarily saved |
| `git reset --soft HEAD~1` | Undo the last commit but keep changes staged | If you committed too early and want to modify |
| `git reset --hard HEAD~1` | Undo the last commit and discard all changes | To completely undo the last commit |
| `git reset <file>` | Unstage a file (opposite of `git add`) | When you've staged a file by mistake |
| `git revert <commit-hash>` | Create a new commit that undoes a previous commit | To safely undo changes in shared/public branches |
| `git tag <tag-name>` | Create a tag at the current commit | To mark important commits (releases, milestones) |
| `git tag <tag-name> <commit-hash>` | Create a tag at a specific commit | To tag older commits |
| `git push origin <tag-name>` | Push a specific tag to the remote | To share version tags with the team |
| `git show <commit-hash>` | Display details (changes) of a specific commit | To review what changed in a specific commit |
| `git blame <file>` | Show who made changes to each line in a file | To track down when specific changes were made |
| `git config --global user.name "Name"` | Set your global Git username | First-time setup for identifying your commits |
| `git config --global user.email "email"` | Set your global Git email | First-time setup for identifying your commits |
| `git config --list` | Display all Git configuration settings | To verify your Git configuration |

---

## Additional Resources

- [Official Git Documentation](https://git-scm.com/doc)
- [Pro Git Book (Free)](https://git-scm.com/book/en/v2)
- [Atlassian Git Tutorials](https://www.atlassian.com/git/tutorials)
- [GitHub Learning Lab](https://lab.github.com/)
- [Visualizing Git Concepts](https://git-school.github.io/visualizing-git/)
- [Interactive Git Learning](https://learngitbranching.js.org/)
- [Git Cheatsheet](https://github.github.com/training-kit/downloads/github-git-cheat-sheet.pdf)

## Next Steps

1. Install Git on your machine from [git-scm.com](https://git-scm.com/)
2. Configure your username and email with the `git config` commands
3. Create your first repository and practice the basic commands
4. Explore GitHub/GitLab to understand remote repositories
5. Learn branching and merging strategies for team collaboration
