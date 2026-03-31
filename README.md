# Awesome Claude Code

A curated list of resources, tools, templates, and tips for Claude Code.

Contributions welcome — see [Contributing](#contributing).

---

## Contents

- [Official Resources](#official-resources)
- [CLAUDE.md Templates](#claudemd-templates)
- [MCP Servers](#mcp-servers)
- [Hooks](#hooks)
- [Chrome Extensions](#chrome-extensions)
- [Tips and Tricks](#tips-and-tricks)
- [Keyboard Shortcuts](#keyboard-shortcuts)
- [Articles and Tutorials](#articles-and-tutorials)
- [Community](#community)

---

## Official Resources

- [Claude Code Documentation](https://docs.anthropic.com/en/docs/claude-code) — Official docs
- [Model Context Protocol](https://modelcontextprotocol.io/) — MCP specification and guides
- [Claude Code GitHub](https://github.com/anthropics/claude-code) — Issue tracker and discussions

## CLAUDE.md Templates

- [CLAUDE.md Starter Template](https://github.com/NyxToolsDev/claude-md-starter) — Free general-purpose template for any project
- [CLAUDE.md Pro Pack](https://nyxtools.lemonsqueezy.com) — 15+ stack-specific templates (React, FastAPI, Go, healthcare IT, DevOps) with rule files and prompt patterns

### Community CLAUDE.md Examples

> Know a great public CLAUDE.md? Open a PR to add it here.

## MCP Servers

### Productivity
- [Calendly MCP Server](https://github.com/NyxToolsDev/calendly-mcp-server) — Manage Calendly from Claude (scheduling, availability, follow-ups)

### Finance
- [QuickBooks MCP Server](https://github.com/NyxToolsDev/quickbooks-mcp-server) — Query QuickBooks in plain English (P&L, invoices, expenses)

### Healthcare
- [DICOM/HL7 MCP Server](https://github.com/NyxToolsDev/dicom-hl7-mcp-server) — Healthcare interoperability (DICOM queries, HL7 parsing, FHIR)

### Developer Tools
- [Claude Memory Manager](https://github.com/NyxToolsDev/claude-memory-manager) — Cross-session memory with semantic search

### Build Your Own
- [MCP Server Template](https://github.com/NyxToolsDev/mcp-server-template) — Boilerplate for building Python MCP servers in 30 minutes

### MCP Registries

Find more MCP servers:
- [Official MCP Registry](https://registry.modelcontextprotocol.io/)
- [mcp.so](https://mcp.so)
- [PulseMCP](https://pulsemcp.com)
- [MCP Market](https://mcpmarket.com)

## Hooks

Claude Code hooks run shell commands automatically before/after Claude performs actions.

### Free Hook: Auto-Lint on Save

Add to your Claude Code settings to auto-lint after every file edit:

```json
{
  "hooks": {
    "PostToolUse": [
      {
        "matcher": "Edit|Write",
        "command": "npx eslint --fix $CLAUDE_FILE_PATH 2>/dev/null || true"
      }
    ]
  }
}
```

### More Hooks
- [Claude Code Hooks Library](https://nyxtools.lemonsqueezy.com) — 20+ pre-built hooks for testing, security, cost tracking, and more

## Chrome Extensions

- Claude Power Tools — Session manager, prompt library, and shortcuts for Claude.ai *(coming soon)*
- AI Chat Vault — Cross-platform AI conversation backup and search *(coming soon)*

## Tips and Tricks

### Get Better Output
1. **Use a CLAUDE.md file.** Even a basic one dramatically improves output quality.
2. **Use `.claude/rules/` for contextual rules.** Security rules when touching auth. Testing rules when writing tests. They load only when relevant.
3. **Be specific in negative constraints.** "Never use enum" > "Follow TypeScript best practices."
4. **Start with Plan mode for complex tasks.** Hit `Shift+Tab` to cycle to Plan mode before diving into implementation.

### Save Money
1. Use `/cost` to check current session spend
2. Use `/clear` to reset context when Claude gets confused (avoids wasting tokens going in circles)
3. Keep CLAUDE.md concise — every line is tokens you pay for every message
4. Use Plan mode first for complex tasks to avoid expensive re-dos

### Work Faster
1. `Shift+Tab` — Cycle between Ask, Edit, and Plan modes
2. `Ctrl+G` — Edit your last prompt without retyping
3. `Esc` — Stop Claude mid-response
4. `Tab` — Accept Claude's suggestion
5. `/clear` — Reset context when things go sideways

## Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `Shift+Tab` | Cycle modes (Ask → Edit → Plan) |
| `Ctrl+G` | Edit last prompt |
| `Esc` | Stop current response |
| `Tab` | Accept suggestion |
| `Ctrl+C` (x2) | Exit Claude Code |
| `/cost` | Check session spend |
| `/clear` | Reset conversation context |
| `/help` | Show available commands |

## Articles and Tutorials

> Know a great article about Claude Code? Open a PR to add it here.

## Community

- [r/ClaudeAI](https://reddit.com/r/ClaudeAI) — Main Claude community on Reddit
- [r/ClaudeCode](https://reddit.com/r/ClaudeCode) — Claude Code specific discussions
- [Claude Code GitHub Issues](https://github.com/anthropics/claude-code/issues) — Bug reports and feature requests

---

## Contributing

1. Fork this repo
2. Add your resource to the appropriate section
3. Open a PR with a brief description of what you're adding

Guidelines:
- Only add resources you've personally used or verified
- Include a one-line description
- Keep descriptions factual, not promotional
- Free resources preferred; paid resources must be clearly marked

---

## License

MIT — see [LICENSE](LICENSE)

---

**Maintained by [NyxTools](https://github.com/NyxToolsDev)** · NyxTools
