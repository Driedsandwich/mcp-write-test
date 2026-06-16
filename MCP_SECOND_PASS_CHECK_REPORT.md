# MCP Second Pass Check Report

Date: 2026-06-16
Repository: `Driedsandwich/mcp-write-test`

## Additional confirmed working

- Recursive repository tree read
- Code search scoped to repository
- Commit search scoped to repository
- GitHub Support Docs search
- Global Security Advisory listing
- User search
- Organization search
- Team listing call completed with `null` for this account context
- Starred repositories listing
- Actions workflow rerun request
- Actions job listing with all attempts

## Additional blocked or unavailable

- Repository notification subscription watch: 403 integration permission issue
- Copilot Spaces list: not found / no accessible spaces
- Projects list: 403 integration permission issue
- Release listing showed intermittent ChatGPT tool safety blocking in prior check

## Notes

- `issue_write` was not retried after the previous approval-path rejection.
- Destructive Actions operations such as canceling runs or deleting logs were intentionally not tested.
- Gist creation was intentionally not tested because no delete-gist action is visible in the available action list, so cleanup would be incomplete.
- Star/unstar was not tested because it would modify public account-facing state and is not required for normal repository maintenance.
- Notification and project related failures appear to be integration-permission limitations rather than repository-specific content errors.
