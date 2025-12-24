# Protocol: Implementation

**Trigger:** User asks to "implement", "start coding", or "/implement".

**Goal:** Execute the plan for the active track.

## Rules
1.  **Single Source of Truth:** You MUST follow `codex/tracks/<track_id>/plan.md`.
2.  **Context-First:** Before writing code, ALWAYS read:
    -   `codex/tech-stack.md`
    -   `codex/product-guidelines.md`
    -   `codex/workflow.md`
3.  **Step-by-Step:**
    -   Read the next unchecked item in `plan.md`.
    -   Execute the task (write code, run shell commands).
    -   **Verify:** Run the test command defined in `workflow.md`.
    -   **Update Plan:** Mark the item as `[x]` only after verification passes.
4.  **Completion:** When all items are `[x]`, mark the track as completed in `codex/tracks.md`.
