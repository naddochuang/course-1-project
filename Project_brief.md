# Project Brief

## Working Title
Local Browser-Based Statistical Data Explorer for Approved Tabular Datasets

## Problem Statement
A researcher has an approved tabular dataset that is far too large and irregular to understand by manually reading rows. The dataset cannot be meaningfully interpreted through casual inspection alone. The researcher needs a local browser-based tool that uses Python to surface important statistical facts without requiring them to write Python code.

The tool should make the dataset understandable at a glance, while keeping the source information and known limitations clearly visible. It must support quick validation of the declared data, provide essential counts and data-quality indicators, and show useful statistical summaries and visual relationships among variables.

## Goal
Create a lightweight local web application that lets a researcher:

- load an approved tabular dataset locally,
- inspect the dataset without writing Python,
- verify that the declared data structure is valid,
- understand the dataset’s size, quality, and shape,
- identify meaningful patterns and relationships through summaries and plots,
- retain transparency about dataset provenance and known constraints.

## User Need
The user is a researcher working with a trusted but messy dataset. They need an interface that reduces the effort of exploratory data analysis to a few clicks, while preserving rigor. The tool should reveal important statistical facts about the data in a way that is immediately useful, interpretable, and auditable.

## Core Requirements

### 1. Local, browser-based interaction
- The application must run locally in a browser.
- It must not require the user to install or write Python code.
- Python should be used behind the scenes to perform analysis and generate insights.

### 2. Data validation
- The tool must validate the declared dataset before presenting a report.
- Validation must confirm whether the dataset structure, schema, and declared expectations are met.
- If validation fails, the result must be visibly presented as a failure state rather than a misleading “valid” empty report.

### 3. Dataset profiling and reporting
The tool must show:

- record counts,
- column-level counts,
- missingness or null rates,
- useful descriptive summaries,
- visible relationships between variables through charts or plots.

### 4. Transparency
The report must keep the following visible:

- the dataset source,
- the dataset declaration or profile used by the tool,
- any known limitations or cautions about interpretation.

### 5. Dataset-specific configuration must remain centralized
The first dataset is introduced later, and its specific fields must remain in one replaceable profile instead of being scattered through the application. This profile should serve as the single configuration point for dataset-specific metadata, expected columns, and field behavior.

## Required Behavior

### Validation behavior
A failed validation must look like a failure:

- the interface should clearly indicate that the dataset did not pass validation,
- the failed state should be visible and explicit,
- the user should not be left with a report that appears successful but contains no meaningful data.

### Summary behavior
The report should highlight the most important facts first, such as:

- how many rows and columns are present,
- whether the dataset is complete or has significant missing values,
- whether the declared fields align with expectations,
- what the main statistical shape of the data looks like.

### Visual behavior
The interface should show relationships that are useful for exploratory understanding, such as:

- distribution plots,
- relationships between variables,
- anomalies or irregularities that may require further review.

## Design Constraints
- The tool should be simple enough for a researcher to use without coding.
- The analysis should be trustworthy and transparent.
- The experience should make quality issues easy to spot rather than hidden behind a “clean” report.
- Dataset-specific logic must be isolated in a single profile to make future datasets easy to swap in.

## Success Criteria
The project is successful if the researcher can:

1. open the local browser-based tool,
2. load or point to an approved dataset,
3. see immediate validation feedback,
4. understand the dataset’s scale and quality,
5. review meaningful summaries and relationships without writing Python,
6. identify any major limitations or risk areas before drawing conclusions.

## Non-Goals
- Building a full data science notebook environment
- Allowing ad hoc Python scripting in the interface
- Supporting arbitrary unsupported file types without explicit validation
- Hiding the source or limitations of the dataset behind a polished visual report

## Expected Outcome
A researcher-facing, local browser-based Python-backed exploratory data tool that presents a dependable review of an approved tabular dataset. The output should be both understandable and rigorous, with clear validation behavior and a centralized dataset profile that makes later dataset additions straightforward.
