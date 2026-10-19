# Gourav's Skills

Reusable agent skills for how I approach software engineering: understand the product, verify the evidence, ask about meaningful decisions, implement simply, and finish the agreed work.

These skills express working preferences rather than a fixed technology stack. Your current instructions, project requirements, and explicit decisions take precedence.

## Skills

| Skill | Purpose |
| --- | --- |
| [gourav-engineering](skills/gourav-engineering/SKILL.md) | Product understanding, official documentation, meaningful decision questions, simple implementations, precise scope, and evidence-based completion. |

## Install

Use the [skills CLI](https://skills.sh/docs/cli) and select the agents you want to install into:

```sh
npx skills@latest add Gourav224/skills --skill gourav-engineering
```

For a user-level installation across projects:

```sh
npx skills@latest add Gourav224/skills --skill gourav-engineering --global
```

To select Claude Code and Codex explicitly:

```sh
npx skills@latest add Gourav224/skills --skill gourav-engineering --global --agent claude-code codex
```

List the skills before installing:

```sh
npx skills@latest add Gourav224/skills --list
```

The CLI supports multiple coding agents. Availability and invocation depend on the host agent; custom profiles may need their own skill location. Alternatively, copy `skills/gourav-engineering/` into your agent's documented skills directory.

## Use

Ask your agent:

> Use gourav-engineering for this task. Understand the problem, bring meaningful decisions to me, and carry the agreed approach through verification.

In Codex, you can invoke it as `$gourav-engineering`. In Claude Code, use `/gourav-engineering`.

Give the agent the task-specific boundaries alongside the skill:

```text
Goal: [observable user outcome]
Scope: [affected workflow or module]
Preserve: [behavior and unrelated work that must stay intact]
Mode: [investigate only / implement]
Compatibility: [existing consumers and data to preserve]
Validation: [checks and external actions permitted]
Delivery: [report / local commit / push to named branch / deployment]
```

## Working principles

- Understand the actual product and trace the cause before choosing a fix.
- Read relevant official documentation for the installed versions; verify assumptions.
- Separate established decisions, verified facts, and unresolved choices.
- Ask about consequential tradeoffs while handling routine details independently.
- Reuse existing flows, components, contracts, and provider capabilities.
- Complete the workflow without unnecessary layers, duplicate logic, or unrelated changes.
- Follow exact scope and references, preserve concurrent work, and continue after agreement.
- Verify what is authorized and distinguish static checks from runtime evidence.

Installing a skill makes it available to an agent; it does not guarantee activation on every message or grant permission to run tools, change data, push code, or deploy.

## Repository layout

```text
skills/
  gourav-engineering/
    SKILL.md
    agents/
      openai.yaml
```

Each skill is self-contained and uses the [Agent Skills format](https://agentskills.io/specification). New skills should get their own folder under `skills/`.

## Inspiration

The collection layout was inspired by [Matt Pocock's skills repository](https://github.com/mattpocock/skills). The skill instructions here were developed from my own engineering and collaboration preferences.

## License

[MIT](LICENSE).
