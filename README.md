# mimo-agent-dev-workflow
An AI Agent workflow for software development, integrating MiMo API with coding tools such as Claude Code, Cursor, and OpenCode for task decomposition, code generation, and documentation.
# MiMo Agent Dev Workflow

A lightweight AI Agent workflow for software development, designed to integrate MiMo API with modern AI coding tools such as Claude Code, Cursor, and OpenCode.

## Overview

MiMo Agent Dev Workflow aims to build a reusable AI-assisted development pipeline. The project focuses on transforming a software requirement into a structured development process, including task decomposition, code generation, code review, test generation, and documentation.

The project will use MiMo API for long-context code understanding, multi-turn reasoning, and batch generation tasks. It is designed as a high-frequency LLM calling scenario for real development workflows.

## Problems to Solve

Current AI coding tools are powerful, but developers still need to manually guide the model across many steps. This project tries to solve the following problems:

1. Requirements are difficult to convert into executable development tasks.
2. Large codebases require long-context understanding and repeated model calls.
3. AI-generated code often lacks review, testing, and documentation.
4. Multiple AI coding tools are hard to coordinate in a consistent workflow.

## Core Workflow

The planned workflow contains five Agent roles:

### 1. Product Agent

Analyzes user requirements and breaks them into smaller development tasks.

### 2. Code Agent

Generates or modifies code based on the task description and project context.

### 3. Review Agent

Reviews generated code for bugs, maintainability, security risks, and style issues.

### 4. Test Agent

Generates unit tests, edge cases, and API test cases.

### 5. Docs Agent

Creates README updates, API documentation, changelogs, and usage examples.

## Planned MiMo API Usage

MiMo API will be used in the following scenarios:

- Long-context code understanding
- Multi-turn Agent reasoning
- Requirement analysis
- Code generation and refactoring
- Code review
- Test case generation
- Error log analysis
- Technical documentation generation
- Multi-model comparison with Claude, GPT, and DeepSeek

## Why This Project Needs a Large Token Plan

This project requires frequent and long-context model calls. Token consumption mainly comes from:

- Sending project files, requirements, and logs as context
- Running multiple Agent steps for a single development task
- Generating tests and documentation in batches
- Comparing MiMo outputs with other model families
- Iterating prompts and workflows across real development cases

## Example Use Cases

### Use Case 1: Generate API from Requirement

Input:

```text
Build a user login API with email/password authentication and JWT token support.
