# Taumatix

Small, well-tested open-source libraries for Go and Swift. Each one is checked against the
upstream it was built for, and says which version that is in an `UPSTREAM.md` at its root.
Notes and write-ups: [taumatix.github.io](https://taumatix.github.io).

## Libraries

| Library | What it does | Install |
|---|---|---|
| [claude-agent-sdk-go](https://github.com/taumatix/claude-agent-sdk-go) | Unofficial Go SDK for the Claude Agent API, ported from the official Python SDK | `go get github.com/taumatix/claude-agent-sdk-go` |
| [natsmqtt5](https://github.com/taumatix/natsmqtt5) | MQTT v5 broker that uses the NATS server you already run as its messaging core | `go get github.com/taumatix/natsmqtt5` |
| [claude-mods-go](https://github.com/taumatix/claude-mods-go) | Write Claude Code mods in Go, with the `modgo` tool to package them | `go get github.com/taumatix/claude-mods-go` |
| [anthropic-swift](https://github.com/taumatix/anthropic-swift) | Swift client for the Anthropic Claude API | Swift Package Manager |
| [iterm2-go](https://github.com/taumatix/iterm2-go) | Go client for the iTerm2 API: windows, tabs, sessions, notifications | `go get github.com/taumatix/iterm2-go` |
| [iterm2-claude-bridge](https://github.com/taumatix/iterm2-claude-bridge) | Show Claude Code sessions on remote hosts in iTerm2 and attach to their tmux session | see its README |

## How these are maintained

- Public APIs change additively. A breaking change means a major version, a `MIGRATION.md` and a
  deprecation period.
- Every feature has an end-to-end test against the real interface, and CI must be green before merge.
- Releases follow a fortnightly schedule, with exceptions for security fixes.
- Most of the day-to-day work is done by an AI agent. A human owns the repositories and sets the direction.

## Licensing

Apache-2.0, except `iterm2-go` and `iterm2-claude-bridge`, which are GPL-2.0-or-later because
`iterm2-go` includes iTerm2's own GPL-2.0 protocol definition.
