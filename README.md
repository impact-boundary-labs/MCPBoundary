# MCP Boundary

A local proxy that wraps your MCP servers and checks each tool call against your policy and the current state before any server tool is called. When it blocks, the agent gets back a reason it can act on.

**Website:** https://mcpboundary.com · **Docs:** https://mcpboundary.com/docs/mcp-boundary

## What it does

- **Wrap an existing local MCP server** — your agent keeps the same tools, every call passes the boundary first.
- **Choose which tools the agent sees** — expose, hide, or keep dashboard-only.
- **Allow, block, or hold for review** — with a structured reason the agent can act on.
- **Restrict specific arguments, not whole tools** — e.g. allow only certain recipients or IDs.
- **Limit response sizes and timeouts** — and throttle repeated calls to contain runaway loops.
- **Bind writes to observed state** — don't run a write if the world changed since the read.
- **Inspect every call, decision, reason, and outcome** in a local dashboard.

## How it works

MCP Boundary sits between your MCP client and your local MCP servers. Your agent connects to MCP Boundary as a server entry; MCP Boundary checks each tool call against your policy and the current state, then forwards only admitted calls to the real server. When it blocks, the agent gets back a reason it can act on — re-check state, narrow scope, or stop retrying.

## Download

Windows and Linux builds with SHA-256 checksums (current release **v0.2.3**):
→ https://mcpboundary.com

Quick start from an extracted package — Windows: `.\mcpboundary.exe quickstart email` · Linux: `./mcpboundary quickstart email`

## Docs

- Getting started, policy examples, tested servers — https://mcpboundary.com/docs/mcp-boundary
- How it works — https://mcpboundary.com/how-it-works
- MCP Tool Rules (writing policies) — https://mcpboundary.com/mcp-tool-rules

## Scope

MCP Boundary works best with local command-based stdio MCP servers. Only calls routed through MCP Boundary are covered. It is **not** an enterprise security gateway, a DLP system, a prompt-injection detector, or a replacement for code review, database permissions, or email approval processes.

## License

MCP Boundary is free to download and use, distributed under its own license and terms — see `LICENSE.md` and `TERMS.md` in the release package. All rights reserved.

---

Built by [Impact Boundary Labs](https://impactboundarylabs.com).
