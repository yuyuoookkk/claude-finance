# claude-finance

Equity research workspace, wired to the [`equity-research`](https://github.com/anthropics/financial-services)
plugin from Anthropic's `claude-for-financial-services` marketplace.

## Setup

`.claude/settings.json` declares the marketplace and enables the plugin, so a fresh
clone picks it up automatically on the next Claude Code session. No manual install
is needed.

To install it outside this repo (user scope):

```
claude plugin marketplace add anthropics/financial-services
claude plugin install equity-research@claude-for-financial-services
```

## Commands

The plugin does not ship a single `/equity-research` command. It ships nine
task-specific commands:

| Command            | What it does                                              |
| ------------------ | --------------------------------------------------------- |
| `/initiate`        | Initiating-coverage report (5-task workflow)               |
| `/earnings`        | Quarterly earnings update report                           |
| `/earnings-preview`| Pre-earnings preview with bull/base/bear scenarios         |
| `/model-update`    | Update a financial model with new data or guidance         |
| `/thesis`          | Create or update an investment thesis                      |
| `/sector`          | Sector / industry overview report                          |
| `/screen`          | Stock screens and idea generation                          |
| `/catalysts`       | Catalyst calendar across the coverage universe             |
| `/morning-note`    | Morning meeting note                                       |

Most take an optional ticker or topic, e.g. `/earnings NVDA Q3 2025`.
