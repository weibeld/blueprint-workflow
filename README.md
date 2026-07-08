# Blueprint Workflow

An agentic software development workflow for greenfield projects.

## 🧠 Workflow

The workflow is described in [`workflow.md`](workflow.md).

## 🤖 Agent Instructions

These are the agent instructions that facilitate the application of the workflow in your software projects.

The agent instructions are defined in [`instructions.md`](instructions.md) and are intended to be injected into the context window of your coding agent.

> **Note:** currently Claude Code is the only supported target agent.

### Usage (Claude Code)

1. Clone the repository:
    ```bash
    git clone https://github.com/weibeld/blueprint-workflow
    ```
2. Import the instructions into your project's `CLAUDE.md` file with the [`@path`](https://code.claude.com/docs/en/memory#import-additional-files) import syntax:
    ```markdown
    @<path>/blueprint-workflow/instructions.md
    ```
    > ⚠️ **Caution:** make sure the import path matches the actual file location. If the paths mismatch, the import will fail silently.
