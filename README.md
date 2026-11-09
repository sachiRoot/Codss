# Codss
Spot on! You nailed the exact workflow for FileZilla.   
To summarize the steps clearly for your exam:
1. Open Site Manager: Open FileZilla and click Site Manager to create a new site configuration.   
2. Enter Connection Details:
  - Protocol: Select SFTP - SSH File Transfer Protocol.   
  - Host: Enter the target server IP (e.g., 193.1.3.17).   
  - Port: Enter 22.   
  - Logon Type: Normal.   
  - User & Password: Enter your assigned credentials (e.g., Student01).   
3. Connect: Click Connect to establish the secure SSH session.


Exactly! You've got the exact command sequence down pat.
Just a tiny correction on the spacing for the email command (make sure --global has no spaces inside it like -- global), but otherwise that is the precise order of commands:   
1. cd: Navigate into your target project directory.   
2. git config --global user.name "...": Set your global Git username.   
3. git config --global user.email "...": Set your global Git email address.   
4. git config --global --list: Verify that your configuration settings were applied correctly.   
5. git init: Initialize an empty Git repository in that folder.   
6. git status: Check the status of your workspace to see your untracked files highlighted in red.



1. SFTP File Transfer (FileZilla)
- Steps to Remember:
  1. Open FileZilla $\rightarrow$ Click Site Manager $\rightarrow$ Create a New Site.   
  2. Set Protocol to SFTP - SSH File Transfer Protocol.   
  3. Enter Host (IP address), Port (22), and Logon Type: Normal.   
  4. Enter your Username (e.g., Student01) and Password $\rightarrow$ Click Connect.   
  5. Drag and drop files between the local pane (left) and remote server pane (right).   
2. Local Git Initialization (Lab 7)
- Commands to Remember:
- Plaintext
- 
- cd C:\Users\HP\Desktop\...\your_folder
- git config --global user.name "sachiRoot"
- git config --global user.email "2006sachinaik@gmail.com"
- git config --global --list
- git init
- git status
- (Note: Untracked files show up in red).   
3. Staging, Committing, and Pushing to GitHub (Lab 8)
- Commands to Remember:
- Plaintext
- 
- git add .
- git commit -m "initial commit"
- git remote add origin "https://github.com/sachiRoot/cloudcomputing.git"
- git branch -m main
- git push -u origin main
- Authentication Note: When git push prompts for credentials, paste your GitHub Personal Access Token (PAT) instead of your password.


Lab 9: Collaborative Workflows (Clone, Pull, Push)
- What's happening: You are working on a team project hosted on GitHub. Instead of creating a new repository locally, you download an existing shared repository using git clone, pull the latest updates from teammates using git pull, make your changes, and push them back.
- Exact Commands to Remember:
- Plaintext
- 
- git clone https://github.com/username/repository.git
- cd repository_folder
- git pull
- git add .
- git commit -m "update message"
- git push
Lab 10: Merge Conflicts & Cloud MySQL (Aiven)
- What's happening:
  1. Git Merge Conflicts: When you and a teammate edit the exact same line of a file (like README.md) at the same time, Git flags a conflict. You fix the file, stage it, commit it, and push it.   
  2. Aiven Cloud MySQL: You deploy a managed MySQL database on Aiven, connect to it securely using MySQL Workbench with an SSL certificate (ca.pem), and run SQL queries to create tables and insert records.
- Exact Git Conflict Fix Commands:
- Plaintext
- 
- git pull
- (Conflict occurs in file, open and edit file to fix)
- git add .
- git commit -m "resolved conflict"
- git push
- ```[cite: 13, 14]
- SQL Script to Remember:
- SQL
- 
- SHOW DATABASES;CREATE TABLE students (
-     student_id INT PRIMARY KEY,
-     name VARCHAR(50),
-     course VARCHAR(50),
-     marks INT
- );SHOW TABLES;INSERT INTO students (student_id, name, course, marks)VALUES 
-     (101, 'RAHUL', 'cloud computing', 82),
-     (102, 'PRIYA', 'cloud computing', 91),
-     (103, 'SITARAM', 'cloud computing', 77),
-     (104, 'SIYA', 'cloud computing', 97),
-     (105, 'ROHAN', 'cloud computing', 87);
