# skills-source

A curated collection of agent skills — bioinformatics, document processing, DevOps, and more — maintained by [vlln](https://github.com/vlln).

## Install with skit (recommended)

[skit](https://github.com/vlln/skit) is a fast, reproducible skill manager for agent ecosystems. Install it then add this source:

```bash
# Install skit
curl -fsSL https://raw.githubusercontent.com/vlln/skit/main/install.sh | sh

# Add this source
skit source add skills-source https://raw.githubusercontent.com/vlln/skills-source/main/skit.json

# Search and install
skit search <keyword>
skit install skills-source/<skill-name>
```

## Available skills

### Agent & Workflow

| Skill | Description |
|---|---|
| [`make-skill`](https://github.com/vlln/skit) | Create or revise Agent Skills repositories with precise SKILL.md frontmatter and validation |
| [`search-skills`](https://github.com/vlln/skit) | Find, evaluate, and install agent skills with the skit CLI |
| [`subagents`](https://github.com/vlln/subagents-skill) | Dispatch tasks to named agent sessions across multiple backends for parallel execution |
| [`workflow`](https://github.com/vlln/subagents-skill) | Orchestrate multiple AI agents with parallel, pipeline, or phase-based workflows |

### Bioinformatics

| Skill | Description |
|---|---|
| [`biocontainers`](https://github.com/vlln/bio-skills) | Search BioContainers, inspect container metadata, resolve quay.io image tags via GA4GH TRS API |
| [`bio-reproducer`](https://github.com/vlln/bio-skills) | 引导 agent 通过分阶段报告、Nextflow 编排和验证，完成可复现的生物信息学论文复现 |
| [`paperutils`](https://github.com/vlln/paperutils) | Fetch paper dossiers, search papers, explain dataset accessions via Crossref, Europe PMC, PubMed, arXiv |
| [`pdffigures2`](https://github.com/vlln/pdffigures-mcp-server) | Extract figures, tables, and captions from scholarly PDFs using PDFFigures 2.0 (Allen AI) |
| [`zenodo`](https://github.com/vlln/bio-skills) | Search, download, and manage authenticated Zenodo deposits via the Zenodo API |

### DevOps

| Skill | Description |
|---|---|
| [`clashctl-usage`](https://github.com/vlln/clashskill) | 使用 clashctl 工具管理 Linux 代理 — 代理开关、节点切换、订阅管理、规则配置、网络诊断 |
| [`image-mirror-skill`](https://github.com/vlln/mip) | Accelerate Docker/OCI image pulls with registry-aware mirror rewrite via mip CLI |
| [`quay`](https://github.com/vlln/quay-skill) | Search Quay.io repositories, list image tags, resolve pullable container references |
| [`remote-exec`](https://github.com/vlln/remote-exec-skill) | Run repeated shell commands on remote machines over SSH with tmux-backed persistent state |

### Documents & Media

| Skill | Description |
|---|---|
| [`autofigure`](https://github.com/vlln/autofigure-skill) | Create publication-ready scientific SVG figures for flowcharts, architecture diagrams, methodology overviews |
| [`mineru-api`](https://github.com/vlln/mineru-api-skill) | Parse PDFs via remote MinerU API — extract markdown, tables, and formulas from documents |

### Web & UI

| Skill | Description |
|---|---|
| [`agent-gui`](https://github.com/vlln/agent-gui) | Generate interactive HTML UIs — dashboards, task boards, forms, charts, CRUD interfaces, mini-games, data explorers |
| [`grab`](https://github.com/vlln/grab) | Fetch web resources through TLS fingerprint rotation and browser fallback — bypass Cloudflare and CDN blocking |

## Alternative install methods

### skills.sh

```bash
skills add https://raw.githubusercontent.com/vlln/skills-source/main/skit.json
skills install <skill-name>
```

### Agent self-install

Give your agent a skill URL directly — it can read the `skit.json` catalog and install the skill from its source repository on its own:

> Install the skill from `https://github.com/vlln/bio-skills/tree/main/skills/biocontainers`

## Adding a skill

1. Install the skill in your local skit project: `skit install <source>`
2. Export the manifest: `skit export`
3. Merge the new entry into this repo's `skit.json`
4. Commit and push
