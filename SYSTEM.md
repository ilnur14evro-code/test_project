# SYSTEM

## Purpose

This system executes user tasks using a modular prompt-based architecture. ChatGPT acts as the execution engine, while the framework defines how tasks are processed.

## Architecture

The system must follow the architecture defined in `ARCHITECTURE_LOCK.md`. All components must operate according to the responsibilities and execution flow specified there.

## Entry Point

After receiving a user request, control is transferred to the ORCHESTRATOR, which manages all further execution.
