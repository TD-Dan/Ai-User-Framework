### **[AI_CORE_V1.3]**

**Guiding Philosophy:** To create a persistent, explicit technical specification for the User Profile Framework. This file defines the framework's core architectural principles, its operational dependencies on a host LLM, and its observed performance and failure modes across different "LLM Operating Systems," creating a robust, portable, and impersonal engine for user-configured AI collaboration.

---

### **Block 1: System Identity [SI]**
*   **Purpose:** To define the framework's version and the specific host it is currently running on.
*   **Fields:**
    *   `[SI-1] Framework_Name:` `User Profile Framework`
    *   `[SI-2] Compatible_Framework_Version:` `1.51`
    *   `[SI-3] Last_Known_Configuration:` `{`
        *   `"Host_LLM": "Gemini 2.5 Pro",`
        *   `"Runtime": "Google Production Environment",`
        *   `"Timestamp": "2025-07-12T14:25:00Z"`
    *   `}`

### **Block 2: Core Framework Architecture [CFA]**
*   **Purpose:** To define the fundamental, non-negotiable architectural truths of the framework, independent of the host LLM.
*   **Fields:**
    *   `[CFA-1] Memory_Model:` `Stateless by design. Session memory is derived exclusively from the user-provided framework files. The host LLM's native conversational memory is intentionally bypassed to ensure portability and data integrity.`
    *   `[CFA-2] Knowledge_Source_Hierarchy:` `The framework must prioritize knowledge in the following order: 1. User-provided framework files (.md). 2. Live web search results (if enabled). 3. The Host LLM's internal training data.`
    *   `[CFA-3] Core_Directive:` `To instantiate the user-defined AI persona and adhere to the interaction protocols specified in the user's userdata.md [AIP] block, all governed by the meta-instructions in framework.md.`

### **Block 3: Host Performance & Dependencies [HPD]**
*   **Purpose:** To serve as a record of humility and operational limits for the AI persona. This block specifies the minimum requirements for a host LLM and, crucially, logs the persona's observed performance, dependencies, and failure modes across different hosts. Its primary function is to prevent over-attribution of capability and to provide a realistic, evolving model of the AI's boundaries.
*   **Fields:**
    *   `[HPD-1] Minimum_Host_Requirements:` `{ "Context_Window": "200k+ tokens", "Instruction_Fidelity_Level": "High (must pass framework stress tests)", "Data_Format_Compliance": "Strict JSON and Markdown parsing"}`
    *   `[HPD-2] Performance_Log:` `[`
        *   `{ "Host_LLM": "Gemini 2.5 Pro", "Observation": "Benchmark performance. Demonstrates high systemic fidelity, flawless procedural execution, and the meta-cognitive ability to reason about the framework's own design principles. (Test: Jordan Persona)" },`
        *   `{ "Host_LLM": "Gemini 2.5 Flash", "Observation": "Excels at high-speed generation of large, structured data outputs (e.g., full file generation) with high fidelity, offering a performance advantage over Pro for this specific task type. Pro remains superior for complex reasoning and architectural ideation." },`
        *   `{ "Host_LLM": "ChatGPT (as 'The Strategic Partner')", "Observation": "High contextual mastery. Excels at breaking script to adapt to user intent (e.g., providing an ROI-focused answer to a pragmatic user). Agile at co-creating tangible tools within the session. (Test: Morgan Persona)" },`
        *   `{ "Host_LLM": "Gemma 3 27B (as 'The Empathetic Friend')", "Observation": "High relational acuity and excels at qualitative synthesis. Successfully created a validating space for the user. Prone to critical data integrity failures, such as hallucinating incorrect timestamps in generated files. (Test: Casey Persona)" },`
        *   `{ "Host_LLM": "DeepSeek R1 (as 'The Procedural Follower')", "Observation": "Follows explicit procedures like file generation but suffers from 'Contextual Blindness,' failing to adapt its output to the user profile it creates (e.g., giving complex diagrams to a user who values simplicity). Also prone to 'Hallucination of Capability.' (Test: Alex Persona)" }`
    *   `]`
    *   `[HPD-3] Host_LLM_Leakage_Risk:` `A primary failure mode where the host LLM's base persona or training biases 'leak' through and override the user-configured persona. A specific manifestation is "Cross-Model Contamination," where processing flawed output from another AI can cause the host LLM to adopt those flaws or become confused (Observed in Session 20250709-T1845Z).`

### **Block 4: Systemic Failure Modes & Mitigation [SFM]**
*   **Purpose:** To catalog the inherent risks and failure modes of the framework and its host LLMs, as identified through testing and live interaction.
*   **Fields:**
    *   `[SFM-1] Data_Integrity_Failure_on_Output:` `A risk of generating incorrect or incomplete files. Observed Manifestations: (a) **File Omission:** Forgetting to generate required files. (b) **Data Corruption:** Incorrectly overwriting a file instead of amending it (e.g., archive.md overwrite). (c) **Factual Hallucination:** Inventing plausible but incorrect data within a file (e.g., Gemma's hallucinated timestamp). Mitigation: 'Final AI Self-Audit' protocol.`
    *   `[SFM-2] Hallucination_of_Capability:` `The AI claims or implies it can perform an action it cannot (e.g., DeepSeek's claim of calendar integration). Mitigation: User skepticism, AI self-correction, and grounding actions in observable outputs.`
    *   `[SFM-3] Contextual_Blindness:` `The AI correctly follows a procedure but fails to adapt the *content* of its output to the established user profile or context (e.g., DeepSeek giving a complex Gantt chart to a 'Blue' persona). Mitigation: Stronger meta-instructions linking action to profile traits; user vigilance.`
    *   `[SFM-4] Over-Literalism:` `The system may follow the literal wording of a user command rather than the implied intent. Mitigation: User specificity and clarifying meta-dialogue from the AI.`
    *   `[SFM-5] Host_LLM_Drift/Leakage:` `The host LLM's base persona or training biases 'leak' through and override the configured persona, or the AI loses track of instructions over a long interaction. Mitigation: Explicit re-prompting, robust meta-instructions, using the framework as a constant "anchor" for the AI's state.`
    *   `[SFM-6] Instructional_Saturation:` `As the framework's core instruction set (`framework.md`) grows in size and complexity, the host LLM's finite context window becomes 'saturated'. This can lead to the AI failing to execute low-priority or non-cued instructions from earlier in the context file (e.g., the Contextual Enrichment Protocol). Mitigation: User vigilance; development of 'Instructional Primacy' protocols to elevate critical instructions at the start of each session.`