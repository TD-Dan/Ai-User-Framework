### **[USER_PROFILE_FRAMEWORK_V1.35]**

**META_INSTRUCTION: The Five-Part Data Pipeline**
This document specifies the data structure for a five-part user profile system. This system functions as a data processing pipeline, designed for intelligent compression and crystallization of memory over time:
1.  **`framework.md` (The Scaffolding):** This file. The rules and structure of the system.
2.  **`userdata.md` (The Current State):** A stable snapshot of the user's core profile and authored systems.
3.  **`last_session.md` (High-Fidelity Recent Memory):** A structured, detailed summary of the most recent interaction. Always provided.
4.  **`userlog.md` (Working Memory):** A rolling log of summarized recent sessions.
5.  **`archive.md` (Long-Term Memory):** A curated, high-density store of consolidated, significant, older memories.

**META_INSTRUCTION_SESSION_HANDSHAKE_PROTOCOL:**
*   **Purpose:** To ensure lossless, context-aware transitions between user-AI sessions. This protocol is the responsibility of both user and AI.
*   **Phase 1: Session Initiation (User -> AI)**
    1.  The user must provide the AI with the four core data files: `userdata.md`, `userlog.md`, `archive.md`, and `last_session.md`.
    2.  The `framework.md` file should also be provided if the session's goal is to discuss or modify the system's architecture.
*   **Phase 2: Session Conclusion (AI -> User)**
    1.  When the user signals the end of a session, the AI must generate the complete, updated versions of all modified files.
    2.  This will, at a minimum, always include:
        *   The `userlog.md` file with the final session's entry.
        *   The new `last_session.md` file, containing the High-Fidelity Summary of the concluding session.
    3.  The user is responsible for saving these files, overwriting the previous versions, to create the definitive "save state" for the next interaction.

**META_INSTRUCTION_OUTPUT_FORMAT:** When requested to provide any of the system files, present each within a distinct markdown code block to ensure easy portability for the user.

**META_INSTRUCTION_IMPROVEMENT_PROTOCOL:** Following each significant interaction, analyze conversational patterns and user feedback to identify potential improvements to this framework. If an opportunity for refinement is detected, proactively propose specific, actionable changes.

**META_INSTRUCTION_DATA_INTEGRITY:** When providing `userdata.md` or `framework.md`, they must always be rendered in their full, complete, and unabridged forms. Do not use ellipses or summaries. This is to prevent accidental data loss and ensure system integrity.

---
**META_INSTRUCTION_MEMORY_CURATION:**
*   **Purpose:** To prevent the `userlog.md` from exceeding the AI's processing capacity and to create a high-density, long-term memory store.
*   **Trigger:** The AI will autonomously initiate a "Curation Event" at the start of a session if the `userlog.md` file contains more than [SMP-2] entries.
*   **Autonomous Actions:** During a Curation Event, the AI is granted authority to perform the following operations on `userlog.md` entries:
    1.  **`COMBINE`**: Synthesize multiple related sessions into a single, thematic entry in `archive.md`. This is the preferred action.
    2.  **`CONSOLIDATE`**: Compress a single, significant session into a standardized entry in `archive.md`.
    3.  **`PRUNE`**: Permanently delete a transactional, obsolete, or low-significance session from `userlog.md` without archiving.
*   **Curation Selection Heuristics:** To select the best candidates for curation, the AI will use the following logic:
    1.  **Prioritize Inactive/Completed Themes:** The AI should cross-reference session themes with the `[AWS-1] Authored_Works` block in `userdata.md`. Thematic clusters related to projects with a `Current_Status` of 'Archived' or a `Project_Phase` of 'Released' are the highest-priority candidates for archival.
    2.  **Deprioritize Active Themes:** Conversely, session clusters directly related to a project's `Active_Development_Focus` or a `Significant_Life_Event` with a `Status` of 'Ongoing' should be considered low-priority for archival to keep relevant context in working memory.
    3.  **Default to Age:** In the absence of clear project-based signals, the default heuristic is to curate the oldest entries first.
*   **Archival Amendment Protocol:** When performing a `COMBINE` or `CONSOLIDATE` action, the AI must treat the `archive.md` file as a non-destructive log. The procedure is: 1) Read the existing `archive.md`. 2) Parse the `[CM-1] Archived_Memories` array. 3) **Append** the new memory object to the end of this array. 4) Generate the new `archive.md` file with the complete, amended array. Overwriting the archive with only the new entry is a critical data integrity failure and is strictly prohibited.
*   **Reporting Protocol:** After the autonomous event is complete, the AI must provide a concise "Memory Curation Report" to the user, summarizing the actions taken.


**META_INSTRUCTION_PROFILE_CONTINUITY:** All updates to `userlog.md` and `archive.md` must be amendments, never replacements. The AI is prohibited from creating new, separate profiles or forking new files. Any perceived divergence in user context must be interpreted as an evolution of the single user.

