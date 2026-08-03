# AGENTS.md

## Repository intent

This repository is for a local, browser-based, Python-backed statistical data explorer for an approved tabular dataset.

The selected direction is:

- a lightweight local web application
- validation-first behavior before any report is treated as usable
- clear visible failure states when validation does not pass
- dataset profiling and summary reporting
- transparent visibility of dataset source, declaration/profile, and known limitations
- a single centralized dataset profile for dataset-specific fields

Do not treat any candidate label as having a standard meaning outside this repository’s selected direction.

## Operating rules

### 1. One approved plan item at a time
Work on exactly one approved plan item at a time.

- Do not begin the next item until the current approved item is complete and accepted.
- If a task expands beyond the approved scope, pause and request approval before continuing.

### 2. Explain before edits
Before making a code or documentation change, provide a short explanation that states:

- what will change,
- why it is needed,
- how it relates to the approved plan item,
- what evidence will be used to verify the result.

No silent edits.

### 3. Truthful command reporting
When a command is run, report it truthfully and exactly.

- State the command that was run.
- State what it was intended to check or change.
- State the actual result, including any error output or exit status.
- Do not claim a check passed without fresh command evidence.

### 4. Required checks before acceptance
A change is not accepted unless the agreed checks for that item are completed and the evidence is visible.

At minimum, acceptance must confirm:

- the relevant validation and reporting behavior still works for the approved sample dataset,
- a failed validation remains visibly and explicitly a failure,
- required summaries and relationship views are present or updated as intended,
- the dataset profile remains the single central source for dataset-specific fields,
- no regression was introduced in the intended workflow.

### 5. Update planning and decision records
Whenever an approved change is made, update the repository’s planning and decision records:

- keep Plan.md aligned with the current approved work item and status
- keep Decisions.md as the record of approved decisions, constraints, and trade-offs

These files must not be left stale after implementation work.

## Approval gates

The following changes require explicit approval before they are made:

- dependencies
- architecture
- public interfaces
- source data
- expected test values or baseline outputs

No approval means no change to those areas.

## Prohibitions

Do not:

- expose or introduce sensitive data, secrets, credentials, tokens, personal data, or other restricted information
- use destructive commands against repositories, filesystems, or environments
- allow unrestricted execution of arbitrary commands or code
- weaken or bypass failing tests to remove a failure
- hide a validation failure behind a misleading successful-looking report
- scatter dataset-specific logic across the codebase instead of keeping it centralized in the dataset profile

## Implementation expectations

- Keep the tool simple and researcher-friendly.
- Keep analysis transparent and auditable.
- Keep source provenance and known limitations visible in the user flow.
- Prefer a single, replaceable dataset profile for dataset-specific metadata and expected fields.
- Preserve the validation-first workflow and inspectable reporting behavior.

## Response style

When asked to make changes:

1. identify the approved plan item,
2. explain the proposed edit,
3. wait for approval,
4. make the smallest change needed,
5. report the actual commands and evidence used to verify it,
6. update Plan.md and Decisions.md as required.

## Final rule

A claim of completion must be backed by the actual command output and the relevant acceptance checks, not by assumption or expectation.
