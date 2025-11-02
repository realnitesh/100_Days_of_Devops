# Setting Up a Central Bare Git Repository

This guide explains how to create and use a bare Git repository for team collaboration, reflecting real practices in DevOps workflows.

### What is a Bare Repository?
A bare Git repository contains only version control information and no working files. It is ideal as a "central remote repo" for development teams, similar to what GitHub or GitLab uses on their servers.

---

## Step 1: Initialize the Bare Repository

Run the following command on your server.

sudo git init --bare /opt/media.git

- The `/opt/media.git` directory will store your project code history.
- `sudo` ensures you have write access to `/opt`.

---

## Step 2: Clone the Central Repository

On each developer's machine, clone the central repo:

git clone user@your-server:/opt/media.git

- Replace `user@your-server` with your actual SSH credentials.

---

## Step 3: Collaborative Workflow

Team members can now:
- Make changes in their local clones
- Commit locally
- Push changes to `/opt/media.git`:
  
- Pull updates from others:
  git pull origin main


---

### Why Use a Bare Repository?

- Prevents direct edits to central codebase; only git push/pull are allowed
- Standard for remote repos, including GitHub/GitLab
- Facilitates safe, collaborative workflows

---
