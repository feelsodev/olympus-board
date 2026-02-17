# Olympus Command Board

An interactive game board that visualizes an AI agent collaboration system in RPG Olympus style.

**[Live Demo](https://feelsodev.github.io/olympus-board/)**

## Features

| Feature | Description |
|---------|-------------|
| **RPG Game Board Layout** | Spatial hierarchy with 8 gods orbiting the Olympus temple |
| **Character Portraits** | Unique PNG portraits with per-agent color themes |
| **Workflow Simulation** | Animated particle flows: Boss → Zeus → parallel dispatch → cycle |
| **Click Modal** | Detailed view with role, persona, stats, rules, and AI mapping |
| **SVG Connections** | Animated dash-pattern lines between temple and agents |
| **Stat Bars** | 3 ability bars per character with unique color gradients |
| **Status Indicators** | IDLE/ACTIVE toggle with green/yellow pulse |
| **Ticket System** | Task tickets with QUEUED/RUNNING/DONE/DELAYED/BLOCKED states |
| **Gold Particles** | Ambient floating golden particle background |
| **Responsive** | Desktop (3-col) → Tablet (2-col) → Mobile (1-col) |

## Agents

```
                    [BOSS]
                      │
                   [ZEUS]          ← Conductor
                  ╱       ╲
           [ATHENA]    [PROMETHEUS] ← Strategy / Planning
           ╱    ╲           ╱    ╲
      [HERMES]  [TEMPLE]  [APOLLO] ← Scout / Design
           ╲       │       ╱
     [HEPHAESTUS]     [SISYPHUS]   ← Forge / Ops
                  ╲   ╱
                 [HADES]           ← Review
```

| God | Role | AI Agent Mapping |
|-----|------|------------------|
| **Zeus** | Chief Orchestrator | Main Orchestrator — receives, decomposes, delegates, reports |
| **Athena** | Strategy & Architecture | Oracle — read-only high-IQ reasoning consultant |
| **Prometheus** | Planning & Decomposition | Planner — strategic task breakdown, task graph generation |
| **Hermes** | Recon & Codebase Search | Explorer — contextual code search messenger |
| **Apollo** | UI/UX & Frontend | Designer — visual engineering specialist |
| **Hephaestus** | Code Implementation | Executor — the forge builder |
| **Sisyphus** | Ops & Persistent Execution | Persistent Worker — never stops until done |
| **Hades** | Code Review & QA | Critic — the unforgiving quality gate |

## Quick Start

```bash
# No install needed. Open directly in browser.
open index.html

# Or serve locally
npx serve .
```

## Tech

- **Zero Dependencies** — no external CDNs or libraries
- **Single File** — HTML + CSS + JS all in one `index.html`
- **Pure CSS Animations** — GPU-accelerated via transform/opacity
- **SVG Connections** — dynamic connection lines with resize handling
- **Vanilla JS** — no frameworks, pure JavaScript

## Structure

```
olympus-board/
├── index.html                  # Main game board (v3)
├── index.html.bak2             # Previous version backup (v2)
├── assets/
│   └── characters/
│       ├── zeus.png
│       ├── athena.png
│       ├── prometheus.png
│       ├── hermes.png
│       ├── apollo.png
│       ├── hephaestus.png
│       ├── sisyphus.png
│       ├── hades.png
│       └── olympus-temple.png
└── README.md
```
