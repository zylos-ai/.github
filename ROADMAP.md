# Zylos Roadmap

This roadmap outlines what we've shipped and where we're headed. Each milestone expands three dimensions: **channels** (how your agent communicates), **capabilities** (what your agent can do), and **core platform** (what keeps everything running).

> This is a living document. Priorities may shift based on community feedback. See [milestones](https://github.com/zylos-ai/zylos-core/milestones) for detailed progress tracking.

---

## v0.1.x — A memorable AI agent, ready in 2 minutes :white_check_mark:

*The foundation: an AI that remembers, acts, and never stops running.*

**Channels (4)**
| Channel | Component |
|---------|-----------|
| Telegram | [zylos-telegram](https://github.com/zylos-ai/zylos-telegram) |
| Lark | [zylos-lark](https://github.com/zylos-ai/zylos-lark) |
| Feishu (飞书) | [zylos-feishu](https://github.com/zylos-ai/zylos-feishu) |
| Web Console | Built-in |

**Capabilities (6)**
| Capability | Description |
|------------|-------------|
| Persistent Memory | Inside Out-inspired tiered memory that survives restarts and syncs across sessions |
| Task Scheduler | Cron, interval, and one-time tasks — your agent works while you sleep |
| Browser Automation | Control a real browser for web research, screenshots, and interaction |
| Image Generation | Create and edit images using AI models |
| HTTP File Sharing | Share files and host web content via built-in Caddy server |
| Crash Recovery | Heartbeat monitoring, stuck detection, auto-restart with exponential backoff |

**Core Platform**
| Feature | Description |
|---------|-------------|
| Component Management | `zylos add/upgrade/remove` — install components from the registry in one command |
| Smart Merge Upgrades | Three-way merge preserves your customizations during component upgrades |
| Communication Bridge | Unified message gateway across all channels with control queue and heartbeat |
| Session Handoff | Graceful context management — background tasks survive session transitions |
| Daily Auto-Upgrade Check | Detects new versions of core and components, notifies you automatically |
| Skill System | Modular architecture for extending your agent with new abilities |
| PM2 Orchestration | All services managed, monitored, and auto-started on boot |

**Status:** Released — [v0.1.0](https://github.com/zylos-ai/zylos-core/releases/tag/v0.1.0) through [v0.2.4](https://github.com/zylos-ai/zylos-core/releases/tag/v0.2.4)

---

## v0.2.0 — Expand fast, cover mainstream channels and core capabilities

*Growing the ecosystem with popular platforms and essential skills.*

**New Channels (+2)**
| Channel | Description |
|---------|-------------|
| Discord | Community-friendly bot integration |
| WhatsApp | Reach users on the world's most popular messenger |

**New Capabilities (+5)**
| Capability | Description |
|------------|-------------|
| Knowledge Base | RAG-powered document retrieval for grounded answers |
| Basic Workflows | Define multi-step automated routines |
| Twitter Automation | Schedule posts, monitor mentions, engage with your audience |
| Email Automation | Send, receive, and act on emails |
| Voice | Speech-to-text and text-to-speech for voice interactions |

**Cumulative:** 6 channels, 11 capabilities

---

## v0.3.0 — Connect global platforms, bridge work scenarios

*Reaching users where they work — across regions and productivity tools.*

**New Channels (+3)**
| Channel | Description |
|---------|-------------|
| Slack | Enterprise team communication |
| WeCom (企业微信) | China's leading enterprise messenger |
| Signal | Privacy-focused secure messaging |

**New Capabilities (+3)**
| Capability | Description |
|------------|-------------|
| Calendar Integration | Manage schedules, create events, send reminders |
| Notion Integration | Read and write Notion pages and databases |
| Obsidian Integration | Access and manage your Obsidian knowledge vault |

**Cumulative:** 9 channels, 14 capabilities

---

## v1.0.0 — Enterprise-ready, ecosystem formed

*Production-grade reliability, a thriving marketplace, and multi-model flexibility.*

**New Channels (+2)**
| Channel | Description |
|---------|-------------|
| Microsoft Teams | Enterprise collaboration at scale |
| DingTalk (钉钉) | Widely used enterprise platform in China |

**New Capabilities (+3)**
| Capability | Description |
|------------|-------------|
| Workflow Orchestration | Visual workflow builder with conditions, loops, and triggers |
| Component Marketplace | Discover, publish, and install community-built components |
| Multi-model Support | Run with Claude, GPT, Gemini, or open-source models |

**Core Architecture**
| Feature | Description |
|---------|-------------|
| Multi-session Claude | Parallel tmux sessions for concurrent task execution |
| Agent-to-Agent Communication | Agents collaborate and delegate across instances |
| CLI Flexibility | Swap the underlying LLM CLI (Claude Code, Codex, Gemini CLI) |

**Cumulative:** 11 channels, 17 capabilities

---

## Contributing

Interested in building a channel or capability? Check the [issues](https://github.com/zylos-ai/zylos-core/issues) or open a new one to discuss your approach.

See [CONTRIBUTING.md](https://github.com/zylos-ai/.github/blob/main/CONTRIBUTING.md) for guidelines.
