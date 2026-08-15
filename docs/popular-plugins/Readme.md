# Popular Plugins (Skills/MCP's)

> Notes: Only tested on Copilot CLI.

Project scope MCP is well-suited for enhancing document-type contexts.

`$PROJECT/.mcp.json` example:
```json
{
  "mcpServers": {
    "patternfly-docs": {
      "command": "npx",
      "args": ["-y", "@patternfly/patternfly-mcp@latest"]
    },
    "mui-mcp": {
      "command": "npx",
      "args": ["-y", "@mui/mcp@latest"]
    },
    "better-auth": {
      "type": "http",
      "url": "https://mcp.better-auth.com/mcp"
    }
  }
}
```

> Notes: Detailed configuration can usually be found in the official MCP documentation.

## Category: Knowledge

Add context to Agent Coding Tool.

### context7
https://context7.com/docs/resources/all-clients

Get the latest documentation and code into Cursor, Claude, or other LLMs.

> Notes: Context7 can run without an API key; registered users can obtain higher rate limits.
> Alternatively, you can manually add the document-type MCP/Skills for each library.

```bash
/mcp add context7
# Type: Local
# Command: npx -y @upstash/context7-mcp
```

If you have an API key, you can specify it: `--api-key`

## Category: Thinking and Workflow

### superpowers
https://github.com/obra/superpowers

Includes test-driven development, debugging, collaboration models, and mature technologies.

| Fixed Scope | Prompt (Keyword)                  |
| ----------- | --------------------------------- |
| Global      | brainstorm / superpowers workflow |

```bash
/plugin marketplace add obra/superpowers-marketplace
/plugin install superpowers@superpowers-marketplace
```

### andrej-karpathy-skills
https://github.com/forrestchang/andrej-karpathy-skills 

Improving the behavior of the Agent Coding Tool stems from Andrej Karpathy's observations and summary of LLM coding pitfalls.

```bash
/plugin marketplace add forrestchang/andrej-karpathy-skills
/plugin install andrej-karpathy-skills@karpathy-skills
```

## Category: Capability

### chrome-devtools-mcp
https://github.com/ChromeDevTools/chrome-devtools-mcp

The official DevTools MCP released by the Google Chrome team.

| Fixed Scope | Prompt (Keyword)                       |
| ----------- | -------------------------------------- |
| Global      | using chrome-devtools to control browser ... |

```bash
/mcp add chrome-devtools
# Type: local
# Command: npx -y chrome-devtools-mcp@latest --no-usage-statistics
```

If you have multiple Chrome installations, you can specify it: `--executable-path`

### document-skills
https://github.com/anthropics/skills

Skills include pdf/pptx/xlsx/docx editing, front-end design, poster design, etc.

> Notes: Some of these skills are Claude only.

| Fixed Scope | Prompt (Keyword)            |
| ----------- | --------------------------- |
| Global      | front-end / read pdf / etc. |

```bash
/plugin marketplace add anthropics/skills
/plugin install document-skills@anthropic-agent-skills
```

### lsp-setup
https://docs.github.com/en/copilot/how-tos/copilot-cli/set-up-copilot-cli/add-lsp-servers

Automatically find the appropriate language server.

> Notes: Deeply integrated with Copilot CLI

| Recommended Scope | Prompt (Keyword) |
| ----------------- | ---------------- |
| Global            | setup lsp        |

```bash
npx skills add -g github/awesome-copilot@lsp-setup
```

### logo-generator-skill
https://github.com/op7418/logo-generator-skill

An SVG logo generator with a preview function.

| Recommended Scope | Prompts (Keyword) |
| ----------------- | ----------------- |
| Global            | generate logo     |

```bash
npx skills add -g https://github.com/op7418/logo-generator-skill.git
```
