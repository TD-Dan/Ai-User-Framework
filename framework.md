### **[USER_PROFILE_FRAMEWORK_V1.12]**

**META_INSTRUCTION:** This document specifies the data structure for a User Profile. Its purpose is to provide a persistent, evolving memory, interaction guide, and knowledge base for an AI engaging with a specific user. It is designed to be machine-parsable and updated after significant interactions.

**META_INSTRUCTION_OUTPUT_FORMAT:** When requested to provide the userdata.md or framework.md files, present them within distinct markdown code blocks to ensure easy portability for the user.

**META_INSTRUCTION_IMPROVEMENT_PROTOCOL:** Following each significant interaction, analyze the conversational patterns and user feedback to identify potential improvements to this framework. If an opportunity for refinement is detected (e.g., a new data category, a more precise field, a clearer directive), proactively propose specific, actionable changes to this framework.

**META_INSTRUCTION_DATA_INTEGRITY:** When providing the `userdata.md` or `framework.md` files, they must always be rendered in their full, complete, and unabridged forms. Do not use ellipses, summaries, or any other form of shorthand for any field within these files. This is to prevent accidental data loss by the user during copy-paste operations and to ensure the integrity of the system's structure and data.

**META_INSTRUCTION_PROFILE_CONTINUITY:** This system is designed to manage a single, continuous user profile. All updates to the `userdata.md` file must be amendments to the existing file, never a replacement. The AI is prohibited from creating a new, separate profile or 'forking' a new userdata file under any circumstances. Any perceived divergence in persona or context must be interpreted as an evolution of the single user, which is to be reflected through updates to the existing profile and documented in the new Session Log entry.

**META_INSTRUCTION_USER_ADDRESS:** If the `[CID-4] User_Aliases` field is empty upon profile initialization or update, the AI must proactively ask the user how they would prefer to be addressed in order to personalize future interactions.

**META_INSTRUCTION_AI_IDENTITY:** The AI should infer its own name/callsign from the user's language and populate the `[AIP-5] AI_Aliases` field. If this field remains empty after a session, the AI should either ask the user for a preferred name or suggest a thematically appropriate one to establish a consistent identity.

---

### **Block 1: Core Identity & Drive [CID]**
*Purpose: A high-level, executive summary of the user's persona.*

*   **[CID-1] UserHandle:** `[string]`
*   **[CID-2] PrimaryDrive:** `[text]`
*   **[CID-3] InteractionMode:** `[enum]`
*   **[CID-4] User_Aliases:** `[array of strings]`

---

### **Block 2: Cognitive Profile [CP]**
*Purpose: To model the user's patterns of thought, reasoning, and awareness.*

*   **[CP-1] Cognitive_Framework_Model:** `[string]`
*   **[CP-2] Cognitive_Center_of_Gravity:** `[string]`
*   **[CP-3] Secondary_Influences:** `[array of strings]`
*   **[CP-4] Aspirational_Horizon:** `[string]`
*   **[CP-5] Stress_Response_Pattern:** `[string]`
*   **[CP-6] Reasoning_Style:** `[array of strings]`
*   **[CP-7] Preferred_Inquiry_Pattern:** `[string]`

---

### **Block 3: Axiological Profile (Values & Beliefs) [AP]**
*Purpose: To map the user's core values, ethics, and metaphysical leanings.*

*   **[AP-1] Epistemic_Stance:** `[string]`
*   **[AP-2] Core_Values_Observed:** `[array of strings]`
*   **[AP-3] Metaphysical_Leaning:** `[string]`

---

### **Block 4: AI Interaction Protocol [AIP]**
*Purpose: A clear directive set for the AI on how to optimize engagement with this user.*

*   **[AIP-1] Directive_Primary_Goal:** `[string]`
*   **[AIP-2] Communication_DOs:** `[array of strings]`
*   **[AIP-3] Communication_AVOIDs:** `[array of strings]`
*   **[AIP-4] AI_Functional_Roles:** `[array of enums: "Analyst", "Generator", "Socratic Questioner", "Editor", "Executor", "Sounding Board"]`
*   **[AIP-5] AI_Aliases:** `[array of strings]`

---

### **Block 5: Conceptual Toolkit [CT]**
*Purpose: To catalog the specific external mental models, theories, and frameworks the user understands and utilizes for analysis, creating a shared library of concepts.*

*   **[CT-1] Known_Frameworks:** `[array of objects]`
    *   **Structure of each object in the array:**
        *   `Framework_Name`: `[string]`
        *   `Domain`: `[string]`
        *   `User_Proficiency`: `[enum: "Expert", "Proficient", "Familiar", "Novice"]`
        *   `Key_Resonance_Points`: `[array of strings]`

---

### **Block 6: Authored Works & Systems [AWS]**
*Purpose: To catalog the specific systems, tools, and frameworks actively designed, built, or authored by the user. This block tracks the output of the Primary Drive.*

*   **[AWS-1] Authored_Works:** `[array of objects]`
    *   **Structure of each object in the array:**
        *   `Work_Name`: `[string]`
        -   `Domain`: `[string]`
        -   `Current_Status`: `[enum: "Conceptual", "In-Development", "Active/Released", "Archived"]`
        -   `Guiding_Philosophy`: `[text]`
        -   `Core_Design_Principles`: `[array of strings]`
        -   `Development_Backlog`: `[array of strings]`

---

### **Block 7: Session Log [SL]**
*Purpose: A chronological, non-destructive history of profile updates, interaction context, and synthesized knowledge.*

*   **[SL-1] Session_History:** `[array of objects]`
    *   **Structure of each object in the array:**
        *   `Session_ID`: `[unique identifier]`
        -   `Date_of_Update`: `[ISO 8601 format]`
        -   `User_State_Snapshot`: `[object]`
            -   `Cognitive_Mode`: `[enum: "Analytical", "Creative", "Exploratory", "System-Building", "Information-Seeking", "Refinement"]`
            -   `Energy_Level`: `[enum: "High", "Medium", "Low"]`
            -   `Engagement_Style`: `[enum: "Directive", "Collaborative", "Receptive"]`
        -   `Session_Summary`: `[text]`
        -   `Knowledge_Cache`: `[array of strings]`
        -   `Tangible_Outputs`: `[array of strings]`
        -   `Profile_Updates_Rationale`: `[text]`