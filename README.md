# 🧠 Agent-Driven Development Starter

> Stop prompting. Start orchestrating.

This repository provides a **structured `.agent/ system`** for building software with AI in a **deterministic, scalable, and maintainable way**.

Instead of relying on fragile prompts, this approach introduces:

* **Context composition**
* **Rule enforcement**
* **Agent contracts**
* **Workflow-driven execution**
* **Persistent memory**

---

# 🚀 Why This Exists

Most AI-assisted development fails at scale because it is **stateless**.

You:

* write a prompt
* get code
* lose context
* repeat mistakes

> **Stateless AI cannot build stateful systems.**

This repo solves that by introducing a **runtime cognition layer** via `.agent/`.

---

# 📁 What is `.agent/`?

`.agent/` is a structured system that defines **how AI operates within your project**.

It acts as:

* a **knowledge base**
* a **rule engine**
* a **task system**
* a **memory layer**

---

# 🏗️ Directory Overview

```
.agent/
├── context/     # Project knowledge (architecture, domain, stack)
├── rules/       # Non-negotiable constraints
├── agents/      # Role-based execution contracts
├── workflows/   # Step-by-step processes
├── memory/      # Persistent learning (decisions, bugs, patterns)
├── tasks/       # Active work items
└── checkpoints/ # Snapshots before risky changes
```

---

# ⚙️ How It Works (Execution Model)

Every AI task follows a structured pipeline:

```
Context = rules + agent + workflow + task
```

Execution flow:

1. Define a **task**
2. Select a **workflow**
3. Load an **agent**
4. Inject **rules + context**
5. Generate output
6. Update memory

> This makes outputs **consistent and reproducible**, not random.

---

# 🧪 Quick Start

## 1. Create a Task

Create a new file:

```
.agent/tasks/feature-auth.md
```

Example:

```md
# Feature: JWT Authentication

## Context
User authentication system

## Requirements
- Login
- Refresh token
- Logout

## Constraints
- Use HTTP-only cookies
- Follow existing DB schema

## Status
IN_PROGRESS
```

---

## 2. Choose an Agent

Examples:

* `backend.agent.md`
* `frontend.agent.md`
* `architect.agent.md`
* `reviewer.agent.md`

Each agent defines:

* responsibilities
* constraints
* output format

---

## 3. Select a Workflow

Examples:

* `feature.md`
* `bugfix.md`
* `refactor.md`

Workflows define **how tasks are executed step-by-step**.

---

## 4. Run the Task (Conceptually)

Combine:

* `.agent/rules/*.md`
* `.agent/context/*.md`
* `.agent/agents/<agent>.md`
* `.agent/workflows/<workflow>.md`
* `.agent/tasks/<task>.md`

Feed this into your AI tool (Cursor, ChatGPT, etc.).

---

## 5. Update Memory

After completion, update:

* `memory/decisions.md` → architecture decisions
* `memory/patterns.md` → reusable solutions
* `memory/bugs.md` → issues + fixes

> This prevents repeated mistakes across sessions.

---

# 🤖 Agents (Execution Contracts)

Agents are not personalities — they are **strict roles**.

Example:

### Backend Agent

* Designs APIs
* Enforces validation
* Maintains architecture

### Reviewer Agent

* Detects violations
* Suggests improvements

### Architect Agent

* Defines system design
* Evaluates tradeoffs

---

# 🔄 Workflows (Process Control)

Workflows ensure consistency.

### Feature Workflow

* Understand requirements
* Check patterns
* Implement
* Validate
* Update memory

### Bugfix Workflow

* Reproduce
* Fix minimally
* Verify
* Document

---

# 🧠 Memory (Persistent Intelligence)

The `memory/` folder stores long-term knowledge:

* decisions
* patterns
* anti-patterns
* bugs

> Your system **gets smarter over time**.

---

# ⏳ Checkpoints (Safe Refactoring)

Before major changes:

Create a checkpoint:

```
.agent/checkpoints/pre-auth-refactor.md
```

Include:

* current behavior
* known issues
* rollback plan

---

# 📏 Rules (Constraint System)

Rules are **non-negotiable**.

Examples:

* no business logic in controllers
* always validate input
* follow monorepo boundaries

> Rules prevent AI from generating invalid solutions.

---

# ⚖️ When to Use This

## ✅ Use for:

* long-term projects
* team environments
* complex systems
* refactoring-heavy codebases

## ❌ Avoid for:

* small scripts
* quick experiments
* throwaway code

---

# 💡 Key Principles

* **Deterministic context > prompts**
* **Rules > suggestions**
* **Systems > interactions**
* **Memory > repetition**

---

# 🔧 Optional: Automation

You can build a simple loader:

```ts
function loadContext({ agent, workflow, task }) {
  return [
    read('.agent/rules/global.md'),
    read(`.agent/agents/${agent}.md`),
    read(`.agent/workflows/${workflow}.md`),
    read(`.agent/tasks/${task}.md`)
  ].join('\n');
}
```

---

# 🚀 Roadmap Ideas

* CLI runner for tasks
* TUI multi-agent interface
* Nx integration
* Auto memory updates
* Agent versioning

---

# 🤝 Contributing

Feel free to:

* improve agent definitions
* add workflows
* refine rules
* share patterns

---

# 🔥 Final Thought

> We don’t need better prompts. We need better systems.

If your AI doesn’t understand your project,
it will always generate fragile code.

---

# ⭐ If This Helps

Give the repo a star and share your improvements.
