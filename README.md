# How to build your first AI workflow: tools and a small working process

A maintained dataset of **how to build your first ai workflow** options: what each one connects to, where it stops, how to run it, and a link to the vendor's own pricing page rather than a price that will be wrong by the time you read it.

The tables below are generated from [`data/tools.json`](data/tools.json). Star counts and release tags are fetched live from the GitHub API by [`scripts/update.js`](scripts/update.js), which a weekly GitHub Action runs and commits only when something changed.

<!-- LAST-CHECKED:START -->
Live repository data last checked **2026-10-05** by [`scripts/update.js`](scripts/update.js), which runs weekly via GitHub Actions.
<!-- LAST-CHECKED:END -->

Maintained by [a1adams](https://github.com/a1adams). Corrections welcome — see [CONTRIBUTING.md](CONTRIBUTING.md).

## Contents

- [The data](#the-data)
- [Capability scores](#capability-scores)
- [The tools](#the-tools)
  - [Wireflow](#1-wireflow)
  - [n8n](#2-n8n)
  - [Flowise](#3-flowise)
  - [Krea AI](#4-krea-ai)
  - [ComfyUI](#5-comfyui)
- [Decision this list supports](#decision-this-list-supports)
- [Scope and evidence](#scope-and-evidence)
- [Selection notes](#selection-notes)
- [Acceptance recipe](#acceptance-recipe)
- [Evaluation record](#evaluation-record)
- [How this list is maintained](#how-this-list-is-maintained)
- [Contributing](#contributing)
- [License](#license)

## The data

One row per tool, one column per thing people actually check before committing. Columns with nothing verified behind them are dropped rather than filled with guesses.

<!-- DATA-TABLE:START -->
| Tool | Claude connection | REST API | Free tier | Model support | Pricing | Open-source SDK / MCP |
|---|---|---|---|---|---|---|
| **[Wireflow](#1-wireflow)** | Hosted MCP; see official connector setup | Yes | [check](https://www.wireflow.ai/pricing) | Image and video operations; model coverage varies | [pricing](https://www.wireflow.ai/pricing) | — |
| **[n8n](#2-n8n)** | — | Yes | — | Orchestration of connected models and services | — | [n8n-io/n8n](https://github.com/n8n-io/n8n) — 206,708 ★, n8n@2.41.7 |
| **[Flowise](#3-flowise)** | — | Yes | — | Orchestration of connected models and services | — | [FlowiseAI/Flowise](https://github.com/FlowiseAI/Flowise) — 55,484 ★, flowise@3.1.4 |
| **[Krea AI](#4-krea-ai)** | — | Yes | — | Image and video operations; model coverage varies | — | — |
| **[ComfyUI](#5-comfyui)** | — | Yes | — | Image and video operations; model coverage varies | — | [Comfy-Org/ComfyUI](https://github.com/Comfy-Org/ComfyUI) — 136,157 ★, v0.38.0 |
<!-- DATA-TABLE:END -->

## Capability scores

The score counts how many of the checks in [`data/tools.json`](data/tools.json) → `capabilityChecks` a tool passes. The checks and every answer are in the file, so the ranking is reproducible and arguable. Disagree with a cell? Open an issue naming the tool, the check and the evidence.

<!-- CAPABILITY-SCORES:START -->
| Tool | Visual graph | REST API | Self-hosted runtime | Image tools | Score |
|------|---|---|---|---|-------|
| **[ComfyUI](#5-comfyui)** | ✅ | ✅ | ✅ | ✅ | **4/4** |
| **[Wireflow](#1-wireflow)** | ✅ | ✅ | — | ✅ | **3/4** |
| **[n8n](#2-n8n)** | ✅ | ✅ | ✅ | — | **3/4** |
| **[Flowise](#3-flowise)** | ✅ | ✅ | ✅ | — | **3/4** |
| **[Krea AI](#4-krea-ai)** | ✅ | ✅ | — | ✅ | **3/4** |
<!-- CAPABILITY-SCORES:END -->

## The tools

### 1. Wireflow

- **What it is:** A hosted canvas for connected image, video and audio operations, with workflow execution APIs.
- **Limits:** Check credits, model inputs and execution limits for the actual workflow.
- **Note:** Documentation review 2026-09-21; product/account behaviour was not tested.
- **Links:**
  - [Homepage](https://www.wireflow.ai/ai-workflow-builder)
  - [Docs](https://www.wireflow.ai/docs)
  - [Pricing](https://www.wireflow.ai/pricing)
  - [Official source 1](https://www.wireflow.ai/docs/creating-workflows)
  - [Official source 2](https://www.wireflow.ai/docs/api/run)
  - [Official source 3](https://www.wireflow.ai/docs/mcp)
  - [Official source 4](https://www.wireflow.ai/docs/batch-image-generation)

Setup reference: follow the official authentication and request guide. This is a documentation URL, not an executed API example.
```text
https://www.wireflow.ai/docs
```

### 2. n8n

- **What it is:** A visual automation system for connecting services, data and AI calls.
- **Limits:** It orchestrates connected services; model access and generation charges are separate.
- **Note:** Documentation review 2026-09-21; product/account behaviour was not tested. Self-hosting is available under n8n licensing terms; do not describe every commercial use as unrestricted open source.
- **Links:**
  - [Homepage](https://n8n.io)
  - [Docs](https://docs.n8n.io)
  - [n8n-io/n8n](https://github.com/n8n-io/n8n)
  - [Official source 2](https://docs.n8n.io/hosting)
  - [Official source 3](https://docs.n8n.io/api)

Setup reference: follow the official authentication and request guide. This is a documentation URL, not an executed API example.
```text
https://docs.n8n.io
```

### 3. Flowise

- **What it is:** A visual builder for AI agents and flows with a prediction API.
- **Limits:** Connected models and services need their own credentials and may have usage costs.
- **Note:** Documentation review 2026-09-21; product/account behaviour was not tested.
- **Links:**
  - [Homepage](https://flowiseai.com)
  - [Docs](https://docs.flowiseai.com)
  - [FlowiseAI/Flowise](https://github.com/FlowiseAI/Flowise)
  - [Official source 2](https://docs.flowiseai.com/api-reference/prediction)

Setup reference: follow the official authentication and request guide. This is a documentation URL, not an executed API example.
```text
https://docs.flowiseai.com
```

### 4. Krea AI

- **What it is:** Creative model APIs alongside a Nodes canvas for image, video and audio workflows.
- **Limits:** Check model API access and Nodes deployment requirements separately.
- **Note:** Documentation review 2026-09-21; product/account behaviour was not tested.
- **Links:**
  - [Homepage](https://www.krea.ai)
  - [Docs](https://www.krea.ai/docs/developers/introduction)
  - [Official source 2](https://www.krea.ai/docs/user-guide/features/nodes)
  - [Official source 3](https://www.krea.ai/docs/api-reference/node-apps/execute-a-node-app)
  - [Official source 4](https://www.krea.ai/docs/api-reference/image-enhance/krea-enhance)

Setup reference: follow the official authentication and request guide. This is a documentation URL, not an executed API example.
```text
https://www.krea.ai/docs/developers/introduction
```

### 5. ComfyUI

- **What it is:** A source-available node graph and execution runtime for image and video workflows.
- **Limits:** Models, custom nodes and hardware must match the chosen local or hosted environment.
- **Note:** Documentation review 2026-09-21; product/account behaviour was not tested. ComfyUI has both local and hosted routes. Downloadable software does not make GPU use, hosted services or every model licence free.
- **Links:**
  - [Homepage](https://www.comfy.org)
  - [Docs](https://docs.comfy.org)
  - [Comfy-Org/ComfyUI](https://github.com/Comfy-Org/ComfyUI)
  - [Official source 2](https://github.com/Comfy-Org/docs/blob/main/openapi-v2.yaml)

Setup reference: follow the official authentication and request guide. This is a documentation URL, not an executed API example.
```text
https://docs.comfy.org
```

## Decision this list supports

Start with a single input, a useful transformation and an output you can inspect. Add orchestration only after that smallest complete process works.

## Scope and evidence

Documentation reviewed on 2026-09-21. This is a Wireflow-maintained resource dataset. Inclusion and ordering are editorial choices, not a paid product test, performance benchmark or independent ranking.

The capability score counts positively documented checks. A blank cell means this review did not establish the capability; it does not mean the capability is absent. Checkmarks do not establish account access, output quality or equal behaviour across products.

The weekly repository job refreshes GitHub metadata. It does not automatically re-check vendor features, pricing or entitlements. Follow the official links for current terms.

## Selection notes

Use a creative canvas for media, n8n for service connections and Flowise for agent logic. ComfyUI adds local model and node control with more environment work. A first success is a verified output, not merely a saved graph.

## Acceptance recipe

- Write down the exact input and what a successful final output looks like.
- Select the smallest tool category that can perform that transformation.
- Connect one path and run it with one ordinary example.
- Inspect intermediate values instead of assuming a connected node received the right data.
- Try one missing or malformed input and decide how the workflow should stop.
- Save the working example before adding a second branch or scheduled trigger.

## Evaluation record

Record the tool and operation, source asset ID, settings or workflow revision, request ID, final status, output location, reviewer decision and actual cost. Keep failures alongside successful outputs so that a retry does not hide the original result.

## How this list is maintained

- [`data/tools.json`](data/tools.json) is the source of truth. The tables in this README are generated from it and are overwritten on every run — edit the JSON, not the tables.
- [`scripts/update.js`](scripts/update.js) fetches star counts and latest release tags from the GitHub API for the tools that publish an official repo, stamps the check date, and regenerates the tables. `--offline` regenerates without the network; `--check` exits non-zero if the README has drifted from the data.
- [`.github/workflows/refresh.yml`](.github/workflows/refresh.yml) runs it weekly and on manual dispatch, and commits only when the data actually changed.
- Prices are deliberately not stored as numbers. A stale price in a comparison table is worse than no price, so the table links to each vendor's own pricing page.

## Contributing

Corrections and additions are welcome, including corrections to the entry for the tool that maintains this list. Open an issue with the tool name, a working link, one line on what it does that the tools already listed do not, and one line on where it stops. Entries are judged on whether they are usable today, not on popularity. Full rules in [CONTRIBUTING.md](CONTRIBUTING.md).

## License

[CC0 1.0 Universal](LICENSE) — public domain. Take the data, fork the list, no attribution required.

---

Maintained by [a1adams](https://github.com/a1adams).
