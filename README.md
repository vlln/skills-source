<h1 align="center">skills-source</h1>

<p align="center">
  <strong>A curated collection of 18 agent skills.</strong><br/>
  Bioinformatics, document processing, DevOps, agent orchestration, and more —<br/>
  one source, one command, all skills.
</p>

<p align="center">
  <a href="https://github.com/vlln/skills-source/stargazers"><img src="https://badgen.net/github/stars/vlln/skills-source?label=%E2%98%85" alt="GitHub stars" /></a>
  <img src="https://badgen.net/badge/license/MIT/blue" alt="MIT" />
  <img src="https://badgen.net/badge/spec/Agent%20Skills/8257D0" alt="Agent Skills spec" />
  <img src="https://badgen.net/badge/skills/18/44CC11" alt="18 skills" />
</p>

---

## Installation

### [skit](https://github.com/vlln/skit) (Recommended)

```bash
# Add this source
skit source add skills-source https://raw.githubusercontent.com/vlln/skills-source/main/skit.json

# Search and install
skit search <keyword>
skit install skills-source/<skill-name>
```

### [skill.sh](https://github.com/vercel-labs/skills)

```bash
npx skills add vlln/skills-source
```

### Manually

Give your agent a skill URL directly:

> Install the skill from `https://github.com/vlln/bio-skills/tree/main/skills/biocontainers`

---

## Skills

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
| [`bio-reproducer`](https://github.com/vlln/bio-skills) | Guide agents through reproducible bioinformatics paper reproduction with phased reports, Nextflow orchestration, and validation |
| [`paperutils`](https://github.com/vlln/paperutils) | Fetch paper dossiers, search papers, explain dataset accessions via Crossref, Europe PMC, PubMed, arXiv |
| [`pdffigures2`](https://github.com/vlln/pdffigures-mcp-server) | Extract figures, tables, and captions from scholarly PDFs using PDFFigures 2.0 (Allen AI) |
| [`zenodo`](https://github.com/vlln/bio-skills) | Search, download, and manage authenticated Zenodo deposits via the Zenodo API |

### DevOps

| Skill | Description |
|---|---|
| [`clashctl-usage`](https://github.com/vlln/clashskill) | Manage Linux proxy agents with clashctl — proxy switching, node selection, subscription management, rule configuration, network diagnostics |
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

---

## Adding a skill

1. Install the skill in your local skit project: `skit install <source>`
2. Export the manifest: `skit export`
3. Merge the new entry into this repo's `skit.json`
4. Commit and push

## License

MIT