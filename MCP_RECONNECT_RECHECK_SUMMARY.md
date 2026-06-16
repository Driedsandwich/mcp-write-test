# MCP Reconnect Recheck Summary

Date: 2026-06-16

## Improved

- PR creation now works.
- PR #1 was created, read, commented on, updated, and closed without merge.
- Repository creation now reaches GitHub API but returns 403.

## Still limited

- Notifications: 403
- Repository notification subscription: 403
- Projects: 403
- Code scanning alerts: 403
- Secret scanning alerts: 403
- Dependabot alerts: disabled or permission-limited
- Copilot Spaces: not found
- Issue creation was not retried because the previous approval-path response said not to call that path again.

## Cleanup

- PR #1 is closed.
- Branch mcp/reconnect-pr-check remains.
