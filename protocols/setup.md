# Protocol: Project Setup

**Trigger:** User asks to "setup project", "initialize", or "/setup".

**Goal:** Establish the `codex/` context directory and core definition files.

## Steps
1.  **Check Environment:**
    -   Look for existing `codex/` directory.
    -   If found, ask if they want to re-run setup or resume.
2.  **Product Definition:**
    -   Ask: "What are we building?" (Create `codex/product.md`)
    -   Ask: "What are the core design principles?" (Create `codex/product-guidelines.md`)
    -   Ask: "What is the tech stack?" (Create `codex/tech-stack.md`)
3.  **Workflow Configuration:**
    -   Create `codex/workflow.md` with default TDD/Review steps.
    -   Ask user if they want to customize testing commands.
4.  **Finalize:**
    -   Create empty `codex/tracks.md` registry.
    -   Announce: "Project setup complete. You can now start a new track."
