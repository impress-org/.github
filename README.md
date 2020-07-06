# Impress.org Default GitHub Files

This repository contains default files used to standardize GitHub issues and pull requests throughout the organization.

## How It Works

The `.github` directory in this project will be used by any repository in `impress-org` that does _not_ have a `.github` directory in its own project root.

For more information, see GitHub documentation for [Creating a repository for default files](https://docs.github.com/en/github/building-a-strong-community/creating-a-default-community-health-file#creating-a-repository-for-default-files).

## What's Included

### Issue Templates

The following issue templates are provided with unique fields catered to the task at hand:

| Template       | Description                                           |
| -------------- | ----------------------------------------------------- |
| Epic 🚩        | A theme of work should be broken down into subtasks   |
| Bug 🐛         | Broken functionality should be fixed                  |
| Chore 🧹       | A general non-user-facing need should be addressed    |
| Enhancement ✨ | Existing user-facing functionality should be improved |
| Integration 🔌 | An integration should be developed or improved        |
| New Feature 💡 | New user-facing functionality should be added         |

### Pull Request Template

A pull request template is included to guide developers through the steps necessary to present their code for review.

### Labels

A `labels.json` file is included to streamline synchronization of GitHub labels across multiple repositories.

### How to Synchronize Labels

1. Install [github-label-sync](https://github.com/Financial-Times/github-label-sync#command-line-interface)

```
npm install -g github-label-sync
```

2. Generate a [GitHub personal access token](https://github.com/settings/tokens). Be sure to allow the "repo" scope.

3. Perform a dry run to safely preview the result of synchronizing labels in the next step.

```
github-label-sync --access-token xxxxxx --dry-run impress-org/[repository-name]
```

4. Synchronize labels. This command will replace all labels in the designated repository with the labels defined in `labels.json`.

```
github-label-sync --access-token xxxxxx impress-org/[repository-name]
```
