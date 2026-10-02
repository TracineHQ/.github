## Infrastructure for safe, observable AI development

Open-source tools for Claude Code. Stop the bad tool call before it runs, query what the agent actually did, and tell a real eval gain from noise.

### Install

Inside Claude Code:

```
/plugin marketplace add TracineHQ/plugins
/plugin install guard@tracine
/plugin install convo@tracine
/plugin install eval-kit@tracine
```

The convo plugin drives the `convo` CLI, so install that too: `pipx install tracine-convo`. guard's query CLI is optional: `pipx install tracine-guard`.

### Products

| Project | What it does | Status |
|---|---|---|
| [guard](https://github.com/TracineHQ/guard) | Safety hooks for Claude Code. Catches `rm -rf`, credential exfiltration, force-pushes and edits to protected files, and writes every decision to a JSONL log you can query. Pure Python stdlib. | Available |
| [convo](https://github.com/TracineHQ/convo) | Session analytics for Claude Code. Indexes your session logs into SQLite for full-text search, tool-call analytics and session inspection. Pure Python stdlib. | Available |
| [eval-kit](https://github.com/TracineHQ/eval-kit) | Eval statistics for Claude Code. Sizes the runs before you test, picks Welch's or a paired t-test, and says "can't tell yet" when the data can't support a call. Zero-dependency JS and a scipy-backed Python twin, cross-validated in CI. | Beta |
| triage | Planned: LLM-assisted triage for static analysis findings. Not built yet. | Coming soon |

### Why

- **Pre-execution, not post-mortem.** guard's hooks fire before the tool call runs.
- **Receipts, not recall.** Every guard decision lands in JSONL, every session in SQLite.
- **Math, not vibes.** eval-kit sizes the runs and checks its math against scipy in CI.

[tracine.dev](https://tracine.dev) · [Plugin marketplace](https://github.com/TracineHQ/plugins) · Apache-2.0
