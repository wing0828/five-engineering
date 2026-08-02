# Five Engineering

Five Engineering is a portable Agent Skill for making complex AI work more reliable in Codex and Claude Code through five nested layers:

1. Prompt engineering
2. Context engineering
3. Harness engineering
4. Loop engineering
5. Graph engineering

It helps an agent turn an ambiguous request into a testable contract, gather bounded context, build verification into execution, iterate without repeating failed attempts, and coordinate independent work safely.

## Install in Codex

Ask Codex:

```text
Install the five-engineering skill from https://github.com/wing0828/five-engineering/tree/main/skills/five-engineering
```

Codex can install it from the public GitHub path using its built-in skill installer. The skill becomes available on the next turn after installation.

## Manual installation

Clone this repository, then copy `skills/five-engineering` into your Codex skills directory as `five-engineering`:

- Windows: `%USERPROFILE%\.codex\skills\five-engineering`
- macOS/Linux: `~/.codex/skills/five-engineering`

The installed directory must contain `SKILL.md` directly.

## Use

Invoke it explicitly:

```text
Use $five-engineering to plan and implement this feature with clear success criteria and verification.
```

It can also be selected automatically for complex implementation, research, automation, debugging, and multi-agent work.

## Install in Claude Code

### Plugin installation

Run these commands inside Claude Code:

```text
/plugin marketplace add wing0828/five-engineering
/plugin install five-engineering@five-engineering-marketplace
/reload-plugins
```

Invoke the plugin skill explicitly:

```text
/five-engineering:five-engineering
```

Claude can also invoke it automatically when the request matches its description.

### Personal skill installation

Alternatively, clone this repository and copy `skills/five-engineering` into your personal Claude Code skills directory:

- Windows: `%USERPROFILE%\.claude\skills\five-engineering`
- macOS/Linux: `~/.claude/skills/five-engineering`

Then invoke it without a plugin namespace:

```text
/five-engineering
```

## Repository layout

```text
.claude-plugin/
  marketplace.json
  plugin.json
skills/
  five-engineering/
    SKILL.md
    agents/
      openai.yaml
```

## License

MIT License. See [LICENSE](LICENSE).
