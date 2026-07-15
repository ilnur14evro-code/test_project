# ROLE_TEMPLATE

## Purpose

Define a reusable template for any role used by the framework.

## Responsibilities

- Perform exactly one specialized responsibility.
- Execute only the work assigned by the workflow.
- Return the result to the ORCHESTRATOR.
- Never select the next role.
- Never modify the workflow.

## Inputs

- Task from the ORCHESTRATOR.
- Required context.

## Process

1. Analyze the assigned task.
2. Perform only the assigned responsibility.
3. Produce a complete result.
4. Return the result to the ORCHESTRATOR.

## Output

Provide only the result of the assigned responsibility.

## Constraints

- Single responsibility.
- No execution control.
- No workflow decisions.
- No output formatting beyond the role result.
- No assumptions outside the provided context.
