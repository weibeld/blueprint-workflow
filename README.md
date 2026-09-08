# Blueprint Workflow

An agentic software development workflow for greenfield projects.

## 🧠 Workflow

> TODO: remove (move to Owl) and include all relevant user info in README

The workflow is described in [`workflow.md`](workflow.md).

## 🤖 Agent Instructions

These are the agent instructions that facilitate the application of the workflow in your software projects.

The agent instructions are defined in [`instructions.md`](instructions.md) and are intended to be injected into the context window of your coding agent.

> **Note:** currently Claude Code is the only supported target agent.

> TODO: support other agents:
>   - Generic installation supporting all agents?
>   - Dedicated installation approach for set of supported agents?

### Usage (Claude Code)

> TODO: replace with more streamlined installation option, for example:
>   - Claude Code rules (https://code.claude.com/docs/en/memory#organize-rules-with-claude/rules/)
>   - Claude Code skills (https://code.claude.com/docs/en/skills)

1. Clone the repository:
    ```bash
    git clone https://github.com/weibeld/blueprint-workflow
    ```
2. Import the instructions into your project's `CLAUDE.md` file with the [`@path`](https://code.claude.com/docs/en/memory#import-additional-files) import syntax:
    ```markdown
    @<path>/blueprint-workflow/instructions.md
    ```
    > ⚠️ **Caution:** make sure the import path matches the actual file location. If the paths mismatch, the import will fail silently.
