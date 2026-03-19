# China Tech Source Index

## Purpose

This is the low-cost entrypoint for the China tech source registry.
Load this file first.
Do not load all source profiles by default.

Use this file to:

- shortlist relevant source IDs by topic
- select `P1` sources before `P2`
- find the exact source profile path to open next

## Retrieval Flow

1. Read this index.
2. Select 2-4 source IDs from `topic_index`.
3. Open only the matching source profile files in `sources/`.
4. If available, open the matching snapshot file in `source-snapshots/`.
5. Open direct source pages only after the profile and snapshot indicate likely value.

## Topic Index

```yaml
topic_index:
  ai_commercialization:
    - wu-bin-jirui
    - baoyu-ai
    - goofy-ai-business
    - digital-life-khazix
  agent_workflow:
    - baoyu-ai
    - sunny-arbor
    - guizang-aigc-weekly
  prompt_engineering:
    - baoyu-ai
    - guizang-aigc-weekly
  open_source_tools:
    - github-daily
    - guizang-aigc-weekly
    - li-mu
  model_tuning_and_finetuning:
    - li-mu
    - li-hongyi
    - ding-xiaohan
  diffusion_and_ai_art:
    - akiba-aaaki
    - simon-arvin
    - hyacinth-ai-culture
    - guizang-aigc-weekly
  china_ai_ecosystem:
    - digital-life-khazix
    - goofy-ai-business
    - datafuntalk-huang-jia
  industry_ai_use_cases:
    - datafuntalk-huang-jia
    - goofy-ai-business
    - wu-bin-jirui
  research_and_courses:
    - li-hongyi
    - li-mu
    - ding-xiaohan
```

## Source Directory

```yaml
sources:
  - id: wu-bin-jirui
    priority: P1
    focus_topics: [AI e-commerce, AIGC commercialization, retail workflows]
    profile_path: /home/cuongpt/Workspaces/openclaw-agents-persona/research-assistant/references/sources/wu-bin-jirui.md
    snapshot_path: /home/cuongpt/Workspaces/openclaw-agents-persona/research-assistant/references/source-snapshots/wu-bin-jirui.md
  - id: guizang-aigc-weekly
    priority: P1
    focus_topics: [AIGC tools, open-source workflows, prompt engineering]
    profile_path: /home/cuongpt/Workspaces/openclaw-agents-persona/research-assistant/references/sources/guizang-aigc-weekly.md
    snapshot_path: /home/cuongpt/Workspaces/openclaw-agents-persona/research-assistant/references/source-snapshots/guizang-aigc-weekly.md
  - id: baoyu-ai
    priority: P1
    focus_topics: [agent workflow, prompt engineering, practical AI deployment]
    profile_path: /home/cuongpt/Workspaces/openclaw-agents-persona/research-assistant/references/sources/baoyu-ai.md
    snapshot_path: /home/cuongpt/Workspaces/openclaw-agents-persona/research-assistant/references/source-snapshots/baoyu-ai.md
  - id: li-hongyi
    priority: P1
    focus_topics: [ML concepts, generative AI, transformers]
    profile_path: /home/cuongpt/Workspaces/openclaw-agents-persona/research-assistant/references/sources/li-hongyi.md
    snapshot_path: /home/cuongpt/Workspaces/openclaw-agents-persona/research-assistant/references/source-snapshots/li-hongyi.md
  - id: github-daily
    priority: P1
    focus_topics: [open-source projects, developer tooling, AI applications]
    profile_path: /home/cuongpt/Workspaces/openclaw-agents-persona/research-assistant/references/sources/github-daily.md
    snapshot_path: /home/cuongpt/Workspaces/openclaw-agents-persona/research-assistant/references/source-snapshots/github-daily.md
  - id: simon-arvin
    priority: P2
    focus_topics: [AI art, Stable Diffusion, visual workflows]
    profile_path: /home/cuongpt/Workspaces/openclaw-agents-persona/research-assistant/references/sources/simon-arvin.md
    snapshot_path: /home/cuongpt/Workspaces/openclaw-agents-persona/research-assistant/references/source-snapshots/simon-arvin.md
  - id: hyacinth-ai-culture
    priority: P2
    focus_topics: [AI culture, guochao aesthetics, style transfer]
    profile_path: /home/cuongpt/Workspaces/openclaw-agents-persona/research-assistant/references/sources/hyacinth-ai-culture.md
    snapshot_path: /home/cuongpt/Workspaces/openclaw-agents-persona/research-assistant/references/source-snapshots/hyacinth-ai-culture.md
  - id: sunny-arbor
    priority: P1
    focus_topics: [AI productivity, Claude workflows, team process]
    profile_path: /home/cuongpt/Workspaces/openclaw-agents-persona/research-assistant/references/sources/sunny-arbor.md
    snapshot_path: /home/cuongpt/Workspaces/openclaw-agents-persona/research-assistant/references/source-snapshots/sunny-arbor.md
  - id: li-mu
    priority: P1
    focus_topics: [fine-tuning, model deployment, reproducible code]
    profile_path: /home/cuongpt/Workspaces/openclaw-agents-persona/research-assistant/references/sources/li-mu.md
    snapshot_path: /home/cuongpt/Workspaces/openclaw-agents-persona/research-assistant/references/source-snapshots/li-mu.md
  - id: ding-xiaohan
    priority: P1
    focus_topics: [CV architecture, model compression, paper interpretation]
    profile_path: /home/cuongpt/Workspaces/openclaw-agents-persona/research-assistant/references/sources/ding-xiaohan.md
    snapshot_path: /home/cuongpt/Workspaces/openclaw-agents-persona/research-assistant/references/source-snapshots/ding-xiaohan.md
  - id: akiba-aaaki
    priority: P1
    focus_topics: [ComfyUI, Stable Diffusion, local setup]
    profile_path: /home/cuongpt/Workspaces/openclaw-agents-persona/research-assistant/references/sources/akiba-aaaki.md
    snapshot_path: /home/cuongpt/Workspaces/openclaw-agents-persona/research-assistant/references/source-snapshots/akiba-aaaki.md
  - id: digital-life-khazix
    priority: P1
    focus_topics: [China AI ecosystem, model dynamics, market pulse]
    profile_path: /home/cuongpt/Workspaces/openclaw-agents-persona/research-assistant/references/sources/digital-life-khazix.md
    snapshot_path: /home/cuongpt/Workspaces/openclaw-agents-persona/research-assistant/references/source-snapshots/digital-life-khazix.md
  - id: goofy-ai-business
    priority: P1
    focus_topics: [AI business model, enterprise deployment, monetization]
    profile_path: /home/cuongpt/Workspaces/openclaw-agents-persona/research-assistant/references/sources/goofy-ai-business.md
    snapshot_path: /home/cuongpt/Workspaces/openclaw-agents-persona/research-assistant/references/source-snapshots/goofy-ai-business.md
  - id: datafuntalk-huang-jia
    priority: P1
    focus_topics: [industry AI, finance, retail, medical deployment]
    profile_path: /home/cuongpt/Workspaces/openclaw-agents-persona/research-assistant/references/sources/datafuntalk-huang-jia.md
    snapshot_path: /home/cuongpt/Workspaces/openclaw-agents-persona/research-assistant/references/source-snapshots/datafuntalk-huang-jia.md
```
