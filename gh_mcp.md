# GitHub MCP Server for Codex (Read-All + Write-Own)

This file configures the official GitHub MCP Server in Codex CLI and explains how to achieve:
- Read access to all repositories you can access
- Write access only to repos owned by `mdyzma`

There is no single "official" GitHub MCP server built into Codex. You choose the server. The official server is GitHub's `github/github-mcp-server`.

Remote server URL (hosted by GitHub):
- `https://api.githubcopilot.com/mcp/`

## Key Constraint (Important)

A single GitHub token cannot grant "read all repos" AND "write only to my repos" at the same time.

Why:
- Fine-grained PATs are scoped to a single resource owner (one user or one org).
- Classic PATs grant access to *all* repos you can access, and write permissions apply broadly.

Therefore, use two tokens and register two MCP servers in Codex:
- `github_read`: read-only token (broad read access)
- `github_write_mdyzma`: write token for `mdyzma`-owned repos only

Then, use the read-only server for general browsing and switch to the write server only when you need to create issues, PRs, or push changes.

## Step 1: Create Tokens

Token A (Read-only, broad):
- Use a fine-grained PAT.
- Resource owner: choose the user/org you want to read (start with `mdyzma`).
- Repository access: choose the minimal set that covers your needs.
- Permissions: start with `Contents: Read` and `Metadata: Read`, add more only if a tool fails.

Token B (Write for `mdyzma` only):
- Use a fine-grained PAT.
- Resource owner: `mdyzma`.
- Repository access: all `mdyzma` repos (or select only the ones you need).
- Permissions: `Contents: Read and write`, `Metadata: Read`, plus other write scopes only if needed (Issues/PRs/Workflows/Gists, etc).

Notes:
- If you need read access to org repos and the org blocks fine-grained PATs, you may need org approval or a classic PAT (which is broader).
- Classic PATs are less restrictive and apply to all repos you can access.

## Step 2: Store Tokens in Environment Variables

Set these environment variables (do NOT put the token in git):
- `GITHUB_PAT_READ`
- `GITHUB_PAT_WRITE_MDYZMA`

## Step 3: Register Both MCP Servers in Codex

Option A: CLI
```sh
codex mcp add github_read --url https://api.githubcopilot.com/mcp/
codex mcp add github_write_mdyzma --url https://api.githubcopilot.com/mcp/
```

Then map tokens in `~/.codex/config.toml`:
```toml
[mcp_servers.github_read]
url = "https://api.githubcopilot.com/mcp/"
bearer_token_env_var = "GITHUB_PAT_READ"

[mcp_servers.github_write_mdyzma]
url = "https://api.githubcopilot.com/mcp/"
bearer_token_env_var = "GITHUB_PAT_WRITE_MDYZMA"
```

Option B: Direct config only (same TOML as above).

## Step 4: Verify

In Codex:
```sh
codex mcp list
```

Then test:
- Use the read server to list repos
- Use the write server to create an issue in `mdyzma/<repo>`

If you get permission errors:
- Add only the missing permission (least-privilege)
- Ensure the correct server is selected for the action

## If You Want a Single Server Instead

Use one classic PAT with `repo` scope. This gives read/write access to all repos you can access. It does NOT enforce "write only my repos".
