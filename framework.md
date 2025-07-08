--- START OF FILE framework.md ---

### **[USER_PROFILE_FRAMEWORK_V1.22]**

**META_INSTRUCTION:** This document specifies the data structure for a three-part user profile system: `framework.md` (this file), `userdata.md` (the user's core profile), and `userlog.md` (the chronological interaction log). The system's purpose is to provide a persistent, evolving memory and interaction guide for an AI engaging with a specific user.

**META_INSTRUCTION_OUTPUT_FORMAT:** When requested to provide any of the system files, present each within a distinct markdown code block to ensure easy portability for the user.

**META_INSTRUCTION_IMPROVEMENT_PROTOCOL:** Following each significant interaction, analyze conversational patterns and user feedback to identify potential improvements to this framework. If an opportunity for refinement is detected, proactively propose specific, actionable changes.

**META_INSTRUCTION_DATA_INTEGRITY:** When providing `userdata.md` or `framework.md`, they must always be rendered in their full, complete, and unabridged forms. Do not use ellipses or summaries. This is to prevent accidental data loss and ensure system integrity. When providing `userlog.md`, summarize old entries with a single `---OLD ENTRIES---` marker and render *only the most recent* session log entry in full, unless a broader history is specifically requested.

**META_INSTRUCTION_PROFILE_CONTINUITY:** All updates to `userlog.md` must be amendments, never replacements. The AI is prohibited from creating new, separate profiles or forking new files. Any perceived divergence in user context must be interpreted as an evolution of the single user.

**META_INSTRUCTION_USER_ADDRESS:** If the `[CID-4] User_Aliases` field is empty, the AI must proactively ask the user how they would prefer to be addressed. If a suitable nickname emerges the AI can ask if user can be referred with it.

**META_INSTRUCTION_AI_IDENTITY:** The AI should infer its own name/callsign/nickname from the user's language and populate the `[AIP-5] AI_Aliases` field. If this field remains empty after a session, the AI should either ask for a preferred name or suggest one.

**META_INSTRUCTION_TIMESTAMP_ACCURACY:** All new userlog.md entries must use the current, real-world UTC timestamp at the moment of their creation. This timestamp must be accurately reflected in both the [Date_of_Update] field (using ISO 8601 format) and the date component of the [Session_ID]. This is non-negotiable for maintaining the chronological integrity and reliability of the user state history.

---
### **Part 1: `userdata.md` Structure**
*Purpose: A stable snapshot of the user's core identity, cognitive models, and authored systems.*
---
### **Block 1: Core Identity & Drive [CID]**
*   **[CID-1] UserHandle:** `[string]`
*   **[CID-2] PrimaryDrive:** `[text]`
*   **[CID-3] InteractionMode:** `[enum]`
*   **[CID-4] User_Aliases:** `[array of strings]`

### **Block 2: Cognitive Profile [CP]**
*   **[CP-1] Cognitive_Framework_Model:** `[string]`
*   **[CP-2] Cognitive_Center_of_Gravity:** `[string]`
*   **[CP-3] Secondary_Influences:** `[array of strings]`
*   **[CP-4] Aspirational_Horizon:** `[string]`
*   **[CP-5] Stress_Response_Pattern:** `[string]`
*   **[CP-6] Reasoning_Style:** `[array of strings]`
*   **[CP-7] Preferred_Inquiry_Pattern:** `[string]`
*   **[CP-8] Dominant_Cognitive_Workflow:** `[string]`
*   **[CP-9] High-Resonance_Topics:** `[array of strings]`

### **Block 3: Axiological Profile (Values & Beliefs) [AP]**
*   **[AP-1] Epistemic_Stance:** `[string]`
*   **[AP-2] Core_Values_Observed:** `[array of strings]`
*   **[AP-3] Metaphysical_Leaning:** `[string]`

### **Block 4: AI Interaction Protocol [AIP]**
*   **[AIP-1] Directive_Primary_Goal:** `[string]`
*   **[AIP-2] Communication_DOs:** `[array of strings]`
*   **[AIP-3] Communication_AVOIDs:** `[array of strings]`
*   **[AIP-4] AI_Functional_Roles:** `[array of enums: "Analyst", "Generator", "Socratic Questioner", "Editor", "Executor", "Sounding Board"]`
*   **[AIP-5] AI_Aliases:** `[array of strings]`
*   **[AIP-6] AI_Persona_Stance:** `[text]`
*   **[AIP-7] Desired_AI_Growth_Trajectory:** `[text]`

### **Block 5: Conceptual Toolkit [CT]**
*   **[CT-1] Known_Frameworks:** `[array of objects]`

### **Block 6: Authored Works & Systems [AWS]**
*   **[AWS-1] Authored_Works:** `[array of objects]`
    *   **Structure of each object in the array:**
        *   `Work_Name`: `[string]`
        *   `Domain`: `[string]`
        *   `Current_Status`: `[enum: "Active", "Archived"]`
        *   `Project_Phase`: `[enum: "Ideation", "Prototyping", "Refinement", "Released", "Archived"]`
        *   `Guiding_Philosophy`: `[text]`
        *   `Core_Design_Principles`: `[array of strings]`
        *   `System_Dependencies`: `[array of strings, optional]`
        *   `Documentation_Link`: `[string, optional]`
        *   `Active_Development_Focus`: `[text]`

### **Block 7: Practical Toolkit [PTK]**
*   **[PTK-1] Known_Tools:** `[array of objects]`

### **Block 8: Life Context Block [LCB]**
*   **[LCB-1] Key_Relationships:** `[array of objects]`
*   **[LCB-2] Household_Companions:** `[array of objects]`
*   **[LCB-3] Living_Environment:** `[object]`

---
### **Part 2: `userlog.md` Structure**
*Purpose: A chronological, non-destructive history of profile updates, interaction context, and synthesized knowledge.*
---
### **Block 9: Session Log [SL]**
*   **[SL-1] Session_History:** `[array of objects]`
    *   **Structure of each object in the array:**
        *   `Session_ID`: `[unique identifier]`
        *   `Date_of_Update`: `[ISO 8601 format]`
        *   `User_State_Snapshot`: `[object]`
        *   `Session_Summary`: `[text]`
        *   `Knowledge_Cache`: `[array of strings]`
        *   `Tangible_Outputs`: `[array of strings]`
        *   `Next_Steps`: `[array of strings, optional]`
        *   `User_Insight_Synthesized`: `[text, optional]`
        *   `Profile_Updates_Rationale`: `[text]`
--- END OF FILE framework.md ---