# Solution Survey

This document tracks candidate solutions. A candidate being listed here does **not** mean it has been adopted; hands-on testing and source/license verification are required before final decisions.

## Evaluation Priorities

In descending order:

1. Casual-player usability
2. Nexus-centered installation and management
3. Stability and maintenance health
4. Existing feature coverage
5. zh-TW readiness / ability to contribute localization upstream
6. Compatibility with other selected components
7. Resource usage and latency
8. Extensibility
9. Amount of custom code required

## Candidate Matrix

| Workstream | Candidate | Intended Role | Initial Strategy | Status |
| --- | --- | --- | --- | --- |
| Localization | lang5-nexus-cn / Nexus Lang5-style solution | Game localization | Install and test before considering any custom implementation | Research / hands-on test |
| Chat data | Events: Chat | Expose GW2 chat events to Nexus addons | Reuse as infrastructure if translation integration is needed | Research |
| Chat translation | CatBridge and other Nexus-compatible translators | Live translation | Determine whether an existing solution is sufficiently seamless | Research |
| Events | World Events | World boss / meta tracking | Compare against actual casual-player needs, not strict Blish feature parity | Hands-on test |
| Pathing | TaimiHUD | Pathing / marker packs / related HUD features | Test existing packs and zh-TW contribution path | Hands-on test |
| Pathing | Other Nexus-native pathing addons | Alternative pathing implementation | Compare only if TaimiHUD has meaningful gaps | Research |
| Chat UX | Better Chat | Improved native chat experience | Investigate integration/API possibilities only if useful | Research |

## Localization Questions

- Can the candidate be installed and updated entirely through Nexus?
- Does it support Traditional Chinese directly?
- What translation source/database does it use?
- How are game updates handled?
- Does it alter game memory, hook strings, replace resources, or use another mechanism?
- Does it coexist cleanly with other Nexus addons?
- Is source code available and what is the license?

## Chat Translation Questions

- Can chat text be consumed directly through Nexus events?
- What is the Events: Chat payload and API stability?
- Is there already a Nexus-native translator that makes custom development unnecessary?
- Can an existing translator run invisibly enough that the player still experiences a single Nexus-centered setup?
- Can player names be excluded from cloud translation requests?
- Can zh-TW terminology be customized?
- What is the typical translation latency?
- Can common phrases be cached locally?

## World Events Questions

Compare World Events with the practical parts of the current Events and Metas Observer workflow:

- Event coverage
- World boss coverage
- Meta-chain coverage
- Favorites/subscriptions
- Upcoming event visibility
- Notifications and sounds
- Map-context awareness
- UI clarity
- zh-TW support
- Maintenance/update quality

Do **not** require feature-for-feature parity if the simpler addon is sufficient in normal play.

## Pathing Questions

- Which TacO/Blish marker-pack formats are supported?
- Do commonly used packs work without conversion?
- Which Blish-specific behaviors are unsupported?
- Does the player actually rely on those unsupported behaviors?
- Is marker-pack installation/update simple?
- Does the project have a localization framework suitable for an upstream zh-TW contribution?
- Is there any reason to maintain our own pathing implementation?

## Integration Rule

Before writing a new component, document:

1. The exact user-visible gap.
2. Existing solutions tested.
3. Why configuration or upstream contribution cannot solve it.
4. The smallest integration layer that could solve it.
5. Why custom implementation has lower lifetime cost than the alternatives.
