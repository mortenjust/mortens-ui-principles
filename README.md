# Morten's UI principles

A shared set of UI principles, fetched fresh whenever an agent uses the skill.

- [`principles.md`](principles.md) is the canonical guidance.
- [`SKILL.md`](SKILL.md) is a small discoverable loader. It tells the agent to fetch the current raw file from `main` once per invocation, apply it, then read relevant project additions.

The initial principles preserve the complete body of Morten's existing global `ui-principles` skill, including all 16 numbered rules. Additional tooltip guidance found in a project copy has not been assumed to be shared policy.

## Install

Use Node.js 22.20 or later with the [skills CLI](https://github.com/vercel-labs/skills). Choose one scope.

Globally for Codex, across projects on this machine:

```sh
npx skills add mortenjust/mortens-ui-principles --skill mortens-ui-principles --agent codex --global --yes
```

Or run this from a project's root for that project only:

```sh
npx skills add mortenjust/mortens-ui-principles --skill mortens-ui-principles --agent codex --yes
```

For Codex, the CLI uses `~/.agents/skills/mortens-ui-principles/` globally and `.agents/skills/mortens-ui-principles/` in a project. Omit `--agent codex --yes` to choose agents interactively. The command flags are documented in the [installation reference](https://github.com/vercel-labs/skills/blob/main/docs/commands.md#skills-add) and `npx skills --help`.

Verify discovery before installing:

```sh
npx skills add mortenjust/mortens-ui-principles --list
```

In Codex, the skill is available on the next turn. Invoke it explicitly with `$mortens-ui-principles`, or let the agent select it for UI work. Installation applies only to the selected machine and scope.

## Shared updates

Edit `principles.md` in this repository and publish the change to `main`. The next invocation instructs the agent to fetch the new text; no periodic sync or revision pin is needed for principle updates. The agent must actually fetch and read it. This instruction-based loader is not a runtime hook and cannot mechanically guarantee agent compliance or upstream cache freshness.

An installation may contain a snapshot of `principles.md` because installers copy repository files. That snapshot is not the invocation source. The loader requests the raw GitHub URL anew with a cache-busting query and a no-cache header. It must report fetch failures or blocked networking, and must never silently call cached or bundled content current. No fallback cache is configured.

Changes to `SKILL.md` itself still require reinstalling/updating the loader. If the default branch is renamed, update its raw URL here and in `SKILL.md`, then update installations.

## Project-specific additions

Keep local UI rules in the project's `AGENTS.md`, or put them in a clearly named file that `AGENTS.md` references, for example:

```markdown
## UI work

Use $mortens-ui-principles for shared UI guidance, then read
[project UI additions](docs/ui-additions.md) for this product's rules.
```

Store only project-specific additions in that file, such as component choices or product terminology. The loader does not change normal instruction precedence. Do not edit the installed `SKILL.md` or copy the shared principles into each project.

When migrating an older UI skill, compare it with `principles.md` first. Preserve unique additions separately, update references to the new skill name, then retire the old duplicate so agents do not select stale guidance. Do not overwrite divergent project rules automatically. Installing this repository alone does not migrate older installations on this or other machines.
