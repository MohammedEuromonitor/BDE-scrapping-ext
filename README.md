# bde-scraper plugin

Lets Claude write, run and check web-scraping robots with the BDE scraper. The plugin has two parts:

- **MCP server** (`mcp-server.js`, started with the bundled `runtime/node.exe`): tools `save_robot`, `run_robot`, `get_status`, `get_failed_urls`, `get_qc_results`, `get_results`, `export_table_csv`, `list_robots`, `stop_run`, `probe_url`.
- **Skill** (`skills/bde-scraper/SKILL.md`): the rules Claude follows (permission check, engine order, QC rules, verdict and report format).

## Try it locally

    claude --plugin-dir "<path to this folder>"

Robots are saved in `robots/` and run output goes to `output/` inside this folder. Copy `.env.example` to `.env` if you need to change run settings.

## Notes

- The skill is also kept in the `bde-code` repo (`.claude/skills/bde-scraper/SKILL.md`). The two copies are separate; update both when the rules change.
- `manifest.json` is the Claude Desktop extension manifest for the same server. It is not used by the plugin.
- If the plugin is installed through a marketplace, a plugin update replaces this folder, so robots and output saved inside it would be lost. Copy anything you want to keep first.
# BDE-scrapping-ext
