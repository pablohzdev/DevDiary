# Basics: Git & GitHub Introduction – Version Control

> **Disclaimer:**  
> These notes reflect my personal understanding of version control concepts.  
> They are written for learning purposes and do not reproduce proprietary documentation.

---

## 1. What Is a Version Control System (VCS)?

A **Version Control System (VCS)** records changes to a file or a set of files over time, allowing you to recall specific versions later.

In software development, source code is the most common type of file being version controlled, but version control can be applied to almost any type of file.

A VCS allows you to:
- Revert individual files to a previous state
- Restore an entire project to an earlier version
- Compare changes over time
- Identify who made a change and when
- Recover files if something goes wrong

Using a VCS provides these benefits with very little overhead and greatly reduces the risk of losing work.

---

## 2. Local Version Control Systems

Early **local VCSs** used a simple database to track changes to files.

One example is **RCS (Revision Control System)**, which worked by storing patch sets (differences between file versions) on disk.  
By applying these patches, the system could reconstruct any version of a file from its history.

While useful, local VCSs were limited to a single machine and did not support collaboration well.

---

## 3. Centralized Version Control Systems

**Centralized Version Control Systems (CVCSs)** use a single central server that stores all versioned files.  
Clients check out files from this server and commit changes back to it.

### Advantages
- Everyone has a shared view of the project
- Administrators can control permissions centrally

### Disadvantages
- The central server is a **single point of failure**
- If the server goes down, collaboration stops
- If backups are missing, data loss can be severe

For many years, this model was the standard for version control.

---

## 4. Distributed Version Control Systems

**Distributed Version Control Systems (DVCSs)**, such as **Git**, **Mercurial**, and **Darcs**, take a different approach.

Instead of checking out only the latest snapshot, each client:
- Downloads a **full copy of the repository**
- Includes the complete project history

This means:
- Work can continue even if the server is unavailable
- Any client repository can be used to restore the server
- Collaboration is faster and more flexible

Git is the most widely used DVCS today.

---

## 5. What Is GitHub?

**GitHub** is a cloud-based platform that hosts Git repositories and enables collaboration.

GitHub allows you to:
1. Store and showcase your code
2. Track and manage changes over time
3. Review code and suggest improvements
4. Collaborate without affecting others’ work prematurely

GitHub builds on Git by adding tools for collaboration, project management, and code review.

---

## 6. About Git

**Git** is a distributed version control system that intelligently tracks changes in files.  
It is especially useful when multiple people are working on the same project simultaneously.

A typical Git workflow involves:
1. Creating a branch from the main codebase
2. Making changes independently in that branch
3. Merging changes back into the main branch
4. Letting Git handle change tracking and conflict resolution

This workflow allows teams to work safely and efficiently.

---

## 7. How Git and GitHub Work Together

When you upload files to GitHub, they are stored in a **Git repository**.  
Each time you make a change (a **commit**), Git tracks and records it.

You can perform some Git-related actions directly on GitHub, such as:
- Creating repositories
- Creating branches
- Editing files

However, most development happens **locally** on a developer’s machine.  
Changes are then synchronized with GitHub by:

- **Pulling** updates from the remote repository
- **Pushing** local commits to the remote repository

Git manages the technical merging of changes, while GitHub provides collaboration features such as **pull requests**.

---

## References

The following resources were used as **conceptual learning references**:

- Git Book – *About Version Control*  
  https://git-scm.com/book/en/v2/Getting-Started-About-Version-Control

- GitHub Docs – *About Git and GitHub*  
  https://docs.github.com/en/get-started/start-your-journey/about-github-and-git

---

## Final Notes

Version control is a foundational skill for modern software development.  
Understanding Git and GitHub early makes collaboration, experimentation, and recovery from mistakes significantly easier.