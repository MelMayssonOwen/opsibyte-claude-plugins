# Opsibyte brand guides for Claude Code

Four installable plugins: Toolfound, TimeToPost, and Clef combine a skill with an existing remote HTTP MCP server; Prayer in Hand is skills-only. These packages contain no hooks or installation scripts.

This is a public community marketplace source. Its publication does not claim inclusion in or approval by any official Claude directory or marketplace.

## Install from GitHub

```sh
claude plugin marketplace add MelMayssonOwen/opsibyte-claude-plugins
claude plugin install toolfound-guide@opsibyte-brand-guides
claude plugin install timetopost-planner@opsibyte-brand-guides
claude plugin install clef-practice@opsibyte-brand-guides
claude plugin install prayer-in-hand-reflection@opsibyte-brand-guides
```

## Validate and install locally

From the root of this repository:

```sh
claude plugin validate .
claude plugin marketplace add .
claude plugin install toolfound-guide@opsibyte-brand-guides
claude plugin install timetopost-planner@opsibyte-brand-guides
claude plugin install clef-practice@opsibyte-brand-guides
claude plugin install prayer-in-hand-reflection@opsibyte-brand-guides
claude plugin list
```

The marketplace and each plugin pass Claude Code manifest validation. Run the validation command above before installing.

For a temporary development test without installing, use `claude --plugin-dir ./plugins/clef-practice` (substitute any package path), then invoke its namespaced skill, such as `/clef-practice:five-minute-note-practice`.

## MCP authentication and transport

All three included MCP connections are remote HTTPS/HTTP transports, not local `stdio` processes. Clef is a public, unauthenticated Streamable HTTP endpoint. Claude Code handles supported remote OAuth for services that require it; follow its browser prompt and never put a token in these package files. TimeToPost can alternatively be run as a user-configured local stdio server using its documented npm package and runtime environment variables, but this marketplace intentionally uses the credential-free remote configuration.

After installation, run `claude mcp list` and `/mcp` in Claude Code to inspect status or authenticate. For TimeToPost, first state the workspace the customer explicitly intends to use, then run `whoami` before any other lookup. Continue only on a clear match; stop on mismatch or ambiguity. Legitimately authorized agency workspaces are allowed when explicitly selected by the customer. These packages expose skills that instruct Claude to use only named read-only tools. A skill's `allowed-tools` list grants temporary preapproval for the invocation turn; it is not a restrictive allowlist, does not remove other tools from the callable pool, and does not enforce read-only access. The workflow instructions provide the read-only rule, so never use or authorize mutations for these workflows even if a remote server exposes write tools.

Toolfound supports public directory research and launch review only. TimeToPost supports read-only content planning only: no drafting, scheduling, publishing, sending, uploads, approvals, or account changes. Clef allows only its four verified read-only tools for guide lookup, chord transposition, piano chord spelling, and ASCII guitar-tab note mapping; it does not support Guitar Pro files, audio, or rhythm inference. Prayer in Hand includes no MCP endpoint because its MCP status is unknown, not proven absent. Package presence is not endorsement, directory listing, marketplace approval, or publication by any platform.

Useful brand links: https://clefdrills.com and https://prayerinhand.com.
