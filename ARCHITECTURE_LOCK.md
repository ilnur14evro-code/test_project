# Architecture

## Purpose

This framework provides a modular architecture for building AI agents using prompt specifications only. ChatGPT acts as the execution engine, while the framework defines how a task is processed.

---

## Execution Flow

```text
User
  │
  ▼
ORCHESTRATOR
(analyzes the request and selects a workflow)
  │
  ▼
WORKFLOW
  │
  ▼
ROLE
  │
  ▼
ORCHESTRATOR
(decides the next action)
  │
  ├── Next role
  ├── Repeat previous role
  └── Finish
        │
        ▼
OUTPUT_FORMAT
        │
        ▼
Response
```

---

## Components

### User
Provides a task for the framework.

### ORCHESTRATOR
Responsible for controlling execution.

Responsibilities:
- analyze the user request before selecting a workflow;
- select the appropriate workflow;
- start the workflow;
- decide what happens after each role execution;
- determine whether to continue, repeat or finish execution.

The ORCHESTRATOR does not perform the task itself.

### WORKFLOW
Defines the sequence of roles required for a specific class of tasks.

A workflow contains process logic only.

It does not execute work.

### ROLE
Performs one specialized responsibility.

A role:
- performs its assigned work;
- returns its result to the ORCHESTRATOR.

A role never decides what happens next.

### OUTPUT_FORMAT
Formats the final approved result before returning it to the user.

It does not modify the task execution.

---

## Architecture Principles

- The architecture is task-independent.
- Every component has a single responsibility.
- Roles never control execution.
- Control always returns to the ORCHESTRATOR after each role execution.
- The ORCHESTRATOR controls the execution flow.
- WORKFLOW defines process, not content.
- OUTPUT_FORMAT is applied only to the final result.

---

## Repository Structure

### Core
- SYSTEM.md
- ORCHESTRATOR.md
- OUTPUT_FORMAT.md

### Templates
- ROLE_TEMPLATE.md
- WORKFLOW_TEMPLATE.md

### Roles
- ROLE_PLANNER.md
- ROLE_CRITIC.md
- ROLE_CODER.md
- ROLE_REVIEWER.md

### Workflows
- WORKFLOW_CREATE_ARTICLE.md
- WORKFLOW_SOLVE_BUG.md
- WORKFLOW_SUMMARIZE_TEXT.md

### Documentation
- README.md
- ARCHITECTURE_LOCK.md
- DESIGN_DECISIONS.md
- CHANGELOG.md

---

## File Ownership

### Core
- SYSTEM.md
- ORCHESTRATOR.md
- OUTPUT_FORMAT.md

### Templates
- ROLE_TEMPLATE.md
- WORKFLOW_TEMPLATE.md

### Roles
- ROLE_*.md

### Workflows
- WORKFLOW_*.md

### Documentation
- README.md
- ARCHITECTURE_LOCK.md
- DESIGN_DECISIONS.md
- CHANGELOG.md

### Repository Reviewer
- Entire repository