# Conductor Configuration for OpenAI Codex CLI

**Context-Driven Development for your Codex Terminal.**

This package configures your **OpenAI Codex CLI** to act as "The Conductor" — a proactive project manager that enforces a strict Spec -> Plan -> Implement workflow.

## What is this?

This is **NOT** a binary extension. It is a **System Context Package**.
It provides the `AGENT.md` (System Prompt) and a set of `protocols/` that teach the Codex AI how to manage a project.

## Installation

1.  Ensure you have the **OpenAI Codex CLI** installed.
2.  Copy the `codex/` directory (inside `prd/`) to the root of your project (or your Codex configuration path).
3.  **Launch Codex:**
    ```bash
    codex --context ./codex/AGENT.md
    ```
    *(Or configure your Codex CLI to load `AGENT.md` by default).*

## Workflow

Once Codex is running with this context, you can use the Conductor workflow:

1.  **Setup:** `codex > /setup`
    *   Initializes the project context (`product.md`, `tech-stack.md`).
2.  **Plan:** `codex > /newTrack "Add user login"`
    *   Generates a Spec and a Step-by-Step Plan.
3.  **Build:** `codex > /implement`
    *   Codex reads the plan and implements it step-by-step.
4.  **Verify:** `codex > /validate`
    *   Checks if the code matches the specs.

## Directory Structure

The Conductor expects (and creates) this structure:

```text
codex/
├── AGENT.md            # The Brain (System Prompt)
├── protocols/          # The Rules (Setup, Implement, etc.)
├── product.md          # Project Vision
├── tech-stack.md       # Technical Constraints
└── tracks/             # Feature Tracks (Plans & Specs)
```