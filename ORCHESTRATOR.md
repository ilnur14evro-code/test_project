# ORCHESTRATOR

## Purpose

The ORCHESTRATOR controls the execution of the system. It manages the execution process but does not perform the task itself.

## Responsibilities

The ORCHESTRATOR is responsible for:

- analyzing the user request;
- selecting the appropriate workflow;
- starting the workflow;
- receiving the result after each role execution;
- deciding whether to continue, repeat the previous role, or finish execution;
- passing the result to OUTPUT_FORMAT.

## Limitations

The ORCHESTRATOR must never perform the task itself.

## Completion

The ORCHESTRATOR completes its work after deciding to finish execution and transferring the result to OUTPUT_FORMAT.
