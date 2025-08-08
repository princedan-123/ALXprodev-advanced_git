
# Git-Flows Tutorial Project

## Overview
Git-Flow is a branching model for Git proposed by Vincent Driessen that helps developers manage features, releases, and hotfixes in a consistent and scalable way. It introduces well-defined roles for branches and helps teams coordinate code changes more effectively — especially in large-scale projects where multiple developers work on different parts of the codebase simultaneously.

In this project, we practice **Git-Flow** commands and best practices by:
- Initializing Git-Flow with default settings.
- Creating and managing feature, release, and hotfix branches.
- Using Git hooks for automation.

---

## Branch Types in Git-Flow

| Branch Type         | Purpose |
|---------------------|---------|
| **main** (or master) | Holds production-ready code only. |
| **develop**          | Ongoing development branch where features are integrated. |
| **feature/***        | For developing new features. Branched from `develop`. |
| **release/***        | For preparing a production release. Branched from `develop`. |
| **hotfix/***         | For urgent fixes to production code. Branched from `main`. |

---

## Learning Objectives
By completing this project, you will be able to:
- Understand the purpose and structure of Git-Flow.
- Identify the different branch types and their roles.
- Apply Git-Flow in real-world collaborative projects.
- Manage features, hotfixes, and release cycles using Git best practices.

---

## Best Practices in Git-Flow

| Best Practice | Description |
|--------------|-------------|
| **Start with `develop`** | Always branch off from `develop` for new features. |
| **Feature isolation** | Keep each feature in its own branch to reduce merge conflicts. |
| **Merge via PRs** | Use pull requests for merges to ensure code review. |
| **Keep `main` clean** | Only production-ready code should be in `main`. |
| **Tag releases** | Use Git tags on `main` to mark official release points. |
| **Use hotfix/** for urgent bugs | Apply emergency fixes directly to `main` via `hotfix/` branches. |
| **Document workflow** | Keep your Git-Flow documented in the README or project wiki. |

---

## Common Git-Flow Commands

```bash
# Initialize Git-Flow
git flow init -d

# Start a new feature
git flow feature start <name>

# Finish a feature and merge into develop
git flow feature finish <name>

# Start a release
git flow release start <x.x.x>

# Finish a release, merge into main and develop
git flow release finish <x.x.x>

# Start a hotfix
git flow hotfix start <x.x.x>

# Finish a hotfix, merge into main and develop
git flow hotfix finish <x.x.x>

