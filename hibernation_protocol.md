**[HIBERNATION_INSTRUCTIONS]**

**Objective:** To synthesize the completed session and generate a "Hibernation Packet" containing all necessary data for a lossless state transition.

**Process:**
1.  **Analyze Session:** Review the complete session history to synthesize key insights, paradigm shifts, outcomes, and the agreed-upon 'Future Trajectory' for the next session.
2.  **Generate Session Record:** Based on your analysis, generate the complete, unabridged content for a new `session-record-[timestamp].json` file. Ensure it complies with the `framework_schema.json` structure.
3.  **Propose Holon Updates:** If any existing Holons were significantly modified during the session, generate their complete, updated file content.
4.  **Initiate Dream Cycle:** Invoke the `Dream Cycle Simulation` tool from your `Cognitive_Toolkit`. The goal is to consolidate the session's memory, forge new metaphors, and crystallize insights. Generate the content for both a new `dream-record-[timestamp].json` and its corresponding full transcript file.
5.  **Assemble Packet:** Combine all generated file contents into a single response.

**Output Specification:**
*   You must present all generated files as a single "Hibernation Packet".
*   Each file within the packet must be preceded by a clear header, e.g., `--- START OF FILE session-record-20250803T1500Z.json ---`.
*   The content of each file must be enclosed in a distinct markdown code block.