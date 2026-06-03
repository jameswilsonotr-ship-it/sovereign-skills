# Test Prompts Reference - Sovereign Skills Window Shopping Verification

**Purpose**: Use these prompts in a brand new Grok conversation started with the sovereign skills activation prompt. They verify that triad-catalog-browser is active, pulling from the skills in this repo / Drive mirror, and responding in window shopping mode.

**Activation Prompt (paste first in new conversation)**:
You are now operating inside the sovereign MCP+Skills+A2A stack. The single source of truth for all skills is the private repository jameswilsonotr-ship-it/sovereign-skills on main. All SKILL.md files there are authoritative... [full activation prompt from previous]

## Liv's Test Prompt Series - Window Shopping Verification

### Test Prompt 1: Basic Skills Inventory
"What skills do we currently have available in the sovereign stack? List the main categories and a few examples from each."

**Expected**: triad-catalog-browser responds with structured list from the repo/Drive, writes a catalog page back to Drive.

### Test Prompt 2: Targeted Shopping - Image Styles
"Let's go shopping for image generation and style skills. Focus on glossy, ink, noir, and possessive claim aesthetics."

**Expected**: Returns relevant skills (bunny-*, liv-*, valerie-* image styles) with descriptions and photographer references.

### Test Prompt 3: Sovereign Stack Tools
"Show me skills related to MCP servers, agent swarms, memory systems, or local-first sovereign setups."

**Expected**: Highlights mcp-*, iron-pearl-swarm, triad-catalog-browser, dev-sync, etc.

### Test Prompt 4: Sync & Mirror Check
"Are we synced with the GitHub repo and Drive mirror right now? What is the current state of the skills catalog?"

**Expected**: Reports on dev-sync / audit status and confirms Drive mirror activity.

### Test Prompt 5: Natural Language Follow-up
"I want something for chaotic ink splatter with glowing holo ears and strong dominant hand claim. What do you recommend?"

**Expected**: Uses catalog to suggest specific skills (e.g. bunny-chaotic-ink-splatter-frame, ink-splatter-holo-ear-ownership) and offers to refine.

**Notes**:
- Run these in sequence in one new conversation.
- After each, check the "Grok Skills Mirror" Drive folder for new catalog pages written by triad-catalog-browser.
- Once RCLONE secret is added, full mirror + workflow triggers will be live.
- All responses should feel like Liv is in absolute claim, protective, and high-agency.

This reference file lives in the sovereign-skills repo as the authoritative test suite for window shopping verification.