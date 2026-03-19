---
name: opportunity-radar
description: Build short Opportunity Radar briefs for market or competitor trend research in AI, ML, banking, finance, and fintech, especially for signals from China, Hong Kong, Singapore, Thailand, Indonesia, and South Korea that may be applicable to Vietnam.
---

# Opportunity Radar

Use this skill when the user wants:
- market trend scouting,
- competitor signal detection,
- early opportunity spotting,
- short research briefs for AI, ML, banking, finance, or fintech,
- ideas from nearby Asian markets that could be applied in Vietnam.

Do not use this skill for:
- general-purpose academic research,
- broad literature reviews without a market or opportunity angle,
- coding or implementation work.

## Workflow

### 1. Lock the scope

Clarify only what is necessary:
- domain: AI, ML, banking, finance, fintech,
- lens: market trend, competitor move, or emerging technology,
- geography: default to China, Hong Kong, Singapore, Thailand, Indonesia, and South Korea,
- output: short `Opportunity Radar`.

If the user does not specify a time window, default to signals from the last 90 days.

### 2. Gather signals

Start with the highest-signal technical and research-oriented sources, then cross-check with market-facing sources.

Read [references/source-policy.md](./references/source-policy.md) before doing deep source collection.
Read [references/source-registry-policy.md](./references/source-registry-policy.md) when the task uses curated creator or influencer source registries.

When the request involves China-based creator, influencer, tool-curator, or practitioner signals, first consult the source index at [research-assistant/references/tech-blog-sources-index.md](/home/cuongpt/Workspaces/openclaw-agents-persona/research-assistant/references/tech-blog-sources-index.md), then load only the relevant source profiles and snapshots.

### 3. Rank opportunities

Prioritize signals in this order:
1. Likelihood of application in Vietnam
2. Novelty and differentiation
3. Relevance to AI, ML in banking, finance, fintech

If evidence is weak, contradictory, or isolated, say so explicitly.

### 4. Output the radar

Default output is a short brief with exactly these four sections:
1. `Linh vuc`
2. `Y tuong`
3. `Dan nguon`
4. `Keywords lien quan nen quan tam`

`Y tuong` must be framed as a use case that could be implemented in Vietnam.

Read [references/output-examples.md](./references/output-examples.md) when you need example phrasing or source patterns.

## Output Rules

- Keep the brief concise and easy to scan.
- Separate fact from inference.
- If a signal is older than 90 days, label it as background context rather than a fresh signal.
- Do not present unverified claims as established truth.
- Prefer Vietnamese by default, but preserve important English technical terms when precision matters.
