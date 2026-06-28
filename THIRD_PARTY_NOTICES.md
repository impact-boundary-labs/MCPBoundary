# Third-Party Notices

This file covers the MCP Boundary v0.1.2 Windows and Linux release packages:

```text
mcpboundary-v0.1.2-windows-amd64.zip
mcpboundary-v0.1.2-linux-amd64.tar.gz
```

## Scope

Covered release components:

- the platform executable (`mcpboundary.exe` on Windows or `mcpboundary` on Linux)
- release documentation included in the package
- the optional `examples/email-demo` learning files

The package does not include source code for MCP Boundary or Impact Boundary
Core.

## Go Modules Observed During Release Preparation

`go list -m all` in the source tree reported the following non-standard-library
modules relevant to the built binary:

| Module | Version | Role | License | Bundled license text |
| --- | --- | --- | --- | --- |
| `adapter-host` | main module | MCP Boundary source component used to build the release binaries | Impact Boundary Labs component. | n/a |
| `impact-boundary-core` | `v0.0.0` | Compiled-in Impact Boundary Core component | Impact Boundary Labs component; source not included in the release packages. | n/a |
| `github.com/zalando/go-keyring` | `v0.2.8` | OS keyring integration | MIT | `third-party-licenses/github.com-zalando-go-keyring-LICENSE.txt` |
| `github.com/danieljoos/wincred` | `v1.2.3` | Windows credential backend used by keyring integration | MIT | `third-party-licenses/github.com-danieljoos-wincred-LICENSE.txt` |
| `github.com/godbus/dbus/v5` | `v5.2.2` | Cross-platform keyring dependency | BSD-2-Clause | `third-party-licenses/github.com-godbus-dbus-LICENSE.txt` |
| `golang.org/x/sys` | `v0.27.0` | Go system-call support package | BSD-3-Clause | `third-party-licenses/golang.org-x-sys-LICENSE.txt` |

The full, unmodified upstream license texts for the third-party dependencies
above are included in the release package under `third-party-licenses/`. The MIT
and BSD licenses require their copyright notice and license text to be
reproduced in binary distributions; those bundled texts satisfy that
requirement.

## Go Standard Library and Toolchain

The binary is built with the Go toolchain and includes Go standard library code.
Go is distributed by Google under a BSD-style license. Review the Go
distribution license for complete terms if your release process requires
toolchain attribution.

## Local Email Demo

The included Local Email Demo is simulated. It does not include a provider SDK,
OAuth artifact, token, credential, mailbox export, or real email data.

## Notes

- This notices file does not invent licenses for Impact Boundary Labs
  components.
- If future releases add bundled tools, generated assets, containers, provider
  SDKs, or additional dependencies, this file must be regenerated and reviewed.
