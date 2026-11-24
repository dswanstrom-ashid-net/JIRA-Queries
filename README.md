# JIRA-Queries

## Tickets moved to Ready for Dev

Run this JQL in Jira's advanced issue search to find tickets currently assigned
to fix version `v3.87` that have ever transitioned to `Ready for Dev`:

```jql
fixVersion = "v3.87" AND status CHANGED TO "Ready for Dev"
```

The search result count is the number of matching tickets. Each ticket is counted
once, even if it transitioned to that status multiple times, and it may have a
different current status. This also includes a ticket's first transition to
`Ready for Dev`; add a `FROM` status to the history clause if a particular
source status defines a return. Add a project filter if the version name is
shared by multiple projects.
