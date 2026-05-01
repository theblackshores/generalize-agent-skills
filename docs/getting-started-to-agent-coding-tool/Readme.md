# Getting Started To Agent Coding Tool

## Using NPM

Almost all Agent Coding Tools support NPM. Because most developers already have NPM installed, using it is a quick and seamless way to get started.

Claude Code:
```bash
npm install -g @anthropic-ai/claude-code
```

Copilot CLI:
```bash
npm install -g @github/copilot
```

You can find installation instructions for other Agent Coding Tools in the official documentation.

<details>
<summary>Windows install NPM via Scoop</summary>

If you don't already have Scoop installed, please install it via PowerShell:
```bash
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
Invoke-RestMethod -Uri https://get.scoop.sh | Invoke-Expression
```

Install nvm (Node Version Manager):
```bash
scoop bucket add main
scoop install main/nvm
```

Install LTS version Node.js:
```bash
nvm install lts
nvm use lts
```
</details>

<details>
<summary>Notes: The Node.js LTS version changes frequently. If you really want to upgrade, you can use the following steps to migrate globally installed packages to the new version.</summary>

Windows:
```bash
npm -g list --json | jq -r '.dependencies | keys | .[]' | grep -Pv '(corepack|npm)' | tee old-npm-global.txt

# After installed the new node version:
while read -r pkg; do npm install -g "$pkg"; done < old-npm-global.txt
```

MacOS/Linux:
```bash
nvm reinstall-packages $old_version
```
</details>

## Using Package Manager

While NPM is convenient, it can cause problems when Agent Coding Tools need to perform actions like "killing all node.exe processes," because Agent Coding Tools installed via NPM also contain one or more node.exe processes.

Therefore, to handle most situations and reduce the need for manual intervention, another option is to install Agent Coding Tools via a package manager, as these are typically distributed as binary files.

Windows (Scoop):
```bash
# Copilot CLI
scoop install main/copilot-cli

# Claude Code
scoop install main/claude-code
```

## Choose Agent Coding Tool On Restricted Regions

### Copilot CLI (Pro/Pro+)

You can access all the most advanced models (Claude Opus, etc.) in an affordable way. Billing based on the number of requests.

News:
- [Switch to usage-based billing on June 1, 2026](https://github.blog/news-insights/company-news/github-copilot-is-moving-to-usage-based-billing/)

### Claude Code

Because Claude employs many restrictions, including but not limited to verification of authentic documents, the best way to use Claude Code is through a custom API.

The documentation from the model vendor you use will usually include instructions on how to use Claude Code through their models.

<details>
<summary>Example for DeepSeek API</summary>

Powershell Script:
```powershell
$env:ANTHROPIC_BASE_URL="https://api.deepseek.com/anthropic"
$env:ANTHROPIC_AUTH_TOKEN="sk-$YOUR_API_KEY"
$env:ANTHROPIC_MODEL="deepseek-v4-pro[1m]"
$env:ANTHROPIC_DEFAULT_OPUS_MODEL="deepseek-v4-pro[1m]"
$env:ANTHROPIC_DEFAULT_SONNET_MODEL="deepseek-v4-pro[1m]"
$env:ANTHROPIC_DEFAULT_HAIKU_MODEL="deepseek-v4-flash"
$env:CLAUDE_CODE_SUBAGENT_MODEL="deepseek-v4-flash"
$env:CLAUDE_CODE_EFFORT_LEVEL="max"

claude @args
```
</details>
