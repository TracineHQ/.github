## Infrastructure for safe, observable AI development

Tracine builds open-source tools that make AI coding agents safer, more transparent, and easier to trust in production workflows.

### Products

| | Project | Description | Install |
|---|---------|-------------|---------|
| **Guard** | [guard](https://github.com/TracineHQ/guard) | Security hooks for Claude Code — validates commands, protects credentials, enforces git safety | `/plugin marketplace add TracineHQ/guard` |
| **Convo** | [convo](https://github.com/TracineHQ/convo) | Claude Code plugin + CLI — auto-indexes session logs to SQLite, FTS5 search, slash commands, and a history-recall skill | `/plugin marketplace add TracineHQ/convo` or `pipx install tracine-convo` |
| **Triage** | tracine-triage | AI-assisted SAST triage — prioritizes security findings with LLM analysis | *Coming soon* |

### Philosophy

- **Safe by default** — Pre-built guardrails that validate every tool call before execution
- **Observable** — Query what your AI agent actually did, not what it said it did
- **Zero dependencies** — Pure Python stdlib. No bloat, no supply chain risk

### Links

[tracine.dev](https://tracine.dev) | [Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0)
