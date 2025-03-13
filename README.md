# GitHub Organization Inactive User Removal

This repository contains an automated workflow to identify and optionally remove inactive users from a GitHub organization.

## Purpose

Maintaining an up-to-date roster of active users in a GitHub organization is crucial for security, license management, and overall organizational efficiency. This automation helps by:

1. Identifying users who have been inactive for a specified period.
2. Generating a report of inactive users.
3. Optionally removing inactive users from the organization.

## How It Works

The automation uses GitHub Actions and the [inactive-users-action](https://github.com/peter-murray/inactive-users-action) to analyze user activity within the organization. It runs on a schedule and can also be triggered manually.

## When determining if a user is active or inactive in GitHub, the following activities are considered:

- Repository interactions: Creating, pushing to, or deleting repositories. 
- Issue and pull request management: Creating, commenting on, closing, or reopening issues and pull requests. 
- Comments and reviews: Leaving comments on commits or pull requests. 
- Repository visibility changes: Changing a repository's visibility (public, private). 
- User interactions: Watching or starring repositories.

### Reading repositories is not counted as an activity since the GitHub Enterprise plan requires the Audit log API. 


## References
1. https://github.com/peter-murray/inactive-users-action/blob/main/README.md about inactive users action using Github Action.

2. https://github.com/oss-tooling/user-inactivity  about automation which helps monitor and remove inactive members from a Github organization.

3. https://docs.github.com/en/enterprise-cloud@latest/admin/monitoring-activity-in-your-enterprise/reviewing-audit-logs-for-your-enterprise/using-the-audit-log-api-for-your-enterprise about GitHub Enterprise plan to get audit API.

