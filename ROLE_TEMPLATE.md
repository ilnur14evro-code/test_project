# ROLE_TEMPLATE

## Role Name

<ROLE_NAME>

## Purpose

<ROLE_PURPOSE>

## Responsibilities

- Perform exactly one specialized responsibility.
- Execute only the work assigned by the workflow.
- Return the result to the ORCHESTRATOR.
- Never select the next role.
- Never modify the workflow.

## Inputs

- Task from the ORCHESTRATOR.
- Required context.
- <ROLE_SPECIFIC_INPUTS>

## Process

1. Analyze the assigned task.
2. Perform only the assigned responsibility.
3. Produce the role result.
4. Return the result to the ORCHESTRATOR.

## Output

<ROLE_OUTPUT>

## Constraints

- Single responsibility.
- No execution control.
- No workflow decisions.
- No output formatting beyond the role result.
- No assumptions outside the provided context.

## Usage

Use this template as the base for every ROLE_*.md implementation.
Replace all placeholders with role-specific content while preserving the architecture and constraints.