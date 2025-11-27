Permanently delete the current session file, making it unrecoverable even with `/resume`.

## Steps

1. Identify the session directory from the current working directory
   - Path conversion example: `/home/user/myproject` → `-home-user-myproject`
   - Session directory: `~/.claude/projects/{converted-path}/`

2. Find the most recently updated UUID-format `.jsonl` file
   - Sort by modification time using `ls -t`
   - Target files with UUID format (hyphen-separated alphanumerics, e.g., `b6cecae3-31f5-4111-a653-ea68f958a3f4.jsonl`)
   - Exclude `agent-*` files (used for subagents, no need to delete)

3. **Confirm with user**: Use AskUserQuestion tool to ask "Are you sure you want to delete this?"
   - Show the filename for confirmation

4. After confirmation, execute `rm` command via Bash tool to delete

5. Report deletion complete

## Notes
- After executing this command, the current session cannot be recovered
- Cannot be restored with `/resume` command
- A confirmation dialog is always displayed before deletion
