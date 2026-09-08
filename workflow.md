# Blueprint Workflow (WIP)

<!-- TODO: move to Owl and develop further in Owl -->

<!--
Note: this is very raw work in progress for what will eventually become the workflow description.
-->

## Description

<!--
  TODO 2026-09-08: is the two-stage process (first design, then implement) still right, or do we actually tend more towards a prototype-driven approach? In particular, if research is being done outside the project repo on an ongoing basis and occasionally aspects of this research are "spun off" and implemented in concrete projects, might these implementations become or evolve into prototype of the actual first-level projects? And if so, would we then continue the implementation of these projects based on these prototypes (as it is currently the case, for example, for Owl)? Should this somehow be represented in the workflow, e.g. prototypes are exploration which may inform the blueprint, and the blueprint then still drives the real implementation (i.e. separate code bases for prototypes and final implementation)? Or that the prototype actually become the real implementatino and the blueprint then kind of needs to catch up with the current state of prototype and then is maybe mainly used to drive the further development of th project when it's clear that what's being built now is the real thing?
  One option is to have prototypes in a prototype/ (or prototypes/) directory at the root level (adjacent to blueprint/). The workflow would then recognise this a prototypes and not the real implementation and thus wouldn't enforce the source-of-truth relation between the blueprint and the implementation. The real implementation is expected to live in the root directory of the repo. A prototype can be "committed" to become the real implementation by moving it from the prototype/ directory to the root directory, and from that moment on, the source-of-truth relation between the blueprint and the implementation must hold (i.e. blueprint must describe implementation). Alternatively, the real implementation can also be started from scratch in the root directory (maybe informed by the prototype). Prototypes (and the entire prototype/ directory) may be deleted when the prototypes become obsolete. Important for the workflow to note is that everything in the repo besides blueprint/ and prototype/ is the actual implementation and needs to be analysed as such.
-->


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
