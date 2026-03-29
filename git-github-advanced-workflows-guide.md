# Git and GitHub Advanced Workflows Guide

## Table of Contents
1. [Advanced Git Workflow](#advanced-git-workflow)
2. [Conflict Resolution](#conflict-resolution)
3. [Interview Questions](#interview-questions)

## Advanced Git Workflow
In this section, we will cover some advanced workflows that can enhance your version control process.  

### Feature Branch Workflow
This workflow involves creating a new branch for each feature or change, keeping the main branch clean. Once the feature is completed, a pull request is created to merge it.  

### Git Flow
Git Flow is a branching model that defines a strict branching pattern, including main, develop, and feature branches.  

### Forking Workflow
Useful in open-source projects, this workflow allows contributors to create a personal copy of the repository and propose changes via pull requests.

## Conflict Resolution
When working with Git, conflicts can arise during merges or rebases. Here’s how to handle them:

### Steps to Resolve Conflicts:
1. **Identify Conflicts**: Git will notify you of conflicts during the merge process.
2. **Edit Conflicted Files**: Open the files with conflicts marked by Git and make the necessary edits to resolve them.
3. **Add Resolved Files**: Use `git add <file>` to mark conflicts as resolved.
4. **Continue Merge**: Use `git merge --continue` to complete the merge process.

## Interview Questions
1. What is the difference between `git merge` and `git rebase`?
2. How do you squash commits in Git?
3. How can you resolve merge conflicts in Git?
4. What are the different ways to undo changes in Git?
5. Can you explain what a pull request is and how it differs from a merge?

---

This guide is structured to help developers understand and implement advanced Git workflows, effectively resolve conflicts, and prepare for related interview questions.