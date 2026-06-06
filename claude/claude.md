# Claude Code

Claude Code is an agentic coding tool that reads your codebase, edits files, runs commands, and integrates with your development tools. Available in your terminal, IDE, desktop app, and browser.

The claude.md file is a special project-level instruction file used by Claude Code to guide how it behaves while working on your codebase or project.

> Think of it as a "persistent system prompt file" that the agent consults every time it processes your commands.

The `claude.md` file is typically located in the root of your project directory and can be used to set project-specific configurations, guidelines, or even reminders for the agent. This allows you to maintain consistency across your project and ensure that the agent understands the context and requirements of your codebase.

You can make a `CLAUDE.md` file in your project directory by command **/init** in Claude Code or by simply creating a new markdown file named `CLAUDE.md` in the root of your project folder. 

> CLAUDE.md is loaded every session, so only include things that apply broadly. For domain knowledge or workflows that are only relevant sometimes, use skills instead. Claude loads them on demand without bloating every conversation.

<img src="https://mintcdn.com/claude-code/6yTCYq1p37ZB8-CQ/images/context-loading.svg?fit=max&auto=format&n=6yTCYq1p37ZB8-CQ&q=85&s=5a58ce953a35a2412892015e2ad6cb67" alt="Context loading: CLAUDE.md loads at session start and stays in every request. MCP tool names load at start with full schemas deferred until use. Skills load descriptions at start, full content on invocation. Subagents get isolated context. Hooks run externally." style="width: 50%;" />

---

## Commands





---

## Skills 

agent skill : https://github.com/agentskills/agentskills.git 

https://agentskills.io/home 

## What is `.claude/settings.local.json`?

This file contains **machine-specific or developer-specific Claude Code settings**.

It is intended for settings that:

- Should not be shared with the entire team
-   Depend on your local environment
-   May contain personal preferences
-   May contain local paths
-   May contain permissions for tools

Typically:

```text

project/
       ├── .claude/│   
       │   ├── settings.json│   
       │   └── settings.local.json

```

###

```json
{
  "permissions": {
    "allow": [
      "Read(*)",
      "Edit(*)",
      "Bash(ls)"
    ]
  }
}
```

