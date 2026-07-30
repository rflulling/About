# GitHub Repository Security Settings

This document provides instructions for configuring high-security settings for this repository.

## Required Manual Configuration Steps

The following settings must be configured through the GitHub repository settings UI:

### 1. Disable Forks

Navigate to: **Settings → General → Features**

- [ ] Uncheck "Allow forking"

### 2. Disable Downloads

Navigate to: **Settings → General → Features**

- [ ] Uncheck "Releases" (prevents creating downloadable releases)
- [ ] Consider disabling "Packages" if enabled

### 3. Branch Protection Rules

Navigate to: **Settings → Branches → Branch protection rules**

Create a rule for the `main` branch with the following settings:

- [ ] Require pull request reviews before merging
- [ ] Dismiss stale pull request approvals when new commits are pushed
- [ ] Require status checks to pass before merging
- [ ] Require branches to be up to date before merging
- [ ] Require conversation resolution before merging
- [ ] Do not allow bypassing the above settings

### 4. General Security Settings

Navigate to: **Settings → Code security and analysis**

- [ ] Enable "Private vulnerability reporting" if available
- [ ] Enable "Dependency graph"
- [ ] Enable "Dependabot alerts" if applicable

### 5. Access Control

Navigate to: **Settings → Collaborators and teams**

- [ ] Review and minimize collaborator access
- [ ] Ensure only authorized users have write access

## Verification

After applying these settings, verify:

1. Visitors cannot fork the repository
2. There are no downloadable releases or archives available
3. Direct pushes to the main branch are blocked
4. Only authorized collaborators can make changes

## Notes

- These settings protect the integrity of your profile README
- The repository remains publicly viewable but contributions are restricted
- Changes can only be made by authorized collaborators through pull requests
