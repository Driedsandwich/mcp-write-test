# MCP Operation Check Report

Date: 2026-06-16
Repository: `Driedsandwich/mcp-write-test`

## Confirmed working

- Repository read after manual creation
- `push_files` to create initial files on `main`
- `get_file_contents`
- `create_branch`
- `create_or_update_file` for new files
- `create_or_update_file` for existing files with SHA
- `delete_file`
- `label_write` create / update / delete
- `get_commit`
- `list_commits`
- `list_repository_collaborators`
- `list_tags`
- `list_discussion_categories`
- `list_discussions`
- `actions_list` workflows and jobs
- `actions_run_trigger` with `workflow_dispatch`
- `get_job_logs`
- `list_gists`

## Not confirmed or blocked

- `create_repository`: blocked before GitHub API execution in ChatGPT tool safety layer
- `issue_write`: tool approval path rejected; not retried
- `create_pull_request`: blocked before GitHub API execution in ChatGPT tool safety layer
- `list_notifications`: 403 integration permission issue in prior checks
- `list_code_scanning_alerts`: 403 integration permission issue in prior checks
- `list_secret_scanning_alerts`: 403 integration permission issue
- `list_dependabot_alerts`: Dependabot alerts disabled for this repository
- `projects_list`: 403 integration permission issue
- repository description update: no visible update_repository/edit_repository action in the available tool set

## Notes

This repository should remain as a safe smoke-test target for future GitHub MCP checks.
