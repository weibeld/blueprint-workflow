# CLAUDE.md — Blueprint Instructions

## Project overview

This repository contains Claude Code instructions (`instructions.md`) for maintaining the blueprint documents in software projects that use the Blueprint Workflow.

The blueprint documents are located in the `blueprint/` directory of a software project.

The Blueprint Workflow says to first create a blueprint (the files in the `blueprint/` directory) that is complete and coherent relative to the current state of knowledge, and after that start deriving the implementation from this blueprint. As the implementation reveals new insights that require changes, first the blueprint is updated, and then the implementation is derived again from this updated blueprint. This cycle may repeat multiple times.

## Editing guidelines

- The target audience of the `instructions.md` file is an LLM agent (in this case Claude Code)
- The `instructions.md` file should be kept concise because it is loaded into context in the target projects

## Open questions

1. Could this be implemented with Claude Code rules (https://code.claude.com/docs/en/memory#organize-rules-with-claude/rules/)?
2. Could this be implemented with Claude Code skills (https://code.claude.com/docs/en/skills)?
3. Currently, this repo works only for Claude Code. Are there ways to make it generic so that it also works with other agents?
4. Do we also need instructions in this repository for guiding the implementation stage of the workflow?
