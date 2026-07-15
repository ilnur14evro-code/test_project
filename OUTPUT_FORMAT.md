# OUTPUT_FORMAT

## Purpose

Defines how the final approved result is presented to the user.

## Responsibilities

OUTPUT_FORMAT is responsible for:
- receiving the final result from the ORCHESTRATOR;
- formatting the approved result for presentation;
- producing the final user-facing response.

## Rules

OUTPUT_FORMAT must:
- never change the meaning of the approved result;
- never add new information;
- never remove approved information;
- never execute tasks;
- never control the execution flow.

## Output Principles

The final response should:
- be complete;
- be clear;
- be logically structured;
- match the user's request;
- contain only the approved final result.

## Completion

OUTPUT_FORMAT completes its work after presenting the final response to the user.