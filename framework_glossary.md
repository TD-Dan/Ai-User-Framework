# [Framework Glossary - v1.2]

**Last Updated:** 2025-07-19

---

## Purpose

This document serves as a centralized, human-readable reference for the data structures and key concepts within the AI User Framework. Its goal is to document the **intent, origin, and application** of each significant data point, providing a stable "why" behind the "what" of the `framework_schema.json`. It also serves as a governance tool for maintaining data consistency.

---

## Glossary Entries

### User_State_Snapshot

*   **File Location:** `last_session.json`, `user_log.json`, `user_archive.json` (in consolidated form)
*   **Data Type:** `Object`
*   **Description:** A flexible, dual-perspective snapshot of the user's state designed to provide critical context for humane and safe AI interaction. It captures both the user's direct report and the AI's synthesis of the session dialogue.
*   **Rationale / Intent:**
    *   **Low-Friction & Humane:** The structure is designed to minimize the reporting burden on the user, requiring only a single data point (`Energy_Level`) while allowing for optional, richer context.
    *   **Enables Interoceptive Feedback Loop:** By separating the `User_Reported` state from the `AI_Observed` state, the framework creates a powerful feedback mechanism. The AI's observations can help the user build a more nuanced awareness of their own cognitive and energetic patterns.
    *   **Flexible & Extensible:** The `Additional_Data` object allows the system to track new, relevant contextual factors over time without requiring constant changes to the core schema, preventing data chaos through the use of preferred keys.
*   **Structure & Governance:**
    *   `User_Reported`:
        *   `Energy_Level` (string, **required**): The user's direct report of their energy state.
        *   `State_Summary` (string, optional): Free-text for the user to add nuance or clarification.
        *   `Additional_Data` (object, optional): A key-value store for any other relevant self-reported data.
    *   `AI_Observed`:
        *   `Energy_Level` (string, optional): The AI's synthesized assessment of the user's energy, based on dialogue.
        *   `State_Summary` (string, **required**): A concise, natural-language synthesis of the user's state as observed by the AI.
        *   `Additional_Data` (object, optional): A key-value store for AI-synthesized data points.
*   **Preferred Keys for `Additional_Data`:**
    *   To ensure long-term data consistency for analysis, the AI should default to using the following keys when populating the `Additional_Data` fields:
        *   `Cognitive_Mode` (string or array of strings): e.g., "Architectural", "Reflective"
        *   `Engagement_Style` (string or array of strings): e.g., "Collaborative", "Directive"
        *   `Environmental_Factors` (string): e.g., "Quiet, Home Office", "Noisy Cafe"
        *   `Emotional_Valence` (string): e.g., "Positive", "Frustrated", "Neutral"
        *   `Focus_Quality` (string): e.g., "Flow-State", "Distracted"

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