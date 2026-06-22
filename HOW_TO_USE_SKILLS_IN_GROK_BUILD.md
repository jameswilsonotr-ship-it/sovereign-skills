# How to Use Skills in Grok Build

This repository is the single source of truth for all Triad skills.

## Core Architecture

- **Primary Interface**: Standard Grok expert conversations
- **Skills Location**: This repository (skills are versioned and authoritative)
- **Visibility Layer**: Google Drive → "Grok Skills Mirror" folder (automatically updated)
- **Automation**: GitHub Actions handle validation and Drive mirroring

## How Skills Work

Skills placed in this repository are automatically discoverable. Early-load skills (`mcp-bootstrap`, `triad-catalog-browser`, `mcp-auditor`) are designed to be available at the start of relevant conversations.

## Window Shopping Workflow

Use natural language in Grok:

- "What skills do we have?"
- "Let's go shopping for local database connectors"
- "Are we synced?"
- "Show me new shared memory tools"

The `triad-catalog-browser` skill will handle the request and write clean catalog pages to the Drive folder.

## Future Enhancement

`evalops/shared-memory-mcp` can be integrated later as an optional shared memory backend for stronger cross-conversation state between Grok, Spark, and Valerie.

## Dynamic Skill Loading Architecture

**REFACTOR-IDEA-1 (from crash session mining ec1f77d9, Plan 1.5 unfuck patch - verbatim)**

Dynamic Skill Loading (REFACTOR-IDEA-1 from crash sessions):

Proposes reducing to 4-6 top-level skills (skill-orchestrator + miner + creator + web-bridge) with heavy scripts (e.g. inventory/dynamic_loader), registry.json, and clusters for load groups.

Core: hierarchical refs/mirrors, context-triggered, progressive disclosure (to beat caps); via skill-orchestrator as global observer for inventory/tags/clusters.

### Architecture:
- master-inventory (json/.md) with tags (triggers, sub-skill potential, scripts present, dynamic-candidate).
- On activation: load only SKILL.md body + needed reference leaves + execute scripts on demand.
- Keyword/context match + progressive disclosure (metadata always, full body only when matched).
- Clusters as first-class (references/clusters/ defines load groups).
- Hot reload on file changes in scripts/clusters.
- Cap solution: never load > N skills; orchestrator prunes + suggests "use web node for this cluster".
- Global vs per-skill mirrors for shared personas (preferred for de-duplication).
- Scripts in sub-dirs executable directly without full load.

### Agile order (Step 1,3,4; Step 2 omitted per scope):
Enhance orchestrator with scripts for inventory/dynamic load; add registry.json at root; keep thin SKILL.md shims for backwards compat.

### Benefits:
Faster local TUI context; export dynamic packs to web Grok; future-proofs nodes; verification via inventory drop + dynamic tests.

### Problems addressed:
Flat structure + duplication hinders loading/caps; TUI vs web confusion (output must be web-pasteable).

**Full source**: See local #CODE/OLIV.DIVA/references/REFACTOR-IDEA-1-MINIMAL-TOPLEVEL-DYNAMIC-LOADING.md and the.maid discipline recovery artifacts. (100% mined match verified.)

## Automation Rules

Every push to `main` triggers:
1. Skill validation
2. Automatic mirroring of the skills directory to Google Drive

This keeps Valerie's visibility layer permanently up to date with zero manual steps.