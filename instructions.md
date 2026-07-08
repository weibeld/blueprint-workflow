# Blueprint Workflow — Agent Instructions

These instructions define the structure and document types of the `blueprint/` directory of a project repository. The blueprint directory contains all documents that define the project and on which the implementation is based.

<!--
TODO:
  - Provide minimal template for concept doc? this is not a hard template but just to remind users how we structure our concept docs usually
  - Same for specs? do the usually follow a certain pattern? 
  - If we provide templates to be seen by the user, we would probably also include html comments for notes (see the curretn /Users/dw/repos/weibeld/giraffe/docs/concept.md), so we should maybe mention this here too. i think also the ADR template includes html comments
-->

## Directory layout

```
blueprint/
├── adr/               # Architecture Decision Records (ADR)
├── notes/             # Research notes
├── concept.md         # Concept doc
├── questions.md       # Open questions log
└── spec-<topic>.md    # Specs (one per topic)
```

The following sections describe the individual document types.


## Architecture Decision Records (ADR)

- **File name:** `adr/<number>-<topic>.md` (e.g. `adr/0001-use-read-write-api.md`, number is four-digit, zero-padded, and sequential)
- **Format:** fixed structure, see template below
- **Editing:** never updated after creation (only the status may change)
- **Goal:** provide a trail of crucial decisions (expensive to reverse or cutting across the system), considered alternatives, rationales, and consequences

ADR template:

fixed structure (template to be defined)
<!--
TODO: decide on the final template form
-->

## Research notes

- **File name:** `notes/<date>-<topic>.md` (e.g. `notes/2026-07-03-api-authentication-method.md`, date in `YYYY-MM-DD` format)
- **Format:** free form
- **Editing:** may be edited at any time
- **Content:** arbitrary notes related to explorations, no guarantees on correctness, completeness, or conclusiveness, discardable
- **Goal:** externalise thinking, support exploration

## Concept doc

- **File name:** `concept.md`
- **Format:** free form
- **Editing:** kept in sync with new stable states of the project (e.g. after major pivots or changes)
- **Goal:** answer the question "What are we building and why?"

## Open questions log

- **File name:** `questions.md`
- **Format:** list of items, each with date, body, and status (see template below)
- **Editing:** append-only (only the status of existing items may be changed)
- **Goal:** maintain a trail of open questions and their resolution; a decided question graduates into an ADR and the item records the pointer
- **Statuses:** `open` | `decided <decision>` | `obsolete` (decision may be specified as an ADR reference or as an inline description)

Open question item template:

fixed structure (template to be defined)
<!--
TODO: define (should it be in section format or each question just a list item in ia flat list (with a sub-list per question)?)
-->

## Specs

- **File name:** `spec-<topic>.md` (e.g. `spec-cli.md`, `spec-storage.md`)
- **Format:** free form, may include design context (architecture, trade-offs) followed by normative requirements
- **Editing:** living documents, edited in place and always kept in sync with the current intended state of the system. Versioning is provided by Git; no version numbers, dates, or sequence numbers in file names. Significant changes are backed by an ADR recording the rationale.
- **Goal:** define what a component or feature must do, precisely enough that an implementation can be derived from and checked against it
