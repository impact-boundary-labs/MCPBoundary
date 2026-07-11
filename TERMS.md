# MCP Boundary v0.2.3 Release Terms

These terms describe the intended public release scope for the MCP Boundary
v0.2.3 local binary packages.

## What This Release Is

This release is a source-free local binary release for wrapping configured
local MCP servers through MCP Boundary on the supported packaged platforms.

Included public artifacts:

```text
mcpboundary-v0.2.3-windows-amd64.zip
mcpboundary-v0.2.3-linux-amd64.tar.gz
```

Each package includes:

- the platform executable (`mcpboundary.exe` on Windows or `mcpboundary` on Linux)
- first-run documentation
- known limitations
- license and third-party notices
- the simulated Local Email Demo example files

## What This Release Is Not

This release is not:

- a public source-code release
- a hosted service
- a production-certified gateway
- a durable audit database
- an exactly-once execution system
- a DLP layer
- a prompt-injection protection system
- a tenant-isolation product
- a guarantee that every MCP server or provider is safe

## Allowed Local Use

You may use this release locally to:

- run the platform executable (`mcpboundary` on Linux or `mcpboundary.exe` on Windows)
- try the simulated Local Email Demo
- wrap configured local MCP servers
- inspect setup, tools, policy, and activity through the localhost dashboard
- test local integrations against the documented v0.2.3 behavior

Only calls routed through MCP Boundary are covered by the Boundary path.

Private use and evaluation are free of charge. Commercial production use by
companies requires a paid license from Impact Boundary Labs.

## Provider Credentials

MCP Boundary does not require provider credentials for the included Local Email
Demo. Real provider use requires a separate downstream MCP server that the
operator can configure and run locally.

Do not paste provider secrets into MCP Boundary docs, example files, dashboard
fields, or support bundles.

## Redistribution and Resale

You may not redistribute, resell, sublicense, repackage, offer as a hosted
service, or commercially provide the runtime package to third parties without
explicit written permission from Impact Boundary Labs.

## Warranty and Production Scope

This release is provided as-is. It is intended for scoped local v0.2.3 usage.
It does not make production-grade security, hosted operation, durable audit,
semantic correctness, human-review replacement, or exactly-once execution
claims.
