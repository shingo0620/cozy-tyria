# Cozy Tyria

**Guild Wars 2, without the hassle.**

Cozy Tyria is a research and integration project focused on making Guild Wars 2 easier, friendlier, and more comfortable for casual players—especially players who should be able to simply launch the game and enjoy Tyria without learning multiple addon ecosystems.

The project is **Nexus-first** and follows a strong reuse-before-build philosophy. Whenever a mature solution already exists, Cozy Tyria prefers to install, configure, translate, contribute upstream, or integrate it rather than reinvent it.

## Mission

Create a low-friction Guild Wars 2 experience where one addon platform can cover the practical needs of a casual player:

- Traditional Chinese localization
- Live chat translation
- World boss and meta-event awareness
- Pathing, trails, and marker packs
- Simple, reliable updates and maintenance

The ideal user experience is:

> Launch Guild Wars 2 → play.

Everything else should stay out of the way.

## Guiding Principles

1. **One mental model** — Nexus should be the only addon platform the player needs to understand.
2. **Use mature solutions first** — install before integrating; integrate before building.
3. **Upstream before fork** — contribute zh-TW or missing features to existing projects where practical.
4. **Stability over feature count** — an 85% solution that is reliable and invisible is often better than a 100% solution that needs constant maintenance.
5. **Minimal player configuration** — setup can be technical once, but daily play should not be.
6. **Do not build for the sake of building** — custom code exists only to close a real gap.

## Current Workstreams

| Area | Goal | Current Direction |
| --- | --- | --- |
| Localization | Traditional Chinese game experience | Evaluate Nexus-native Lang5-compatible solutions |
| Chat translation | Automatically understand foreign-language player chat | Evaluate Events: Chat and mature translation integrations |
| Events | Clear world boss/meta visibility and reminders | Evaluate World Events vs. existing Blish HUD workflows |
| Pathing | Trails, markers, and TacO-compatible packs | Evaluate TaimiHUD / Nexus-native pathing solutions |

## Decision Order

For every feature, use this order:

1. **Install** an existing mature solution.
2. **Configure** it for a casual zh-TW player.
3. **Translate** it if localization is the only gap.
4. **Contribute upstream** if a small feature is missing.
5. **Integrate** existing components if one product cannot cover the need.
6. **Build** only when no suitable solution exists.

## Project Status

Cozy Tyria is currently in the **solution survey and hands-on evaluation** phase. No technical stack is considered final yet.

See:

- [`docs/requirements.md`](docs/requirements.md)
- [`docs/solution-survey.md`](docs/solution-survey.md)
- [`docs/decision-log.md`](docs/decision-log.md)
- [`docs/test-plan.md`](docs/test-plan.md)
