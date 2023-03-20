# Automerge PRs

> ***Note***
> It's not the same as [Automatically Merging a PR](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/incorporating-changes-from-a-pull-request/automatically-merging-a-pull-request)

This is an example about using GitHub CLI, Projects and Actions to review PRs with certain criteria and automatically merge them given a `Release date` field.

## How this works?

PR should be part of a GitHub Project and fill the `Release date`. Of course, this can be used with scheduled workflows

```yaml
on:
  schedule:
    - cron: 0 13 * * 1-5
```

Three env vars should be configured: `GH_TOKEN`, `PROJECT_ID`, `ORG_ID`
