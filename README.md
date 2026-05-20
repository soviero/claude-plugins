# Eesier for Claude Code

> You ship product. Eesier ships customers.

A Claude Code plugin that gives your AI agent a full-time **Sales Development Rep**. Describe your business once, then let Claude:

- 🔎 **Find** B2B prospects matching your ICP
- ✉️ **Write** a personalized cold email to each one
- 🔁 **Follow up** automatically until they reply or unsubscribe
- 💬 **Route replies** back to you, with full context
- 📊 **Report** on what's working — by campaign, message type, and industry

All from your terminal. 24/7. Powered by [Eesier](https://eesier.com).

---

## Install

```bash
/plugin marketplace add soviero/claude-plugins
/plugin install eesier@eesier
```

## Connect your account

1. Go to your Eesier console → **Account** page → **External Agents (MCP)** → **Generate Token**.
2. Set the token as an environment variable:
   - **Windows (PowerShell):** `[Environment]::SetEnvironmentVariable("EESIER_MCP_TOKEN", "<TOKEN>", "User")`
   - **macOS / Linux:** add `export EESIER_MCP_TOKEN="<TOKEN>"` to your `~/.zshrc` or `~/.bashrc`
3. **Restart Claude Code.**
4. Try: *"Run a status check on my prospecting account."*

If you don't have an Eesier account yet, register at [eesier.com](https://eesier.com).

## What you can ask Claude

Once connected, the agent has 49 tools at its disposal. Talk to it like a sales assistant:

- *"Onboard me — I run a B2B SaaS for HR teams in Brazil."*
- *"How many leads did we send last week? What's the reply rate?"*
- *"Show me my interested leads — group by campaign."*
- *"Pause the 'Enterprise' campaign and bump up follow-up frequency on 'SMB'."*
- *"This lead is hot — let me take it over. Email them now with this message."*
- *"What's changed in my account since I last logged in (3 weeks ago)?"*

The plugin bundles an operator skill that teaches Claude how to use each tool correctly — onboarding flow, campaign vocabulary, lead-status semantics, takeover triggers, human-review handling, and more.

## What's inside

```
eesier-claude-plugin/
└── plugins/eesier/
    ├── .claude-plugin/plugin.json   # plugin manifest
    ├── .mcp.json                    # registers https://mcp.eesier.com
    └── skills/eesier/SKILL.md       # operator guide (autoloaded)
```

The MCP server is hosted by Eesier at `https://mcp.eesier.com`. Your token is the only secret — never committed, never logged. Plugin code itself contains zero credentials.

## Pricing & data

- Eesier itself is a paid SaaS — see [eesier.com](https://eesier.com) for plans.
- The plugin is free.
- Leads come from publicly available data with LGPD-aligned safeguards.

## Support

- Product questions: ask Claude with the plugin installed — it queries the Eesier knowledge base directly.
- Plugin bugs: open an issue on this repo.
- Direct contact: [rodrigo@eesier.com](mailto:rodrigo@eesier.com)

## License

MIT — see [LICENSE](LICENSE).
