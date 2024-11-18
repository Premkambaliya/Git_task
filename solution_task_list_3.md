## **Task List: Focused on Repository Management, Commits, Branching, and Merging**

### **Part 1: Creating and Cloning Repositories**

#### **Task 1: Create a Local Git Repository**
1. Create a new project folder:  
   ```bash
   mkdir MyProject
   cd MyProject
   ```
   ans:- mkdir create new folder 
   ans:- enter in folder

2. Initialize it as a Git repository:  
   ```bash
   git init
   ```
ans:- initialize reposatory

3. Verify the repository status:  
   ```bash
   git status
   ```
   - **Example Output**:  
     ```
     On branch main
     No commits yet
     nothing to commit (create/copy files and use "git add" to track)

ans:- cheak files to that's add or not add in repo

#### **Task 2: Clone a Remote Repository**
1. Clone a GitHub repository:  
   ```bash
   git clone https://github.com/username/repo.git
   ```
ans:- git clone clone any website and you put that your github account

2. Verify the cloned repository structure:  
   ```bash
   cd repo
   ls -a
   ```
   - **Output**: The `.git` folder should be present.
   
ans:- go in to the repo folder
ans:- all list of files
---

### **Part 2: Understanding Commits and Commit Messages**

#### **Task 3: Commit Changes Locally**
1. Create a new file and add content:  
   ```bash
   echo "Welcome to Git" > README.md

   ```
ans:- make new files and in file some text

2. Stage the file:  
   ```bash
   git add README.md
   ```
   - **Explanation**: `git add` moves changes to the staging area.

ans:- git add . all files add in repo

3. Commit the staged file:  
   ```bash
   git commit -m "Initial commit: Added README.md"
   ```
   - **Explanation**: Commits save the current state of the repository with a message describing the change.
 
 ans:- commit files and enter a new message
 
   
#### **Task 4: Write Effective Commit Messages**
1. Create a detailed commit message:  
   ```bash
   git commit -m "Added initial version of README.md with project overview"
   ```
   - **Explanation**: Commit messages should follow conventions such as starting with a capital letter, being concise, and using the imperative mood.

 ans:- commit files and enter a new message


2. Commit multiple files with one message:  
   ```bash
   touch file1.txt file2.txt
   git add .
   git commit -m "Added two new files for feature setup"
   ```
ans:- git add . all files add in repo
ans:- commit files and enter a new message

   
---

### **Part 3: Viewing Commit History with `git log`**

#### **Task 5: View Detailed Commit History**
1. View full commit logs:  
   ```bash
   git log
   ```
   - **Explanation**: Shows a detailed list of commits with hash, author, date, and message.
ans:- show all commit hestory 
2. View commit history in a compact format:  
   ```bash
   git log --oneline
   ```
   - **Example Output**:  
     ```
     e23d8a7 Added initial version of README.md
     f7b3c62 Initial commit: Added README.md
     ```
     

#### **Task 6: Customize Log Outputs**
1. View logs with a graphical representation:  
   ```bash
   git log --oneline --graph --decorate
   ```

2. Filter logs for a specific file:  
   ```bash
   git log README.md
   ```
   
   
ans:- Filters the commit history to show only those commits that affected the specified file
   


### **Part 4: Understanding Branching and Merging**

#### **Task 7: Understanding Branching**
1. List all branches:  
   ```bash
   git branch
   ```
   - **Explanation**: Displays the current branch and all other branches.

ans:-This command lists all the branches in your Git repository.

2. Create a new branch:  
   ```bash
   git branch feature-branch
   ```
   - **Explanation**: Creates a new branch without switching to it.

ans:- git branch name

3. Switch to the new branch:  
   ```bash
   git checkout feature-branch
   ```
  ans:- This command is used to switch into any branch.

   - **Alternative Command**:  
     ```bash
     git checkout -b feature-branch
     ```
     - **Explanation**: Creates and switches to the branch in one command.
    
ans:- This Command create new branch and switch into it in one step.
     
---

### **Part 5: Creating and Working with Branches**

#### **Task 8: Make Changes in a Branch**
1. Add content to a file in the new branch:  
   ```bash
   echo "Feature in progress" > feature.txt
   git add feature.txt
   git commit -m "Added feature.txt in feature-branch"
   ```
    ans:- echo using for make a new file and in file write a message

    ans:- git add use for you add a file in repo but first you initilaizetion repo 
    
    ans:- after git add you use git commit that useing for any message write in file in your repo


#### **Task 9: Merging Branches**
1. Switch back to the `main` branch:  
   ```bash
   git checkout main
   ```
 ans:- This command switch any branch to main branch.
2. Merge the `feature-branch` into `main`:  
   ```bash
   git merge feature-branch
   ```
   - **Explanation**: Combines the changes from `feature-branch` into `main`.
   
   
---

### **Part 6: Resolving Merge Conflicts**

#### **Task 10: Simulate a Merge Conflict**
1. Modify the same line in a file on two branches:  
   ```bash
   echo "Main branch content" > conflict.txt
   git add conflict.txt
   git commit -m "Added conflict.txt in main branch"
   ```
    ans:- echo using for make a new file and in file write a message

    ans:- git add use for you add a file in repo but first you initilaizetion repo 
    
    ans:- after git add you use git commit that useing for any message write in file in your repo


2. Switch to the other branch and make conflicting changes:  
   ```bash
   git checkout feature-branch
   echo "Feature branch content" > conflict.txt
   git add conflict.txt
   git commit -m "Modified conflict.txt in feature-branch"
   ```
    ans:- switch branch

    ans:- echo using for make a new file and in file write a message

    ans:- git add use for you add a file in repo but first you initilaizetion repo 
    
    ans:- after git add you use git commit that useing for any message write in file in your repo


3. Merge `feature-branch` into `main`:  
   ```bash
   git checkout main
   git merge feature-branch
   ```
ans:- swith branch


4. Resolve the conflict by editing the file and choosing the correct version:  
   - Open `conflict.txt` and decide which changes to keep.
   - Stage the resolved file:  
     ```bash
     git add conflict.txt
     ```
   - Commit the merge:  
     ```bash
     git commit -m "Resolved conflict in conflict.txt"
     ```
     
ans:- add new file with file name

ans:- commit any file
---

### **Part 7: Deleting and Renaming Branches**

#### **Task 11: Delete a Branch**
1. Delete a local branch:  
   ```bash
   git branch -d feature-branch
   ```
   - **Explanation**: This deletes the branch only if it has been fully merged.  
ans:- delete branch
2. Force-delete a branch:  
   ```bash
   git branch -D feature-branch
   ```
ans:- delete branch with merge  


#### **Task 12: Rename a Branch**
1. Rename the current branch:  
   ```bash
   git branch -m new-branch-name
   ```
ans:- rename that branch

2. Rename another branch (not checked out):  
   ```bash
   git branch -m old-branch-name new-branch-name
   ```
ans:- rename that branch
  

   
---

### **Consolidated Flow Summary**

1. Start by creating and cloning repositories.
2. Learn to commit changes effectively with clear messages.
3. Explore commit history using various `git log` commands.
4. Understand branching and practice creating, switching, and merging branches.
5. Dive into resolving merge conflicts.
6. End by managing branches through deletion and renaming.