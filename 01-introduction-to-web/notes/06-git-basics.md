# Basics: Git & GitHub – Intro

> **Disclaimer**  
> These notes represent my personal understanding of fundamental computing concepts.  
> They are written for learning purposes and do not reproduce any specific course material.

---

## Environment

- **Git version:** 2.5  
- **Current branch:** `main`

---

## Key Concepts and Terms

### Branch
A parallel version of your code that exists within the same repository.  
It does not affect the primary (`main`) branch unless it is merged.

### Clone
To download a complete copy of a repository from GitHub, including the full history of every file and folder.

### Fork
A new repository that shares code and visibility settings with the original (*upstream*) repository.  
Forks allow independent development without affecting the original project.

### Merge
The process of taking changes from one branch and applying them to another branch.

### Pull Request
A request to merge changes from one branch into another.  
Pull requests are commonly used for code review and collaboration.

### Remote
A version of a repository hosted on a remote server (such as GitHub), rather than on your local machine.

### Upstream
The original repository from which a fork or clone was created.  
The corresponding repository that depends on it is often referred to as *downstream*.

---

## Working with GitHub Repositories

### General Information
- https://docs.github.com/en/repositories/creating-and-managing-repositories/about-repositories

### Creating a New Repository
- https://docs.github.com/en/repositories/creating-and-managing-repositories/quickstart-for-repositories
- https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-new-repository

### Cloning a Repository Locally
- https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository

---

## Learning Git Branching

To practice Git branching concepts, I use the following interactive tool:

- https://learngitbranching.js.org

> You can change the language using the icon in the bottom-right corner.

The website describes itself as **"a visual and interactive way to learn Git on the web."**  
I have tried it before and found it very useful. It allows you to work with **local and remote branches** through different levels of increasing difficulty.

---

## Git Commands Covered

### Local Git

So far, I have completed the following topics (up to **rebase**):

- `git commit`

- `git branch`
- `git checkout`
- `git merge`
- `git rebase`

---

### Remote Git

#### `git clone`
Creates a local copy of a remote repository.

#### `git checkout origin/main`
Checks out the remote tracking branch.

#### `git fetch`
`git fetch` performs two main actions:

1. Downloads commits that exist on the remote repository but are missing locally.
2. Updates remote-tracking branches (for example, `origin/main`).

`git fetch` synchronizes your local view of the remote repository without modifying your working branch.

Remote branches reflect the state of the remote repository the last time you communicated with it.  
`git fetch` is how you update that information.

> `git fetch` usually communicates with the remote repository over the Internet (using protocols such as `https://` or `git://`).

#### `git pull`
A shorthand command that performs:

1. `git fetch`
2. Followed by a merge of the fetched branch into the current branch

#### `git push`
Uploads your local commits to the remote repository.

---

## Notes

- These notes are intended as a learning diary.
- All definitions are written in my own words.
- External links are included for reference and further study.