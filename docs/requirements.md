# Requirements

## Product Goal

Make Guild Wars 2 comfortable for a casual player who does not want to learn or maintain multiple addon systems.

The product is the **experience**, not the codebase.

## Primary User Experience

After initial setup by a technical user, normal usage should ideally be:

1. Launch Guild Wars 2.
2. Nexus and required addons load automatically.
3. The game is understandable in Traditional Chinese where practical.
4. Foreign player chat is understandable without manual copy/paste.
5. Useful meta/world-event information appears at the right time.
6. Pathing and markers are available when needed.
7. The player does not need to manage separate addon applications during normal play.

## Functional Requirements

### R1 — Localization

- Prefer Traditional Chinese (Taiwan usage).
- Preserve established Guild Wars 2 terminology and commonly used community abbreviations where translating them would reduce clarity.
- Prefer an existing Nexus-compatible localization solution over a new localization engine.

### R2 — Chat Translation

- Translate incoming non-Chinese player chat into zh-TW with low perceived latency.
- Support common channels such as map, party, squad, guild, and whisper where technically available.
- Avoid requiring OCR when direct chat events are available.
- Avoid automatic outgoing messages; the player remains in control of anything sent to the game.
- Prefer an existing mature translator if it provides an acceptable Nexus-centered user experience.

### R3 — World Events / Meta Events

- Show relevant world bosses and meta events.
- Provide useful upcoming-event visibility and optional reminders.
- Prefer an existing Nexus addon if it covers the practical casual-player workflow.
- Feature parity with an existing Blish HUD module is not required if the simpler solution provides a better overall experience.

### R4 — Pathing

- Support useful trails, markers, and existing marker-pack ecosystems where possible.
- Prefer a maintained Nexus-native solution.
- Do not port/rewrite Blish HUD Pathing unless an important real-world compatibility gap remains.

## Non-Functional Requirements

### NFR1 — Single Mental Model

The player should only need to understand **Nexus** as the addon entry point.

Multiple Nexus addons are acceptable. Multiple independently managed addon frameworks/applications are strongly discouraged.

### NFR2 — Low Daily Friction

Normal gameplay should not require opening configuration screens, moving files, selecting translation providers, or troubleshooting dependencies.

### NFR3 — Low Maintenance

Prefer projects with active maintenance, automatic updates, permissive integration paths, and stable behavior.

### NFR4 — Reuse Before Build

Decision order:

**Install → Configure → Translate → Contribute → Integrate → Build**

### NFR5 — Upstream Friendly

When an existing project only lacks zh-TW or a small feature, prefer contributing upstream rather than maintaining a permanent fork.

### NFR6 — Safe, Read-Oriented Behavior

Avoid gameplay automation. Translation, visualization, reminders, and read-oriented assistance are preferred over automated input or automated responses.

## Success Criteria

Cozy Tyria succeeds when a casual player can launch Guild Wars 2 and comfortably play without needing to understand how the underlying addon stack works.
