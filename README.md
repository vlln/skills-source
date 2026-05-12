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
| `biocontainers` | Search BioContainers, inspect container metadata, resolve quay.io image tags via GA4GH TRS API |
| `paperutils` | Fetch paper dossiers, search papers, explain dataset accessions via Crossref, Europe PMC, PubMed, arXiv |
| `quay` | Search Quay.io repositories, list image tags, resolve pullable container references |
| `image-mirror-skill` | Accelerate Docker/OCI image pulls with registry-aware mirror rewrite via mip CLI |
| `remote-exec` | Run repeated shell commands on remote machines over SSH with tmux-backed persistent state |

## Adding a skill

1. Install the skill in your local skit project: `skit install <source>`
2. Export the manifest: `skit export`
3. Merge the new entry into this repo's `skit.json`
4. Commit and push