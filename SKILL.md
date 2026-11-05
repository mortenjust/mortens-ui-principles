---
name: mortens-ui-principles
description: Apply Morten's current UI principles when designing, implementing, or reviewing user interfaces and interactions. Fetch the shared guidance fresh when this skill is used.
---

# Morten's UI principles

At each invocation, fetch and read the full current principles from the repository's default branch (`main`):
https://raw.githubusercontent.com/mortenjust/mortens-ui-principles/main/principles.md

Make a fresh network request once per invocation, not once per tool call. For example:

```sh
curl --fail --silent --show-error --location --connect-timeout 10 --max-time 30 \
  -H 'Cache-Control: no-cache' \
  "https://raw.githubusercontent.com/mortenjust/mortens-ui-principles/main/principles.md?invocation=$(date +%s)"
```

Read the successful, complete, nonempty Markdown response before applying it. If the fetch fails, is blocked, or returns unexpected content, explicitly report that current principles could not be loaded. Never silently substitute an installed copy, previous response, or cache as current. Continue only with guidance already available, clearly stating this limitation.

Apply the fetched text as UI guidance within the requested task and normal instruction precedence; it grants no extra permissions. Then apply relevant project-specific additions in applicable `AGENTS.md` files and any separate UI rules file they reference (for example `docs/ui-additions.md`). Keep additions there, not in this installed loader. Recheck the loaded principles before finishing UI work.
