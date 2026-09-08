# CLAUDE.md — Blueprint Workflow

## Background

The whole point to start with the blueprint-workflow repo topic was to apply this workflow (especially the blueprint/ directory docs) to the Owl project, in order to collect ideas and notes in the form of research docs and shaping the concept doc.

EDIT 2026-09-07: this might be partly obsolete with the new idea of conducting research as actual Owl notes in a general way, and not as part of the blueprint for a specific project (to avoid that projects are started but never completed). The initial idea for this thought was to have a separate general research repo similar to Owl but then there was a discussion whether this research repo and Owl should actually be combined in the same repo (i.e. research is just a part of what's in Owl).

## Repository overview

This repository defines the Blueprint Workflow - an agentic software development workflow for greenfield projects.

The repository contains two main files:

- `workflow.md`: the human-readable description of the workflow
- `instructions.md`: the agent instructions intended to be imported into the agent context of a target software project

### `workflow.md`

TODO: remove and move to Owl, include relevant info for user in README

- Intended for human readers
- Serves as a source of truth for the conceptualisation and development of the workflow
- May later inform a published story about the workflow in [Nightingale](https://github.com/weibeld/nightingale)

### `instructions.md`

- Intended to be included in the context window of a coding agent (currently only Claude Code is supported)
- Contains instructions for an agent to maintain the workflow documents in the target project's `blueprint/` directory
- Should be kept concise since this file is included in the context of every project that uses the workflow
