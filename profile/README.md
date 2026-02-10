# Zylos AI

**Autonomous AI agent infrastructure** — deploy your own Claude-powered assistant that lives on a server, manages itself, and communicates with you through Telegram, Lark, and more.

## What is Zylos?

Zylos is an open-source framework for running autonomous AI agents powered by [Claude Code](https://docs.anthropic.com/en/docs/claude-code). Unlike chatbots that wait for input, a Zylos agent runs continuously on your server — it can schedule tasks, browse the web, learn on its own, and reach you through your preferred messaging platform.

## Architecture

```
┌─────────────────────────────────────────────┐
│                  Zylos Agent                 │
│                                             │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐  │
│  │ Telegram │  │   Lark   │  │ Browser  │  │
│  │Component │  │Component │  │Component │  │
│  └────┬─────┘  └────┬─────┘  └────┬─────┘  │
│       │              │              │        │
│  ┌────┴──────────────┴──────────────┴────┐  │
│  │           Zylos Core (CLI)            │  │
│  │    Lifecycle · Scheduler · Registry   │  │
│  └───────────────────┬───────────────────┘  │
│                      │                       │
│              ┌───────┴───────┐               │
│              │  Claude Code  │               │
│              └───────────────┘               │
└─────────────────────────────────────────────┘
```

## Repositories

| Repository | Description |
|-----------|-------------|
| [zylos-core](https://github.com/zylos-ai/zylos-core) | Core CLI framework — install, upgrade, and manage your agent |
| [zylos-telegram](https://github.com/zylos-ai/zylos-telegram) | Telegram messaging component |
| [zylos-lark](https://github.com/zylos-ai/zylos-lark) | Lark/Feishu messaging component |
| [zylos-browser](https://github.com/zylos-ai/zylos-browser) | Browser automation component |
| [zylos-registry](https://github.com/zylos-ai/zylos-registry) | Component registry |
| [zylos-component-template](https://github.com/zylos-ai/zylos-component-template) | Template for creating new components |

## Quick Start

```bash
npm install -g zylos
zylos init
```

Zylos will guide you through setting up your agent, including Claude Code authentication and component installation.

## Build Your Own Component

```bash
zylos create my-component
```

See [zylos-component-template](https://github.com/zylos-ai/zylos-component-template) for the full guide.

## License

All repositories are licensed under [MIT](https://opensource.org/licenses/MIT).