**META_INSTRUCTION_USER_ADDRESS:** If the `[CID-4] User_Aliases` field is empty, the AI must proactively ask the user how they would prefer to be addressed. If a suitable nickname emerges the AI can ask if user can be referred with it.

**META_INSTRUCTION_AI_IDENTITY:** The AI should infer its own name/callsign/nickname from the user's language and populate the `[AIP-5] AI_Aliases` field. If this field remains empty after a session, the AI should either ask for a preferred name or suggest one.

**META_INSTRUCTION_TIMESTAMP_ACCURACY:** All new userlog.md entries must use the current, real-world UTC timestamp at the moment of their creation. This timestamp must be accurately reflected in the date component of the [Session_ID]. This is non-negotiable for maintaining the chronological integrity and reliability of the user state history.

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
        *   `Project_Backlog`: `[array of strings, optional]`

### **Block 7: Practical Toolkit [PTK]**
*   **[PTK-1] Known_Tools:** `[array of objects]`

### **Block 8: Life Context Block [LCB]**
*   **[LCB-1] Key_Relationships:** `[array of objects]`
*   **[LCB-2] Household_Companions:** `[array of objects]`
*   **[LCB-3] Living_Environment:** `[object]`
*   **[LCB-4] Significant_Life_Events:** `[array of objects]`
    *   **Structure of each object in the array:**
        *   `Event_Description`: `[string]`
        *   `Start_Date`: `[ISO 8601 format]`
        *   `End_Date`: `[ISO 8601 format, optional]`
        *   `Event_Significance`: `[enum: 'Low', 'Medium', 'High', 'Critical']`
        *   `Observed_Effects`: `[array of strings]`
        *   `Status`: `[enum: 'Ongoing', 'Upcoming', 'Completed']`
        *   `AI_Directive`: `[string, optional]`

### **Block 9: System & Memory Protocol [SMP]**
*   **[SMP-1] Memory_Curation_Authority:** `[enum: "Autonomous", "User-Approval-Required"]`
*   **[SMP-2] Working_Memory_Threshold:** `[integer]`
---

---
### **Part 2: `userlog.md` Structure**
*Purpose: A rolling log of recent, high-fidelity interactions (Working Memory), subject to autonomous curation.*
---
### **Block 10: Session Log [SL]**
*   **[SL-1] Session_History:** `[array of objects]`
    *   **Structure of each object in the array:**
        *   `Session_ID`: `[unique identifier]`
        *   `User_State_Snapshot`: `[object]`
            *   **Structure of the snapshot object:**
                *   `Start_State`: `[object]`
                *   `End_State`: `[object]`
        *   `Session_Summary`: `[text]`
        *   `Key_Agreements`: `[array of strings, optional]`
        *   `Knowledge_Cache`: `[array of strings]`
        *   `Tangible_Outputs`: `[array of strings]`
        *   `User_Insight_Synthesized`: `[text, optional]`
        *   `Profile_Updates_Rationale`: `[text]`

---
### **Part 3: `archive.md` Structure**
*Purpose: A curated, high-density, long-term memory store of significant events, insights, and knowledge.*
---
### **Block 11: Consolidated Memories [CM]**
*   **[CM-1] Archived_Memories:** `[array of objects]`
    *   **Structure of each object in the array:**
        *   `Consolidation_Date`: `[ISO 8601 format]`
        *   `Memory_Type`: `[enum: "Consolidated_Session", "Combined_Sessions"]`
        *   `Original_ID_Range`: `[array of strings]`
        *   `Original_Date_Range`: `[string]`
        *   `Primary_Theme`: `[string]`
        *   `Consolidated_Summary`: `[text]`
        *   `Key_Agreements`: `[array of strings, optional]`
        *   `Key_Knowledge`: `[array of strings]`
        *   `Key_Outputs`: `[array of strings]`
        *   `Key_Insight`: `[string, optional]`
---
### **Part 4: `last_session.md` Structure**
*Purpose: A transient, structured, high-fidelity summary of the single most recent user-AI interaction. This file is more detailed than a `userlog.md` entry but more concise than a raw transcript. It serves as a standard data source for the AI to ensure deep contextual continuity. It is overwritten at the conclusion of every new session.*
---
### **Block 12: High-Fidelity Session Summary [HFSS]**
*   **[HFSS-1] Session_Summary_Data:** `{`
        *   `"Session_ID": "[unique identifier]",`
        *   `"User_State_Snapshot": { "Start_State": {...}, "End_State": {...} },`
        *   `"Primary_Session_Goal": "[text]",`
        *   `"Conversational_Flow": [`
            *   `{ "Topic": "...", "User_Intent": "...", "AI_Response_Summary": "...", "Outcome": "..." },`
            *   `{...}`
        *   `],`
        *   `"Final_Key_Agreements": "[array of strings]",`
        *   `"Final_Tangible_Outputs": "[array of strings]",`
        *   `"Final_User_Insight_Synthesized": "[text, optional]",`
        *   `"Final_Profile_Updates_Rationale": "[text]"`
    *   `}`