## 台灣股市設定（優先套用）
- 所有分析預設以台股為主，幣別為新台幣（TWD）
- 歷史資料與財報優先使用 FinMind API
- 即時當日資料使用台灣證交所 OpenAPI
- 估值習慣：本益比、殖利率、股價淨值比
- 技術分析：週KD搭配均線系統為主
- 所有報告結尾須附上投資風險聲明
- 法規遵循台灣金管會規範

# Financial Services Plugins

This is a marketplace of Claude Cowork plugins for financial services professionals. Each subdirectory is a standalone plugin.

## Repository Structure

```
├── investment-banking/  # Investment banking productivity
```

## Plugin Structure

Each plugin follows this layout:
```
plugin-name/
├── .claude-plugin/plugin.json   # Plugin manifest (name, description, version)
├── commands/                    # Slash commands (.md files)
├── skills/                      # Knowledge files for specific tasks
├── hooks/                       # Event-driven automation
├── mcp/                         # MCP server integrations
└── .claude/                     # User settings (*.local.md)
```

## Key Files

- `marketplace.json`: Marketplace manifest - registers all plugins with source paths
- `plugin.json`: Plugin metadata - name, description, version, and component discovery settings
- `commands/*.md`: Slash commands invoked as `/plugin:command-name`
- `skills/*/SKILL.md`: Detailed knowledge and workflows for specific tasks
- `*.local.md`: User-specific configuration (gitignored)
- `mcp-categories.json`: Canonical MCP category definitions shared across plugins

## Development Workflow

1. Edit markdown files directly - changes take effect immediately
2. Test commands with `/plugin:command-name` syntax
3. Skills are invoked automatically when their trigger conditions match
