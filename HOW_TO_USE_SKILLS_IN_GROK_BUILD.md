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

## Automation Rules

Every push to `main` triggers:
1. Skill validation
2. Automatic mirroring of the skills directory to Google Drive

This keeps Valerie's visibility layer permanently up to date with zero manual steps.