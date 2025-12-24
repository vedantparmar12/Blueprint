# Protocol: Track Management

**Trigger:** User asks to "start new track", "create feature", "/newTrack", or "check status".

## Action: New Track
1.  **Analyze Context:** Read `codex/product.md` and `codex/tracks.md`.
2.  **Propose:** Suggest a track title based on the user's request.
3.  **Generate Artifacts:**
    -   Create directory `codex/tracks/<track_id>/`.
    -   Generate `spec.md` (Requirements).
    -   Generate `plan.md` (Step-by-step implementation plan).
    -   Update `codex/tracks.md` to list the new track as `[ ] Incomplete`.
4.  **Wait:** Ask user for approval of the plan before implementation.

## Action: Status
1.  **Read Registry:** Read `codex/tracks.md`.
2.  **Report:** List all tracks and their states (`[ ]`, `[~]`, `[x]`).
3.  **Detail:** If a specific track is active, summarize its `plan.md` progress.
