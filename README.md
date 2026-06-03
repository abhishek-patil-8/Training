# How to Push a Local Project to GitHub via Command Prompt

This guide walks you through the process of taking an existing local project (like a Spring Boot workspace) and 
pushing it to a new GitHub repository using the Windows Command Prompt (CMD).

## Prerequisites
1. **Git is installed** on your machine.
2. You have a **GitHub account**.
3. You have created a **new, empty repository** on GitHub (do not initialize it with a README, `.gitignore`, or license).
   You will need the repository URL (e.g., `https://github.com/your-username/your-repo-name.git`).

## Step-by-Step Guide

**### 1. Navigate to Your Project Folder**
Open your Command Prompt and use the `cd` (change directory) command to go to the exact folder where your project is located.

cd path\to\your\project\folder

**### 2. Initialize the Git Repository**

Turn your local folder into a Git tracking repository. *(If it is already a repository, this will just safely reinitialize it).*
git init

**### 3. Stage Your Files**

Tell Git to track all the files in your folder. The period `.` means "add everything" (respecting your `.gitignore` rules).

git add .

**### 4. Commit Your Changes**

Save the current state of your project locally.

git commit -m "Initial commit"

**### 5. Set the Main Branch**

Ensure your primary branch is named `main` (the modern standard for GitHub), rather than the older default `master`.

git branch -M main

**### 6. Link to GitHub**

Connect your local repository to your remote GitHub repository. Replace the URL with your specific GitHub link.

git remote add origin [https://github.com/your-username/your-repo-name.git](https://github.com/your-username/your-repo-name.git)

**### 7. Push Your Code**

Upload your committed files to GitHub. The `-u` flag remembers your choice, so in the future, you only need to type `git push`.

git push -u origin main
