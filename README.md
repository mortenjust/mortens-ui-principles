# Morten's UI principles

[UI rules](principles.md) for agents designing, building, or reviewing interfaces.

## Install

Requires Node.js 22.20 or later.

```sh
npx skills add mortenjust/mortens-ui-principles
```

Run this in your project folder. Add `--global` to install across projects.

Ask your agent to use Morten's UI principles when working on UI. The skill tells the agent to fetch the current principles each time and report any fetch failure.

## Update the rules

Edit [principles.md](principles.md) on `main`. Rule changes need no reinstall. Changes to the [skill loader](SKILL.md) do.

Keep project-specific rules in `AGENTS.md` or a file it links to. Leave the installed loader unchanged.
