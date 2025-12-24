# OpenAI Codex Agentic Framework


This is a specialized configuration and protocol suite for the **OpenAI Codex CLI**. It transforms the standard Codex session into an autonomous, agentic project manager that follows a strict **Context-Driven Development** methodology.

## Why use this?

Standard AI coding often leads to "spaghetti context" where the AI forgets project goals or writes code that doesn't align with your tech stack. This framework solves that by:

1.  **Enforcing Structure:** The AI cannot write code without first generating a Specification (`spec.md`) and a phased Plan (`plan.md`).
2.  **Persistent Context:** It maintains a `codex/` directory in your project root which acts as the "Source of Truth" for your Product Vision, Tech Stack, and Workflow.
3.  **Autonomous Implementation:** Using the `/implement` command, the agent works through your task list, verifies its own work, and only marks tasks as complete when they meet the project standards.
4.  **Native Integration:** Built specifically for the Codex CLI ecosystem, utilizing native features like `/diff`, `/compact`, and `codex cloud`.

## How to Connect to Codex CLI

To use this framework, you need to load the `AGENT.md` file as the system context when launching your Codex session.

### Method 1: Direct Launch (Recommended)
Run this command from your project root:
```bash
codex --context ./prd/codex/AGENT.md
```

### Method 2: Global Configuration
If you want Codex to always use this agent, you can point your Codex global config to the `AGENT.md` path.

## Workflow Commands

Once the session is active, the Agent recognizes several "Virtual Commands" to manage your project:

| Command | Action |
| :--- | :--- |
| `/setup` | Initialize the project (Product goals, Tech stack, Workflow). |
| `/newTrack` | Start a new feature or bug fix (Generates Spec & Plan). |
| `/implement` | Autonomous coding (Codex works through the active plan). |
| `/status` | View progress of all tracks and project health. |
| `/validation` | Validate that the implemented code matches the PRD/Specs. |

## Project Structure

When initialized, the framework manages the following structure in your project:

```text
codex/
├── AGENT.md            # System Instructions
├── protocols/          # Operational Protocols
├── product.md          # High-level Product Requirements
├── tech-stack.md       # Languages, Frameworks, and Tools
├── workflow.md         # Testing and Deployment rules
└── tracks/             # Feature-specific Plans and Specs
```

---
*Created by Vedant Parmar.*
