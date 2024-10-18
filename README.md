# Git - Useful Commands

### Agenda
- `git clone URL` vs. `git remote add origin URL`
- Explanation of Flow Commands 
- `git log` vs. `git log --oneline`
- Other Useful Commands

## 1. `git clone URL` vs. `git remote add origin URL`

1-1. `git clone URL` 
The `git clone URL` command is used to create a copy of an existing repository. When you run `git clone`, Git downloads the entire content of the remote repository to the local machine, including all files, branches, and commit history. 

e.g.)

```
git clone https://github.com/user/repository.git
```

1-2. `git remote add origin URL`
If you have a local project that you want to upload to a new GitHub repository, you would first create a repository on GitHub, then use this command to link it. 

e.g.)

```
git remote add origin https://github.com/username/repository.git
```

Key Differences:
- `git clone URL` creates a new directory, copies all content from the remote repository, and sets the remote origin. 
- `git remote add origin URL` adds a remote repository to an existing local repository without creating a new directory or copying files. 


## 2. Explanation of Flow Commands 

2-1. `git init` initializes a new Git repository in the current directory. It creates a `.git` directory, where all Git tracking information is stored. 

2-2. `git add .` stages all the changes in the working directory for the next commit. The `.` means "all changes" - you can also specify individual files or directories.

2-3. `git status` displays the status of the working directory and staging area. It shows which changes have been staged, which haven't, and which files aren't being tracked by Git. 

2-4. `git commit -m "message"` commits the staged changes to the local repository with a message describing what the commit does. 

2-5. `git push` uploads the commits from the local repository to  a remote repository. It's used to share the work with other collaborators. 


## 3. `git log` vs. `git log --oneline`

3-1. `git log` command displays detailed commit history such as commit hashes, author information, date, and the commit message. 

3-2. `git log --oneline` displays a simplified, one-line-per-commit view of the history, showing only the first seven characters of the commit hash and the commit message. 

Key Differences:
- `git log` provides detailed commit history. 
- `git log --oneline` provides a compact, easy-to-read summary of the commit history. 

## 4. Other Useful Commands

4-1. `git restore filename` command is used to restore working directory files to their last committed state. This command can discard changes in the working directory. 

4-2. `git checkout -b new-branch` command is used to switch or restore working directory files. When used with a branch name, it changes the current branch; when used with a file name, it restores the file. 

4-3. `git revert commit-hash` is used to revert a commit by creating a new commit that undoes the changes of a previous commit, without removing the commit from history. 

4-4. `git mv oldname.txt newname.txt` is used to move or rename a file or directory in the working directory and stage the change for the next commit. 

4-5. `git diff` is used to show the differences between the working directory and the staging area or between commits. 
