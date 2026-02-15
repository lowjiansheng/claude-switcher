# Claude Switcher

A CLI tool to quickly switch between different LLM providers in Claude Code.

## Features

- Switch between MiniMax, Kimi, and Anthropic Claude (subscription)
- Simple command-line interface
- Easy to add new providers

## Installation

1. Clone this repository
2. Add to your PATH:

```bash
# Add to ~/.zshrc
export PATH="/path/to/claude-switcher:$PATH"
```

3. Restart your terminal or run `source ~/.zshrc`

## Usage

```bash
# Switch to a provider
claude-switch minimax
claude-switch kimi
claude-switch claude

# List all available profiles
claude-switch list

# Show current profile
claude-switch status

# Add a new profile
claude-switch add

# Remove a profile
claude-switch remove <name>
```

## Available Profiles

| Profile | Provider | Auth Method |
|---------|----------|-------------|
| minimax | MiniMax M2.5 | API Token |
| kimi | Kimi K2.5 | API Token |
| claude | Claude (Opus 4.6) | OAuth |

## Requirements

- Claude Code installed
- API keys for MiniMax/Kimi (already configured)
- Claude.ai subscription for OAuth (claude profile)

## Notes

- When switching profiles, restart Claude Code to use the new model
- Configuration files are stored in `configs/` directory
- Current settings are applied to `~/.claude/settings.json`
