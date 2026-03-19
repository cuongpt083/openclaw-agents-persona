# Source Registry Policy

Use this policy when working with curated creator and influencer registries, especially the China source registry at [research-assistant/references/tech-blog-sources-index.md](/home/cuongpt/Workspaces/openclaw-agents-persona/research-assistant/references/tech-blog-sources-index.md).

## Purpose

The registry exists to reduce noisy platform search and make source selection more repeatable.
Use it to:

- shortlist relevant creators quickly
- open known source pages directly
- constrain search to a creator's actual topic coverage
- extract trend and idea signals with consistent citation

## Default Retrieval Order

Use this order unless the user explicitly asks for wider exploration:

1. `topic_index`
2. source profile
3. source snapshot
4. `direct_urls`
5. `lookup_urls`
6. generic platform search

Do not start from generic search when a relevant registry entry already exists with usable URLs.

## Source Selection Rules

- Prefer `P1` sources before `P2` sources.
- Prefer sources whose `focus_topics` and `signal_types` match the user request closely.
- For broad scans, start with 3-5 sources, not the whole registry.
- For narrow technical validation, choose fewer but higher-fit sources.
- For China creator signals, prefer direct creator pages over reposts, summaries, or aggregator commentary.
- Load the source index first, not the full registry overview.
- Open only the 2-4 source profiles that match the task.
- If a snapshot file exists, scan it before reopening live source pages.

## Time Window

- Default to the last 90 days.
- Older content can be used as background context, but label it clearly as not a fresh signal.
- If the registry source is active but recent posts are missing on one platform, check the source's other listed platforms before widening search.

## Evidence Standards

A strong registry-backed signal usually has:

- a matching index topic and source profile
- a useful recent snapshot item or a clear reason to fetch a live page
- a direct source page
- a recent post or article
- an explicit topic match
- at least one concrete implementation, tool, workflow, or market move

A weaker signal usually has:

- only a lookup URL
- ambiguous identity
- only reposted commentary
- no obvious path to a Vietnam-relevant use case

## Citation Requirements

When using registry-backed findings, capture these fields whenever available:

- source ID
- source name
- platform
- page URL
- post or article title
- post date
- extracted signal
- classification: `fact`, `inference`, or `hypothesis`

## Fallback Rules

Expand beyond the registry only when:

- the registry has no relevant source for the topic
- listed URLs are dead, stale, or inaccessible
- the topic is too new and registry coverage is clearly insufficient
- you need corroboration from official, technical, or market-facing sources

When expanding, preserve the registry source as the starting anchor and document what the registry did not cover.

## Maintenance Guidance

- Keep the index compact and stable.
- Keep source profiles durable and relatively static.
- Store recent signals in snapshot files so they can be refreshed without rewriting the profiles.
- Recheck direct URLs periodically.
- Upgrade a source only after repeated high-signal output.
- Deprecate a source when it becomes inactive, low-quality, or identity-ambiguous.
