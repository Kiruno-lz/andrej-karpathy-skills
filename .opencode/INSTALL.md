# Installing Karpathy Guidelines for OpenCode

## Prerequisites

- [OpenCode.ai](https://opencode.ai) installed

## Installation

Add karpathy-guidelines to the `plugin` array in your `opencode.json` (global or project-level):

```json
{
  "plugin": ["karpathy-guidelines@git+https://github.com/forrestchang/andrej-karpathy-skills.git"]
}
```

Restart OpenCode. That's it — the plugin auto-installs and registers the skill.

Verify by asking: "use skill tool to list skills"

## Usage

Use OpenCode's native `skill` tool:

```
use skill tool to list skills
use skill tool to load karpathy-guidelines
```

The guidelines will also be automatically injected into every session via bootstrap.

## What It Does

This plugin:

1. **Registers the skill** - Makes `karpathy-guidelines` available via the skill tool
2. **Injects bootstrap** - Adds behavioral guidelines to every session automatically

## The Four Principles

- **Think Before Coding** - Don't assume, surface tradeoffs, ask when unclear
- **Simplicity First** - Minimum code that solves the problem, nothing speculative
- **Surgical Changes** - Touch only what you must, clean up only your own mess
- **Goal-Driven Execution** - Define success criteria, loop until verified

## Updating

Karpathy Guidelines updates automatically when you restart OpenCode (if using Git URL).

To pin a specific version:

```json
{
  "plugin": ["karpathy-guidelines@git+https://github.com/forrestchang/andrej-karpathy-skills.git#v1.0.0"]
}
```

## Tool Mapping

When skills reference Claude Code tools:

- `TodoWrite` → `todowrite`
- `Task` with subagents → `@mention` syntax
- `Skill` tool → OpenCode's native `skill` tool
- File operations → your native tools

## Getting Help

- Report issues: <https://github.com/forrestchang/andrej-karpathy-skills/issues>
- Original project: <https://github.com/forrestchang/andrej-karpathy-skills>

