# [Framework Glossary - v1.0]

**Last Updated:** 2025-07-17

---

## Purpose

This document serves as a centralized, human-readable reference for the data structures and key concepts within the AI User Framework. Its goal is to document the **intent, origin, and application** of each significant data point, providing a stable "why" behind the "what" of the `framework_schema.json`.

---

## Glossary Entries

### Next_Session_Vector
*   **File Location:** `last_session.json`
*   **Data Type:** `Object`
*   **Description:** A transient, tactical object generated at the conclusion of a session. It acts as a cognitive bridge, providing a clear, actionable set of proposals and reminders to smooth the transition into the next session.
*   **Rationale / Intent:**
    *   **Cognitive Friction Damper:** Its primary purpose is to reduce the cognitive load required for the user and AI to re-orient themselves at the start of a new session, preventing loss of momentum.
    *   **Tactical vs. Strategic:** The vector is explicitly **tactical** (for the *next* session only). This keeps the strategic, long-term `Project_Backlog` in `user_profile.json` clean and focused, preventing it from being cluttered with immediate, short-term tasks.
    *   **State-Aware Handoff:** It includes a `State_Check_Advisory` to ensure the AI's initial approach in the next session is appropriate to the user's concluding energy and cognitive state from the previous one.
*   **Properties:**
    *   `Primary_Focus_Proposal` (string): Suggests the most logical high-level task.
    *   `Open_Loops_to_Close` (array of strings): Lists specific, unresolved minor items.
    *   `Review_and_Validate` (array of strings): Lists new artifacts or principles that need confirmation.
    *   `State_Check_Advisory` (string): A note on the user's concluding state for the next AI instance.
