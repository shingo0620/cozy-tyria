# Hands-on Test Plan

The purpose of hands-on testing is to evaluate the **player experience**, not merely confirm that an addon runs.

## Rating Scale

Use 1–5 for each category:

- **5** — essentially invisible/easy; suitable for a casual player
- **4** — small setup friction, good for daily use
- **3** — usable but noticeable complexity or missing features
- **2** — significant friction or reliability concerns
- **1** — unsuitable

## Common Test Dimensions

For every candidate record:

- Installation difficulty
- First-time configuration difficulty
- Daily-use friction
- Update/maintenance model
- Stability
- UI clarity
- zh-TW quality/readiness
- Compatibility with the rest of the Nexus setup
- Does the player need to know this addon exists after setup?

## Test A — Nexus Baseline

Goal: establish whether Nexus itself is comfortable as the single addon-management platform.

Check:

- Installation experience
- In-game addon discovery
- Install/update flow
- Enable/disable flow
- Error/recovery experience
- Whether normal play requires interacting with Nexus

## Test B — Localization

Candidate: Nexus-compatible Lang5-style localization solution.

Check:

- Install/update experience
- Traditional Chinese availability
- UI coverage
- Story/dialogue coverage
- Items/skills/events coverage
- Terminology quality
- Font/rendering issues
- Game-update resilience
- Compatibility with other selected addons

## Test C — World Events

Candidate: World Events.

Check during normal play:

- Can upcoming useful events be understood at a glance?
- Are favorite events easy to configure?
- Are notifications useful without being annoying?
- Does it cover the events actually played?
- Is anything from Events and Metas Observer genuinely missed?
- Does lack of zh-TW materially hurt usability?

## Test D — Pathing

Candidate: TaimiHUD.

Check:

- Marker-pack discovery/install
- Existing favorite packs
- Trails
- POI markers
- Map changes
- Performance
- Visual clutter
- Compatibility gaps compared with Blish HUD Pathing
- Whether those gaps matter in actual play

## Test E — Chat Translation

Candidates: existing mature translators first; custom integration only if needed.

Test messages in several languages and common GW2 shorthand.

Check:

- Map / party / squad / guild / whisper coverage
- Translation latency
- GW2 terminology quality
- UI intrusiveness
- Privacy/configuration burden
- Whether a separate application must be understood or manually launched
- Whether it feels like part of the Nexus-centered experience

## Field Notes Template

```md
### Candidate

Version/date:

Scores:
- Installation: /5
- Setup: /5
- Daily use: /5
- Maintenance: /5
- Stability: /5
- UI clarity: /5
- zh-TW: /5

What worked:
-

What was annoying/confusing:
-

Missing features that actually mattered:
-

Would a casual player need help again after initial setup?
-

Verdict: Keep / Keep + upstream contribution / Investigate / Replace
```

## Acceptance Principle

A candidate does not need feature parity with an existing power-user tool. It needs to make normal Guild Wars 2 play easier and more enjoyable with less ongoing support.
