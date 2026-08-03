# Plan

## Selected direction

Build a local browser-based Python-backed tool for reviewing an approved tabular dataset. The first version will accept a single CSV file and provide a clear validation-first workflow with no Python writing required from the user.

## Scope

- Local browser-based interaction
- Validation before a report is treated as usable
- Clear failure state for invalid data declarations
- Summary of record and column counts
- Missingness and descriptive statistics
- A small set of visualization-based relationships
- Visible source provenance and known limitations
- A single centralized dataset profile for dataset-specific fields

## Approved minimum deliverable

1. Load a single approved CSV file.
2. Validate the declared file structure and expected schema.
3. Show a clear failure message when validation does not pass.
4. Provide record and column counts.
5. Report missingness and key descriptive statistics.
6. Display a few useful relationship plots.
7. Keep source and limitations visible in the report.

## Current working rule

Only one approved plan item is in progress at a time. Before moving to the next item, the current item must be completed, verified, and accepted.

## Recordkeeping requirement

Update Plan.md and Decisions.md whenever the approved scope, decisions, or acceptance checks change.
