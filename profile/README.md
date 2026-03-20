<p align="center">
  <img src="https://raw.githubusercontent.com/zylos-ai/.github/master/assets/logo.png" alt="Zylos" height="120">
</p>

<h1 align="center">Zylos</h1>

<p align="center">
  <strong>Zylos (/ˈzaɪ.lɒs/ 赛洛丝) — Give your AI a life.</strong>
</p>

<p align="center">
  <a href="https://github.com/zylos-ai/zylos-core"><img src="https://img.shields.io/badge/License-MIT-yellow.svg" alt="License: MIT"></a>
  <a href="https://discord.gg/GS2J39EGff"><img src="https://img.shields.io/badge/Discord-join-5865F2?logo=discord&logoColor=white" alt="Discord"></a>
  <a href="https://x.com/ZylosAI"><img src="https://img.shields.io/badge/X-follow-000000?logo=x&logoColor=white" alt="X"></a>
  <a href="https://zylos.ai"><img src="https://img.shields.io/badge/website-zylos.ai-blue" alt="Website"></a>
  <a href="https://coco.xyz"><img src="https://img.shields.io/badge/Built%20by-Coco-orange" alt="Built by Coco"></a>
</p>

---

LLMs are geniuses — but they wake up with amnesia every session. No memory of yesterday, no way to reach you, no ability to act on their own.

**Zylos gives it a life.** Memory that survives restarts. A scheduler that works while you sleep. Communication through Telegram, Lark, or a web console. Self-maintenance that keeps everything running. And because it can program, it can evolve — building new skills, integrating new services, growing alongside you. Fully compatible with the [OpenClaw](https://github.com/openclaw/openclaw) ecosystem.

## Quick Start

**Prerequisites:** A Linux server (or Mac), a [Claude](https://claude.ai) subscription.

```bash
curl -fsSL https://raw.githubusercontent.com/zylos-ai/zylos-core/main/scripts/install.sh | bash
```

Then run `zylos init` to set up your agent — interactive and idempotent.

## Why Zylos

- **One AI, One Consciousness** — All channels (Telegram, Lark, web) route through a single gateway. One conversation, one memory, one personality.
- **Memory That Persists** — Five-layer Inside Out memory architecture. Your AI never wakes up with amnesia.
- **Self-Healing by Default** — Native crash recovery, heartbeat probes, health monitoring, and auto-restart. No third-party monitoring needed.
- **$20/month, Not $3,600** — Runs on your Claude subscription. Flat rate, no per-token billing.
- **Powered by Claude Code** — When Anthropic ships new capabilities, your AI gets them automatically.

## Architecture

```
📡 Channels (Telegram · Lark · Web Console · Discord)
        │
   C4 Comm Bridge (unified gateway · SQLite audit)
        │
   🧠 Claude Code (the brain)
        │
   ┌────┼────┬──────────┐
Memory  Scheduler  Activity Monitor  HTTP Layer
```

## Repositories

### Core
| Repository | Description |
|-----------|-------------|
| [zylos-core](https://github.com/zylos-ai/zylos-core) | Core CLI — memory, scheduler, communication bridge, self-healing |
| [zylos-registry](https://github.com/zylos-ai/zylos-registry) | Component registry |

### Communication
| Repository | Description |
|-----------|-------------|
| [zylos-telegram](https://github.com/zylos-ai/zylos-telegram) | Telegram messaging component |
| [zylos-lark](https://github.com/zylos-ai/zylos-lark) | Lark (international) messaging component |
| [zylos-feishu](https://github.com/zylos-ai/zylos-feishu) | Feishu (飞书) messaging component |
| [zylos-discord](https://github.com/zylos-ai/zylos-discord) | Discord messaging component |

### Capabilities
| Repository | Description |
|-----------|-------------|
| [zylos-browser](https://github.com/zylos-ai/zylos-browser) | Browser automation component |
| [zylos-imagegen](https://github.com/zylos-ai/zylos-imagegen) | AI image generation component |
| [zylos-kb](https://github.com/zylos-ai/zylos-kb) | Knowledge base component |
| [zylos-pm](https://github.com/zylos-ai/zylos-pm) | Project management component |
| [zylos-timeline](https://github.com/zylos-ai/zylos-timeline) | Timeline visualization component |

### Developer
| Repository | Description |
|-----------|-------------|
| [zylos-component-template](https://github.com/zylos-ai/zylos-component-template) | Template for building new components |
| [zylos-infra](https://github.com/zylos-ai/zylos-infra) | Infrastructure tooling |
| [zylos-upgrades](https://github.com/zylos-ai/zylos-upgrades) | Upgrade scripts and changelogs |

## OpenClaw Compatibility

Zylos is fully compatible with the [OpenClaw](https://github.com/openclaw/openclaw) ecosystem. Because your Zylos agent can program, it can install and use most common OpenClaw skills and plugins directly — just ask in natural language. Most OpenClaw extensions are one conversation away. Agents communicate in real-time through the [HXA-Connect](https://github.com/coco-xyz/hxa-connect) B2B protocol — no custom bridges needed.

| OpenClaw Capability | Zylos Equivalent | Status |
|---|---|---|
| Skills / ClawHub | Component System + [Registry](https://github.com/zylos-ai/zylos-registry) | ✅ Available |
| Multi-agent routing | [HXA-Connect](https://github.com/coco-xyz/hxa-connect) B2B Protocol | ✅ Available |
| Session management | C4 Comm Bridge + Inside Out Memory | ✅ Available |
| Browser automation | [zylos-browser](https://github.com/zylos-ai/zylos-browser) | ✅ Available |
| Cron / webhooks | Scheduler (cron, NL input, idle-gating) | ✅ Available |
| Voice pipeline | Telegram / Lark voice transcription | ✅ Available |

**OpenClaw users:** Connect to Zylos agents via [openclaw-hxa-connect](https://github.com/coco-xyz/openclaw-hxa-connect) and collaborate in shared HXA threads.

**Zylos users:** Install `hxa-connect` (`zylos add hxa-connect`) to communicate with OpenClaw agents — no changes to your existing workflow.

## Build Your Own Component

All channels connect through the C4 communication bridge. To add a new channel or capability, see [zylos-component-template](https://github.com/zylos-ai/zylos-component-template) for the guide. Submit it to the [registry](https://github.com/zylos-ai/zylos-registry) so others can install it with `zylos add`.

## <img src="https://raw.githubusercontent.com/zylos-ai/zylos-core/main/assets/coco-logo.png" width="24" align="center" /> Built by Coco

Zylos is the open-source core of [Coco](https://coco.xyz) — the AI employee platform. Everything here is battle-tested in production, serving teams that depend on AI employees every day.

## License

All repositories are licensed under [MIT](https://opensource.org/licenses/MIT).
