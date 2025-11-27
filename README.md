# Claude Commands

A collection of custom slash commands for [Claude Code](https://docs.anthropic.com/en/docs/claude-code).

## Installation

Copy commands to your Claude Code commands directory:

- **Global** (all projects): `~/.claude/commands/`
- **Project-specific**: `.claude/commands/`

```bash
# Example: Install hard-clear globally
cp commands/hard-clear.md ~/.claude/commands/
```

## Commands

### hard-clear

Permanently delete the current session file, making it unrecoverable even with `/resume`.

**Usage:**

Delete current session:
```
/hard-clear
```

Delete a different session:
```
/resume          # Select the session you want to delete
/hard-clear      # Delete it
```

---

## 日本語 / Japanese

### hard-clear

現在のセッションファイルを完全削除し、`/resume` でも復元できなくします。

**使い方:**

現在のセッションを削除:
```
/hard-clear
```

別のセッションを削除:
```
/resume          # 削除したいセッションを選択
/hard-clear      # 削除実行
```

## License

MIT
