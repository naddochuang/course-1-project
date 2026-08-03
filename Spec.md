# Specification

## Product intent 

Create a lightweight local web application for approved tabular dataset review. The tool supports quick exploratory understanding without requiring the user to write Python.

## User workflow

1. Open the local browser-based tool.
2. Load an approved CSV dataset.
3. Receive immediate validation feedback.
4. Review counts, missingness, descriptive summaries, and relationship plots.
5. Interpret the output with visible source and limitation context.

## Functional requirements

- The tool must run locally in a browser.
- Python is used behind the scenes for analysis and reporting.
- The dataset must be validated before the report is presented as usable.
- Validation failure must be explicit and visibly displayed.
- The report must surface key statistical facts first.
- Relationship plots should help reveal structure, patterns, and irregularities.

## Data handling requirements

- The first dataset profile must remain centralized and replaceable.
- Dataset-specific logic must not be scattered through the app.
- Source provenance and known constraints must remain visible in the report.

## Acceptance expectations

The implementation is acceptable only when the user can:

- load a local approved dataset,
- see validation outcomes clearly,
- understand the dataset’s scale and quality,
- examine key summaries and relationships,
- identify limitations before drawing conclusions.
