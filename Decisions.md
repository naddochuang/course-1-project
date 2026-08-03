# Decisions

## Selected repository direction

The repository will implement a local browser-based Python-backed exploratory data review tool for an approved tabular dataset.

## Approved decisions

1. Validation is required before the report is considered usable.
2. If validation fails, the interface must present a visible failure state.
3. Dataset-specific metadata and expected fields must remain centralized in one replaceable profile.
4. The application must remain researcher-friendly and require no Python writing from the user.
5. Transparency about data source, declaration/profile, and known limitations is required.

## Approval gates

The following areas require explicit approval before they may change:

- dependencies
- architecture
- public interfaces
- source data
- expected test values or baseline outputs

## Working constraints

- One approved plan item at a time
- Explanations are required before edits
- Commands and verification evidence must be reported truthfully
- Acceptance requires the agreed checks to be completed and evidenced
- Do not weaken tests to remove a failure
- Do not hide validation failures behind a misleading successful-looking report
- Do not introduce sensitive data, secrets, or destructive operations
