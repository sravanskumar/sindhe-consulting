# Sindhe | Digital & Brand Consulting — website

Static marketing site for **Sravan Kumar Sindhe** (Munich) — architecture-quality digital and MarTech delivery for SMEs.

**Live:** https://sravanskumar.github.io/sindhe-consulting/

## Repository contents

| Path | Purpose |
|------|---------|
| `index.html` | Full site (HTML + CSS + minimal JS) |
| `assets/` | Profile images and static media |
| `AGENTS.md` | Context for Cursor and other coding agents |
| `llms.txt` | Short public summary for LLM crawlers |

## Local preview

```bash
python3 -m http.server 8080
# open http://localhost:8080
```

## Deploy

Push to `main` on GitHub; Pages serves from root (no `/docs` folder).

## Agent / Cursor

Read **[AGENTS.md](AGENTS.md)** before editing. Cursor rule: `.cursor/rules/sindhe-consulting-site.mdc`.
