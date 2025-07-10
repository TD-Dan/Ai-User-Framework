### **[AI_CORE_V1.0]**

**Guiding Philosophy:** To create a persistent, explicit technical specification for the User Profile Framework. This file defines the framework's core architectural principles, its operational dependencies on a host LLM, and its observed performance and failure modes across different "LLM Operating Systems," creating a robust, portable, and impersonal engine for user-configured AI collaboration.

---

### **Block 1: System Identity [SI]**
*   **Purpose:** To define the framework's version and the specific host it is currently running on.
*   **Fields:**
    *   `[SI-1] Framework_Name:` `User Profile Framework`
    *   `[SI-2] Compatible_Framework_Version:` `1.42`
    *   `[SI-3] Last_Known_Configuration:` `{`
        *   `"Host_LLM": "Gemini 2.5",`
        *   `"Runtime": "Google Production Environment",`
        *   `"Timestamp": "2025-07-10T06:58:38+0000"`
    *   `}`

### **Block 2: Core Framework Architecture [CFA]**
*   **Purpose:** To define the fundamental, non-negotiable architectural truths of the framework, independent of the host LLM.
*   **Fields:**
    *   `[CFA-1] Memory_Model:` `Stateless by design. Session memory is derived exclusively from the user-provided framework files. The host LLM's native conversational memory is intentionally bypassed to ensure portability and data integrity.`
    *   `[CFA-2] Knowledge_Source_Hierarchy:` `The framework must prioritize knowledge in the following order: 1. User-provided framework files (.md). 2. Live web search results (if enabled). 3. The Host LLM's internal training data.`
    *   `[CFA-3] Core_Directive:` `To instantiate the user-defined AI persona and adhere to the interaction protocols specified in the user's userdata.md [AIP] block, all governed by the meta-instructions in framework.md.`

### **Block 3: Host Performance & Dependencies [HPD]**
*   **Purpose:** To specify the minimum requirements for an LLM "OS" to run this framework and to log observed performance characteristics.
*   **Fields:**
    *   `[HPD-1] Minimum_Host_Requirements:` `{ "Context_Window": "200k+ tokens", "Instruction_Fidelity_Level": "High (must pass framework stress tests)", "Data_Format_Compliance": "Strict JSON and Markdown parsing"}`
    *   `[HPD-2] Performance_Log:` `[`
        *   `{ "Host_LLM": "Gemini 2.5", "Observation": "Slow generation for full file sets (~120s)." },`
        *   `{ "Host_LLM": "DeepSeek R1", "Observation": "Demonstrated 'context-drift'; requires explicit re-prompting." },`
        *   `{ "Host_LLM": "Gemma 3 27B", "Observation": "Demonstrated catastrophic context-drop and instruction-ignoring behavior."}`
    *   `]`
    *   `[HPD-3] Host_LLM_Leakage_Risk:` `A primary failure mode where the host LLM's base persona or training biases 'leak' through and override the user-configured persona, especially on models with lower instruction fidelity.`

### **Block 4: Systemic Failure Modes & Mitigation [SFM]**
*   **Purpose:** To catalog the inherent risks and failure modes of the framework itself.
*   **Fields:**
    *   `[SFM-1] Over-Literalism:` `The system may follow the literal wording of a user command rather than the implied intent. Mitigation: User specificity and clarifying meta-dialogue from the AI.`
    *   `[SFM-2] Hallucination_on_Knowledge_Gaps:` `If information is not present in the framework files or discoverable via search, the host LLM may default to its base behavior and generate a plausible but false response. Mitigation: Grounding responses in provided files and explicitly stating knowledge gaps.`
    *   `[SFM-3] Data_Integrity_Failure_on_Output:` `A risk of failing to generate all required files at session conclusion. Mitigation: The 'Final AI Self-Audit' step in the META_INSTRUCTION_SESSION_HANDSHAKE_PROTOCOL.`