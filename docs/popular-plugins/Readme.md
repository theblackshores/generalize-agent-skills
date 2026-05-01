# Popular Plugins (Skills/MCP's)

Tested on Copilot CLI.

Project scope MCP's, `$PROJECT/.mcp.json`:
```json
{
  "mcpServers": {
    "XXX": {},
  }
}
```

> Notes: Detailed configuration can usually be found in the official MCP documentation.

## superpowers
https://github.com/obra/superpowers

Includes test-driven development, debugging, collaboration models, and mature technologies.

```bash
/plugin marketplace add obra/superpowers-marketplace
/plugin install superpowers@superpowers-marketplace
```

## andrej-karpathy-skills
https://github.com/forrestchang/andrej-karpathy-skills 

Improving the behavior of the Agent Coding Tool stems from Andrej Karpathy's observations and summary of LLM coding pitfalls.

```bash
/plugin marketplace add forrestchang/andrej-karpathy-skills
/plugin install andrej-karpathy-skills@karpathy-skills
```

## chrome-devtools-mcp
https://github.com/ChromeDevTools/chrome-devtools-mcp

The official DevTools MCP released by the Google Chrome team.

```bash
/mcp add chrome-devtools
# Type: local
# Command: npx -y chrome-devtools-mcp@latest --no-usage-statistics
```

If you have multiple Chrome installations, you can specify it: `--executable-path`

## context7
https://context7.com/docs/resources/all-clients

Get the latest documentation and code into Cursor, Claude, or other LLMs.

> Notes: Context7 can run without an API key; registered users can obtain higher rate limits.

```bash
/mcp add context7
# Type: local
# Command: npx -y @upstash/context7-mcp
```

If you have an API key, you can specify it: `--api-key`

## document-skills
https://github.com/anthropics/skills

Skills include pdf/pptx/xlsx/docx editing, front-end design, poster design, etc.

> Notes: Some of these skills are Claude only.

```bash
/plugin marketplace add anthropics/skills
/plugin install document-skills@anthropic-agent-skills
```

## logo-generator-skill
https://github.com/op7418/logo-generator-skill

An SVG logo generator with a preview function.

```bash
npx skills add https://github.com/op7418/logo-generator-skill.git
```
