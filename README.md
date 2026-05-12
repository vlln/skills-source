# skills-source

Skit skill source — a curated collection of bioinformatics and DevOps skills installable via [skit](https://github.com/vlln/skit).

## Usage

```bash
skit source add skills-source https://raw.githubusercontent.com/vlln/skills-source/main/skit.json
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

## Adding a skill

1. Install the skill in your local skit project: `skit install <source>`
2. Export the manifest: `skit export`
3. Merge the new entry into this repo's `skit.json`
4. Commit and push