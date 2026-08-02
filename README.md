# Five Engineering

Five Engineering is a portable Agent Skill for making complex AI work more reliable in Codex and Claude Code through five nested layers:

1. Prompt engineering
2. Context engineering
3. Harness engineering
4. Loop engineering
5. Graph engineering

It helps an agent turn an ambiguous request into a testable contract, gather bounded context, build verification into execution, iterate without repeating failed attempts, and coordinate independent work safely.

## What you get

- **Clear outcomes before execution** - turn vague requests into observable success criteria.
- **Less context noise** - gather only the files, decisions, constraints, and evidence needed for the next step.
- **Verification built into the work** - define how every meaningful change will be checked before implementation begins.
- **Smarter iteration** - avoid repeating unchanged failures and stop with precise evidence when blocked.
- **Safer parallel work** - give independent branches explicit ownership, dependencies, merge points, and review gates.
- **One workflow across tools** - use the same five-layer method in Codex and Claude Code.

Five Engineering does not replace the agent's tools or judgment. It provides a reusable operating method that makes complex AI work easier to inspect, verify, and coordinate.

## Who it is for

- Developers using AI for implementation, debugging, refactoring, or migration work
- Researchers who need source discipline and explicit evidence
- Automation builders running iterative or long-running tasks
- Teams coordinating multiple agents or independent workstreams
- Anyone who wants more than a one-shot answer from an AI coding agent

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

## Share

Ready-to-post Korean launch copy is available in [PROMOTION_KO.md](PROMOTION_KO.md).
