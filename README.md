# Morten's UI principles

[UI rules](principles.md) for agents designing, building, or reviewing interfaces.

## Install

Requires Node.js 22.20 or later. Install for Codex across projects:

```sh
npx skills add mortenjust/mortens-ui-principles --skill mortens-ui-principles --agent codex --global --yes
```

For one project, run the command from its folder without `--global`.

Use `$mortens-ui-principles` when working on UI. The skill tells the agent to fetch the current principles each time and report any fetch failure.

## Update the rules

Edit [principles.md](principles.md) on `main`. Rule changes need no reinstall. Changes to the [skill loader](SKILL.md) do.

Keep project-specific rules in `AGENTS.md` or a file it links to. Leave the installed loader unchanged.
