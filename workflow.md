# Blueprint Workflow (WIP)

<!-- TODO: move to Owl and develop further in Owl -->

<!--
Note: this is very raw work in progress for what will eventually become the workflow description.
-->

## Description

Workflow:

1. Create initial blueprint (50%)
   - Exploration and conceptualisation (what and why) and design (how)
   - Document types
      - Knowledge capture (for yourself)
         - Research notes
      -  Project definition docs (for the agent)
         - Concept doc (what and why)
         - ADRs
         - Design docs and specs (how)
    - Project definition docs are the actual blueprint
2. Implement and iterate on blueprint (50%)
   - Decompose specs into actionable tasks
   - Use spec-driven development (SDD), Gemini Conductor, etc
   - On new insights, revise blueprint: update specs and design docs, if necessary, amend concept doc
   - Restart implementation on new version of blueprint

Principles:

- Blueprint is always coherent and complete *relative to your current understanding* before implementation starts
- Blueprint is source of truth for intention: always change blueprint first, implementation follows blueprint

Catch phrases:

- Design first, build second
- The intellectual asset of the project is no longer primarily the code, it's the blueprint
- The primary artifact shifts from being the codebase to being the living specification of the system
- The better the blueprint is, the more independently and reliably an agent can work.
- The blueprint is the programming interface between you and the agent.
- Coding agents make it worthwhile to invest much more effort in design because the implementation cost has dropped so dramatically.
- Thinking about systems before setting your agent loose (HumanLayer promo video)

Caveats:

- Curation creep: exit criteria for phase 1 ("the blueprint is ready when an agent could start component X without asking me anything") (TODO: to be refined)
- Prototyping: make prototyping an explicit phase-1 activity: prototypes feed research notes and ADRs and are then deleted (TODO: this might include some creep too, if you start polishing a prototype)

References:

- https://mattfarrugia.com/posts/experiments-in-blueprint-driven-development: primary resource where the term "blueprint-driven development" is used with a similar meaning (besides that, there seem to be no major usages of this term)
- https://github.com/weibeld/agentic-dev-workflow: early attempt at an agentic software development workflow


## Related Approaches

### Spec-Driven Development (SDD)

GitHub Spec Kit:

1. Specify (what and why)
2. Plan (how)
3. Tasks
4. Implement

AWS Kiro:

1. Requirements (what and why)
2. Design (how)
3. Tasks
4. Implement

Changes and iterations:
- Describe large changes in new specs
- Small changes as edits to existing spec (then run through plan, tasks, and implement steps again)

Notes:
- For both new projects (greenfield) and existing projects (brownfield)

References:
- https://github.com/github/spec-kit

### Research-Plan-Implement (RPI)

1. Research (understand existing code base and requirements)
2. Plan (how)
3. Implement

Evolution: QRDSPI

1. Questions
2. Research
3. D - TODO
4. Structure
5. Plan
6. Implement

Notes:
- For existing code bases (brownfield projects)
- Assumes that the "what" and "why" already exist
- Implemented in the HumanLayer IDE
- RPI to QRDSPI evolution explained in https://youtu.be/YwZR6tc7qYg?si=XN4jTHh_f87h5kYg

References:
- https://www.youtube.com/watch?v=rmvDxxNubIg (context engineering, introduction of RPI)
- https://www.youtube.com/watch?v=YwZR6tc7qYg (RPI to QRDSPI)
- https://www.youtube.com/watch?v=8kMaTybvDUw (12 factor agents)
- https://github.com/humanlayer/12-factor-agents (12 factor agents)
- https://github.com/humanlayer/advanced-context-engineering-for-coding-agents (advanced context engineering for coding agents)
