# CLAUDE.md — Blueprint Workflow

## Repository overview

This repository defines the Blueprint Workflow - an agentic software development workflow for greenfield projects.

The repository contains two main files:

- `workflow.md`: the human-readable description of the workflow
- `instructions.md`: the agent instructions intended to be imported into the agent context of a target software project

### `workflow.md`

- Intended for human readers
- Serves as a source of truth for the conceptualisation and development of the workflow
- May later inform a published story about the workflow in [Nightingale](https://github.com/weibeld/nightingale)

### `instructions.md`

- Intended to be included in the context window of a coding agent (currently only Claude Code is supported)
- Contains instructions for an agent to maintain the workflow documents in the target project's `blueprint/` directory
- Should be kept concise since this file is included in the context of every project that uses the workflow

## Open questions

1. Could the instructions be implemented with Claude Code rules (https://code.claude.com/docs/en/memory#organize-rules-with-claude/rules/)?
2. Could the instructions be implemented with Claude Code skills (https://code.claude.com/docs/en/skills)?
3. Currently, the instructions work only for Claude Code. Are there ways to make it generic so that it also works with other agents?
4. Do we also need instructions in this repository for guiding the implementation phase of the workflow?
