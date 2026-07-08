# Blueprint Instructions (Claude Code)

Claude Code instructions for maintaining the blueprint documents (`blueprint/` directory) in software projects using the Blueprint Workflow.

## Usage

To use the blueprint instructions for your project, proceed as follows:

1. Clone the repository:
    ```bash
    git clone https://github.com/weibeld/blueprint
    ```
2. Import the blueprint instructions into your project's `CLAUDE.md` file with the [`@path`](https://code.claude.com/docs/en/memory#import-additional-files) import syntax:
    ```markdown
    @<path>/blueprint/instructions.md
    ```
    > ⚠️ **Caution:** make sure the import path matches the actual file location. If the paths mismatch, the import will fail silently.
