# Source Snapshot Template

Use one file per source under `source-snapshots/`.
The goal is to keep a cheap rolling cache so the agent can scan recent signals without reopening many source pages.

## Instructions

- Keep only the latest 10-20 relevant items.
- Prefer the last 30-90 days.
- Each item should be 1-3 lines, not a full summary.
- Include direct post URLs where possible.
- Remove stale or duplicate signals.

```yaml
source_id: example-source
last_refreshed: YYYY-MM-DD
coverage_window_days: 90
snapshot_items:
  - date: YYYY-MM-DD
    title: "Short post or article title"
    platform: "Weibo"
    url: "https://example.com/post"
    signal: "One-sentence extraction of the trend, workflow, tool, or business move."
    tags: [agent-workflow, prompt-engineering]
    confidence: high
  - date: YYYY-MM-DD
    title: "Another item"
    platform: "Zhihu"
    url: "https://example.com/post-2"
    signal: "Another short extraction."
    tags: [commercialization]
    confidence: medium
gaps:
  - "Missing direct URLs for WeChat official account posts."
next_refresh_hint:
  - "Check the weekly archive first."
```
