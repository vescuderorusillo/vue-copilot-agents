# Git Workflow Guide

This document provides instructions on how to use the Git workflow automation tools set up in this project.

## Setup

1. Install dependencies:

```bash
npm install
```

This will automatically set up Husky Git hooks.

## Daily Git Workflow

### Creating a new feature branch

```bash
git checkout -b feature/your-feature-name
```

### Making commits

Instead of using `git commit` directly, use our interactive commit tool:

```bash
npm run commit
```

This runs Commitizen which will guide you through making a properly formatted commit message:

1. Select the type of change (feat, fix, docs, etc.)
2. Enter the scope of the change (optional)
3. Write a short description
4. Add a longer description (optional)
5. Specify breaking changes (if any)
6. Reference issues (if applicable)

### Pre-commit checks

Before each commit, the pre-commit hook will automatically:
- Run ESLint on staged files
- Fix formatting issues when possible

### Before pushing

The pre-push hook will automatically run tests before allowing a push to the remote repository.

### Pushing to remote

```bash
git push origin feature/your-feature-name
```

## Creating Pull Requests

When your feature is ready:

1. Ensure your branch is up to date with the main branch:

```bash
git checkout main
git pull
git checkout feature/your-feature-name
git rebase main
```

2. Resolve any conflicts if necessary
3. Push your changes
4. Create a pull request on GitHub/GitLab/etc.

## Tips for a Clean Git History

- Use `git rebase -i main` to clean up your commits before creating a pull request
- When merging PRs, consider using squash merges to keep the main branch history clean

## Useful Git Commands

```bash
# View status of your working directory
git status

# View commit history
git log --oneline --graph

# Stash changes temporarily
git stash
git stash pop

# Amend the most recent commit (before pushing)
git commit --amend

# Force push with lease (safer than force push)
git push --force-with-lease
```