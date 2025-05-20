---
description: This workflow is intended to quickly raise a pull request on a given changeset or patch.  This uses sensible default values for PR information with the option to override certain values if mentioned in the prompt.
---

# You must raise a pull request with team best-practiced defaults for the values described below

Examine the prompt for any overrides to the values below. You must also
identify if a patch is present in the prompt, if so the user should have
recommended a name for the feature branch. If not, ask the user for a short
description of the changes and use

You must always adhere to the branch naming format of:
feature/WR-XXXX-<pull-request-title-hyphenated>

Use the Github MCP to create this branch. Apply the patch changes to this
branch. Add, commit, and push the changes to this newly created branch. For
your commit message, generate a detaile description of the changes based on
the list_commits in this feature branch. You must always use conventional commit
format.

Use the Github MCP to raise the pull request with the following information -

owner: Retail-Success
repo: the current repository's name
head: the name of the feature branch
base: develop
title: <name of the feature branch>
body: Generate draft based on the list_commits in this feature branch.
Ensure your changes are committed and pushed to your feature branch on GitHub.
Identify the following information:
Repository owner (username or organization)
Repository name
Name of the branch with your changes (feature branch)
Name of the base branch to merge into the `develop`
Pull request title and description
Use the GitHub MCP to create the pull request:
Call the create_pull_request action with:

assignee: current user found in the list of commits

Confirm the pull request was created successfully by checking the returned PR number or URL.
(Optional) Share the pull request link with reviewers or stakeholders.
