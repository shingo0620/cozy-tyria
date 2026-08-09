# Decision Log

This log records product and architecture decisions so the project does not gradually drift toward unnecessary custom development.

## D-001 — Optimize for the casual-player experience

**Status:** Accepted  
**Date:** 2026-08-09

### Decision

The primary optimization target is not maximum addon functionality. It is a comfortable Guild Wars 2 experience for a casual player with minimal technical knowledge.

### Consequences

- Simpler solutions may win over more powerful ones.
- Configuration complexity counts as product cost.
- Maintenance burden counts as product cost.
- Invisible/reliable behavior is preferred over feature-rich dashboards.

---

## D-002 — Nexus-first

**Status:** Accepted  
**Date:** 2026-08-09

### Decision

Use Nexus as the preferred addon platform and the single addon-management mental model presented to the player.

### Clarification

This does not require all functionality to live in one DLL. Multiple independently maintained Nexus addons are desirable when Nexus provides a unified installation/update experience.

### Escape hatch

A second framework/application may only be introduced when it provides a major user benefit that cannot reasonably be achieved inside the Nexus-centered experience.

---

## D-003 — Reuse before build

**Status:** Accepted  
**Date:** 2026-08-09

### Decision

Use the following escalation path for every feature:

**Install → Configure → Translate → Contribute → Integrate → Build**

### Consequences

- Existing mature addons are the default solution.
- Missing zh-TW should normally result in an upstream localization contribution, not a fork.
- Missing small features should normally result in an upstream issue/PR.
- New repositories/components require a documented gap analysis.

---

## D-004 — Do not commit to a custom all-in-one addon yet

**Status:** Accepted  
**Date:** 2026-08-09

### Decision

Cozy Tyria begins as a solution survey, integration, configuration, localization, and contribution project. A custom monolithic "Tyria Companion" is not currently a goal.

### Reason

Nexus may already provide most required functionality through independently maintained addons. Combining them in code would create maintenance work without necessarily improving the player's experience.
