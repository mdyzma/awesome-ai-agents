# GitHub MCP Server for Codex (Single Repo: mdyzma/awesome-ai-agents)

This file configures the official GitHub MCP Server in Codex CLI to read
and write **only** the `mdyzma/awesome-ai-agents` repository, including
Issues, PRs, and Projects (project boards).

## 1) Create a GitHub Token (Least Privilege)

Use a fine-grained PAT and limit access to just this repo.

UI steps (GitHub):

1. Open GitHub in your browser.
2. Go to Settings -> Developer settings -> Personal access tokens ->
   Fine-grained tokens.
3. Click "Generate new token".
4. Token name: `codex-mcp-awesome-ai-agents`.
5. Expiration: choose a short/medium lifetime.
6. Resource owner: `mdyzma`.
7. Repository access: select "Only select repositories" ->
   check `mdyzma/awesome-ai-agents`.
8. Permissions: set the following:
   - `Contents: Read and write`
   - `Metadata: Read`
   - `Issues: Read and write`
   - `Pull requests: Read and write`
   - `Projects: Read and write`
9. Click "Generate token" and copy it once.

Notes:

- Projects permission is required to move/close items on project boards.
- If you prefer classic PATs, you must use `repo` scope and it will apply
  to *all* repos you can access. Fine-grained PAT is recommended to keep
  access scoped.

## 2) Store the Token Securely (Persistent)

Use a persistent environment variable and do not commit it.

Windows PowerShell (persistent, user scope):

```powershell
[Environment]::SetEnvironmentVariable(
  "GITHUB_PAT_TOKEN", "<YOUR_TOKEN>", "User"
)
```

macOS zsh (persistent):

```sh
echo 'export GITHUB_PAT_TOKEN="<YOUR_TOKEN>"' >> ~/.zshrc
source ~/.zshrc
```

## 3) Configure Codex

The official GitHub MCP Server is hosted at:

- `https://api.githubcopilot.com/mcp/`

Add the server to Codex config at `~/.codex/config.toml`:

```toml
[mcp_servers.github]
url = "https://api.githubcopilot.com/mcp/"
# Replace with your real PAT env var name.
# Keep the token in your environment, not in the file.
bearer_token_env_var = "GITHUB_PAT_TOKEN"
```

You can also add the server via CLI:

```sh
codex mcp add github --url https://api.githubcopilot.com/mcp/
```

## 4) Verify

In Codex:

- Run `/mcp` in the TUI or use the MCP panel in the IDE.
- Ask: "List repos I can access" and verify only
  `mdyzma/awesome-ai-agents` is writable.
- Ask: "List project boards" and verify you can move items.

If you see permission errors, add only the missing permission in the
fine-grained PAT and retry.

## Permission Troubleshooting

If Codex (via the MCP server) fails an action, the error usually
indicates a missing permission. Common mappings:

- Can't read repo files or branch contents: add `Contents: Read`.
- Can't push commits / update files: add `Contents: Read and write`.
- Can't view issues: add `Issues: Read`.
- Can't create or close issues: add `Issues: Read and write`.
- Can't view PRs: add `Pull requests: Read`.
- Can't open or update PRs: add `Pull requests: Read and write`.
- Can't list or move project board items: add `Projects: Read` or
  `Projects: Read and write`.
- "Resource not accessible by integration": make sure the PAT is scoped
  to `mdyzma/awesome-ai-agents` and you selected the correct resource
  owner.
