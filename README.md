# skills-source

A curated collection of agent skills — bioinformatics, document processing, DevOps, and more — maintained by [vlln](https://github.com/vlln).

## Install with skit (recommended)

[skit](https://github.com/vlln/skit) is a fast, reproducible skill manager for agent ecosystems. Install it then add this source:

```bash
# Install skit
go install github.com/vlln/skit/cmd/skit@latest

# Add this source
skit source add skills-source https://raw.githubusercontent.com/vlln/skills-source/main/skit.json

# Search and install
skit search <keyword>
skit install skills-source/<skill-name>
```

## Available skills

| Skill | Description |
|---|---|
| [`biocontainers`](https://github.com/vlln/bio-skills) | Search BioContainers, inspect container metadata, resolve quay.io image tags via GA4GH TRS API |
| [`zenodo`](https://github.com/vlln/bio-skills) | Search, download, and manage authenticated Zenodo deposits via the Zenodo API |
| [`bio-reproducer`](https://github.com/vlln/bio-skills) | Guide agents through reproducible bioinformatics paper reproduction with Nextflow |
| [`paperutils`](https://github.com/vlln/paperutils) | Fetch paper dossiers, search papers, explain dataset accessions via Crossref, Europe PMC, PubMed, arXiv |
| [`quay`](https://github.com/vlln/quay-skill) | Search Quay.io repositories, list image tags, resolve pullable container references |
| [`image-mirror-skill`](https://github.com/vlln/mip) | Accelerate Docker/OCI image pulls with registry-aware mirror rewrite via mip CLI |
| [`remote-exec`](https://github.com/vlln/remote-exec-skill) | Run repeated shell commands on remote machines over SSH with tmux-backed persistent state |
| [`mineru-api`](https://github.com/vlln/mineru-api-skill) | Parse PDFs via remote MinerU API — extract markdown, tables, and formulas from documents |
| [`pdffigures2`](https://github.com/vlln/pdffigures-mcp-server) | Extract figures, tables, and captions from scholarly PDFs using PDFFigures 2.0 (Allen AI) |
| [`make-skill`](https://github.com/vlln/skit) | Create or revise Agent Skills repositories with precise SKILL.md frontmatter and validation |
| [`search-skills`](https://github.com/vlln/skit) | Find, evaluate, and install agent skills with the skit CLI |

## Alternative install methods

### skills.sh

```bash
skills add https://raw.githubusercontent.com/vlln/skills-source/main/skit.json
skills install <skill-name>
```

### Agent self-install

Give your agent a skill URL directly — it can read the `skit.json` catalog and install the skill from its source repository on its own:

> Install the skill from `https://github.com/vlln/bio-skills/tree/main/skills/biocontainers`

### Install from source

```bash
git clone https://github.com/vlln/bio-skills.git
skit install ./bio-skills/skills/biocontainers
```

## Adding a skill

1. Install the skill in your local skit project: `skit install <source>`
2. Export the manifest: `skit export`
3. Merge the new entry into this repo's `skit.json`
4. Commit and push