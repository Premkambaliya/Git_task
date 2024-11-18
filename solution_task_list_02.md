## **Part 1: Git Basics**

### **Task 1: Install and Configure Git**
1. Install Git from [git-scm.com](https://git-scm.com/).  
2. Configure your global Git settings:  
   ```bash
   git config --global user.name "Your Name"
   git config --global user.email "your-email@example.com"
   ```
   ans:- git config globel using for configrution settings set and manage.


3. Verify the configuration:

```
git config --list
```
ans:- git config --list using for show a list in list our name ,email , path etc.


## **Task 2: Initialize a Repository**

1. Create a directory and initialize it as a Git repository:

```
mkdir MyProject
cd MyProject
git init
```
ans:- mkdir using for make new folder and cd using for you go inside any folder and git init initilize your repo


## **Part 2: Basic Workflow**

### **Task 3: Creating and Committing Files**

1. Create a file:

```
echo "Hello Git" > file1.txt
```
   ans:- echo using for make a new file and in file write a message

2. Stage and commit the file:
```
git add file1.txt
git commit -m "Initial commit: Added file1.txt"
```

   ans:- git add use for you add a file in repo but first you initilaizetion repo 
   ans:- after git add you use git commit that useing for any message write in file in your repo


### **Task 4: Viewing Changes**

1. Modify the file:
```
echo "Git is awesome!" >> file1.txt
```
   ans:- echo using for make a new file and in file write a message

2. Check file status and differences:
```
git status
git diff
```
   ans:- git status useing for cheak a status of your files
ans:- git diff show changes between your working directory and the index or between commits. Use git diff to see unstaged changes and git diff --staged for staged ones. You compare commits or branches 

### **Task 5: Undoing Changes**
1. Unstage a staged file:
```
git reset file1.txt
```
* only affects the staging area

2. Discard uncommitted changes:
```
git checkout -- file1.txt
```
* Restores the file to its last committed state.


### **Part 3: Branching and Merging**

### **Task 6: Branch Management**

1. Create a branch and switch to it:
```
git checkout -b feature-branch
```

ans:- create new branch

2. List branches:
```
git branch
```

ans:- that give branch list

3. Rename a branch:
```
git branch -m feature-branch feature-enhanced
```
ans:- change branch name

### **Task 7: Merging Branches**

1. Merge ```feature-enhanced``` into ```main```:

    ```
    git checkout main
    git merge feature-enhanced
    ```


 ### **Task 8: Handling Merge Conflicts**

 1. Create two conflicting branches and resolve a conflict manually:

```
git merge <branch-name>
```

2. Create two conflicting branches and resolve a conflict manually:

```
git add <resolved-file>
git commit
```


## **Part 4: Remote Repositories**

### **Task 9: Remote Setup**

1. Add a remote repository:

```
git remote add origin https://github.com/your-username/repo.git
```


2.
Verify the remote:

```
git remote -v
```


### **Task 10: Push and Pull**

1. Push changes to the remote repository:

```
git push -u origin main
```

ans:- push file to your local to globle

2. Pull changes from the remote:
```
git pull origin main
```


#### **Task 11: Cloning a Repository**
1. Clone a remote repository:  
   ```bash
   git clone https://github.com/your-username/repo.git
   ```
 ans:- git clone copi any repository with help remote link

---

### **Part 5: Advanced Git**

#### **Task 12: Stashing Changes**
1. Save uncommitted changes:  
   ```bash
   git stash
   ```
2. Apply stashed changes:  
   ```bash
   git stash apply
   ```
3. Drop the stash:  
   ```bash
   git stash drop
   ```

#### **Task 13: Tagging Commits**
1. Create and annotate a tag:  
   ```bash
   git tag -a v1.0 -m "Version 1.0 release"
   ```
2. Push the tag to the remote:  
   ```bash
   git push origin v1.0
   ```
 

#### **Task 14: Rewriting Commit History**
1. Use interactive rebase to modify commit messages:  
   ```bash
   git rebase -i HEAD~3
   ```
   - Replace `pick` with `edit` or `squash` as needed.
   


#### **Task 15: Cherry-Picking Commits**
1. Apply a specific commit to another branch:  
   ```bash
   git cherry-pick <commit-hash>
   ```



### **Part 6: Collaboration**

#### **Task 16: Forking and Pull Requests**
1. Fork a repository and clone it locally:  
   ```bash
   git clone https://github.com/your-username/forked-repo.git
   ```
    ans:- git clone copi any repository with help remote link

2. Make changes and push them:  
   ```bash
   git checkout -b fix-typo
   echo "Typo fixed" >> README.md
   git commit -m "Fixed a typo"
   git push origin fix-typo
   ```
    ans:- make new branch and switch branch

    ans:- echo using for make a new file and in file write a message

    ans:- after git add you use git commit that useing for any message write in file in your repo

    ans:- git push use for push repo in github

3. Open a pull request on GitHub.
   *  Fork: Forking a repository on GitHub creates a copy of someone repository in your own GitHub account.

*   git clone <forked-repo-url>: This command clones your forked repository from GitHub to your local . 

 *  git checkout -b <branch-name> : This command creates a new branch and switches to that branch.

  * echo "Typo Fixed" >> README.md: This command add some text "Typo fixed" in README.md file.

  * git add README.md: Stages the README.md file for committ.

  * git commit -m "Fixed a typo": Commits changes with a message.

 *  git push origin fix-typo: This command pushes fix-typo branch and changes the fork on GitHub.
   

   #### **Task 17: Simulating Team Collaboration**

   1. Simulate a conflict by having two users modify the same file.

   2. Practice resolving the conflict as a team.
   
   Explaination :- 1. Create two branches:
   ```
   git branch branch-A
   git branch branch-B
   ```
   2. Modify the same line in README.md in both branches.

   3. Merge branch-A into main:
   ```
   git checkout main
   git merge branch-A
   ```
   4. Attempt to merge branch-B into main (this will cause a conflict):
   ```
   git merge branch-B 
   ```
   5. Resolve the conflict manually in README.md, then:
   ```
   git add README.md
   git commit -m "Resolved merge conflict between branch-A and branch-B"
   ```
   
---

### **Part 7: Ignoring Files**

#### **Task 18: Using .gitignore**
1. Create a `.gitignore` file:  
   ```bash
   echo "node_modules/" > .gitignore
   git add .gitignore
   git commit -m "Added .gitignore"
   ```
2. Verify that ignored files are not staged:  
   ```bash
   git status
   ```
  * echo "node_modules/" > .gitignore: This command creates a .gitignore file and adds the line node_modules/ to it.

  * git add .: The command stages all changes in the current directory for commit.

 *  git commit -m "":

 *  git status: This command shows the current state of your working directory and staging area.
   


### **Part 8: Automation and Cleanup**

#### **Task 19: Cleaning the Repository**
1. Remove untracked files:  
   ```bash
   git clean -f
   ```
  * This command is used to remove untracked files from your working directory.
   

#### **Task 20: Aliases and Shortcuts**
1. Create an alias for frequently used commands:  
   ```bash
   git config --global alias.st status
   git config --global alias.cm commit
   ```
2. Use the alias:  
   ```bash
   git st
   git cm -m "Message"
   ```
* git config: Modifies Git's configuration files.
  * --global: Applies the configuration globally for all repositories on your system.

 *  alias.st: Creates a shortcut for the git status command. After this, you can type git st instead of git status.

 *  alias.cm: Creates a shortcut for the git commit command. After this, you can type git cm instead of git commit.
   
 *  git st: Execute the git status.

 *  git cm -m "M": Execute the git commit im "message".
   




