# **GIT**
### **History**
Git was created by Linus Torvalds in 2005 for development of the Linux kernel, with other kernel developers contributing to its initial development. Since 2005, Junio Hamano has been the core maintainer.
### **What is GIT ?**
Git is software for tracking changes in files, usually used for coordinating work. Its goals include speed, data integrity, and support for distributed, non-linear workflows. It is like tree system, files coordination and updates are stored simultaneously. mostly useful for software developers. files security is the most useful part for developers. 
### **What is Version Control System ?**
A version Control System is the tracking and managing changes to software code. Version control systems are software tools that help software teams manage changes to source code over time. 

### **GIT Commands**
- We create first empty repository in our local system
    ```
    git init .  // git repository created
    ```
- Then we check the git status.
    ```
    git status      // current status of file
	   IF :  Red   - untracted file
	        green - changes to the commited file
	        commit - committed
    ```
- Then We add the untracked files
    ```
    git add <name> // to add file into git repository
	- to add something into file use cat >> <file> command.
	git add . or *  //added all the files
    ```
- Which git shows the location of git
    ```
    which git
    ```
- next step is commit the code to store into version history.
    ```
    git commit -m"Added readme file"    // commit the file    
    ```
- we check the commit history by using this command
    ```
    git log // prints all the committed ID's and status.
    ```
- shows changes in the file after commit.
     ```
    git show <commit ID>
	green and '+' - shows content is added to existing file
	Red and '-' - shows content is removed to existing file
    ```
- shows changes into the file but not committed yet
    ```
    git diff <file> .
	Red - removed content shows into red
	Green - added content shows into green
    ```
    
#### **Branches in GIT**
- To check the current branch
    ```
    git branch // pointing to current branch
	    //(HEAD -> master) - head is like pointer and master is an branch
	```
- To create  a new branch we can do
    ```
	git branch <name> // created new branch from master
	```
- To delete branch
    ```
	git branch <name> -d/D // to delete branch
    ```
- To retrive the deleted branch
    ```
    git checkout -- <deleted branch> 
    ```
- We can jump from one branch to other by using
    ```
    git checkout <name>     // head pointing to the <name> branch
	```
- revert all the files to the last commited state
    ```
	git checkout -- .
    ```
- To merge the branch
    ```
    git merge <branch name>
    ```

#### **Here we can Connect with existing Repository and pull the code, push the code.**
- To connect with existing repository
    ```
    git remote add origin <remote>
    ```
- We can push the code to the origin then to any of the branch we connect.
    ```
    git push origin master //push code to origin(link) at master (branch)
    ```
- To clone the existing Repository in our local system we use
    ```
    git clone <remote repo url> 
    ```
- To Fetch the origin to branch
    ```
    git fetch origin <branch> 
    ```
-  if we want to merge two branches first checkout branch then add <name> branch into the first branch
    ```
    git merge <branch>
    ```
- From stagged to untracked stage
    ```
    git reset HEAD <file name>
    ```
- We can pull the branch from Remote Repo.
    ```
    git pull origin master // to pull branch from remote
    ```
- to save the current state of working directory when we want to reverts the working directory to match the HEAD commit.
    ```
    git stash 
    ```
