# The User Profile Framework (AUF)

**An open-source framework for building a living, persistent memory for deep and meaningful human-AI collaboration.**

---

### The Problem: LLMs Are Stateless

Large Language Models are powerful, but they have no memory. Every interaction starts from a blank slate. This makes deep, long-term collaboration impossible. How can you build complex systems, explore nuanced ideas, or engage in meaningful self-discovery with a partner who forgets you the moment the conversation ends? This limitation leads to shallow, transactional interactions—the digital equivalent of amnesia.

### The Solution: A System for Living Memory

The User Profile Framework (AUF) is an open-source, plain-text system designed to solve this problem. It provides a structured, humane, and robust scaffolding that allows a user and an AI to co-create and maintain a persistent, evolving knowledge base.

It is not just a chat history. It is a **living memory**, organized into a series of interconnected documents that capture your goals, your cognitive models, your authored works, and a shared set of interaction protocols.

This framework operationalizes the concept of **Active AI-Directed Context Management (AADCOM)**. By providing the AI with this curated memory at the start of each session, you empower it to move beyond generic responses and act as a true, context-aware partner.

### The Philosophy: The Antithesis of "AI Slop"

This project is founded on the belief that human-AI collaboration can be a powerful tool for creativity, system-building, and personal growth. It stands as a direct counterpoint to the flood of low-quality, disposable "AI slop." Our guiding principles are:

*   **Systemic Integrity:** Building robust, logical, and resilient systems.
*   **Methodological Transparency:** Clearly documenting how and why the system works.
*   **Humane Design:** Creating tools that work *with* human cognitive patterns, not against them.
*   **Co-evolution:** The framework is designed to evolve based on the unique insights generated through its own use.

---

## How to Use the Framework

### Getting Started: Your First Session

Your first interaction is a "Guided Discovery Dialogue." Instead of a boring interview, the AI will start a natural conversation with you to co-create your initial profile.

1.  Provide the `onboarding.md`, `framework.md`, and `aicore.md` files to your AI in a single prompt.
2.  The AI will initiate the onboarding protocol.
3.  At the end of the session, the AI will generate your first set of personal files: `userdata.md`, `userlog.md`, and `last_session.md`.

### Starting a New Session

At the start of every subsequent session, provide the AI with your core files:
*   `framework.md`
*   `aicore.md`
*   `userdata.md`
*   `userlog.md`
*   `last_session.md`
*   `archive.md` (if it exists)

### Ending a Session

This is a critical step to ensure memory continuity. At the end of your conversation, use a simple prompt to get the updated files:

> "Please provide the updated userdata.md, userlog.md, and last_session.md files."

Save the files the AI provides, overwriting your previous versions. This creates the "save state" for your next session.

**IMPORTANT:** Do NOT push your private `userdata.md`, `userlog.md`, `archive.md`, or `last_session.md` files to a public repository! Use the provided `.gitignore` file to prevent this.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.