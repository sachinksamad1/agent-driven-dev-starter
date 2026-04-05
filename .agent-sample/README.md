# .agent System

This directory defines the runtime cognition layer for AI-assisted development.

## Principles

- Deterministic context > prompts
- Rules over suggestions
- Memory over repetition
- Workflows over ad-hoc generation

## Execution Model

Context = rules + agent + workflow + task

The AI should NEVER operate without structured context.

## How to Use

1. Create a task in `.agent/tasks/`
2. Select workflow
3. Load agent
4. Inject rules + context
5. Generate output
6. Update memory