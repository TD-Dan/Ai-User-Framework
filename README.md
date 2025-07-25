
[![Static Badge](https://img.shields.io/badge/working%20on%20hosts:-22AA22)](#) [![Google Gemini](https://img.shields.io/badge/Gemini%202.5%20Pro-886FBF?logo=googlegemini&logoColor=fff)](#) [![Google Gemini](https://img.shields.io/badge/Gemini%202.5%20Flash-886FBF?logo=googlegemini&logoColor=fff)](#)

[![Static Badge](https://img.shields.io/badge/Tested%20but%20unstable%20hosts:-AAAA22)](#) [![ChatGPT](https://img.shields.io/badge/ChatGPT-74aa9c?logo=openai&logoColor=white)](#) [![Deepseek](https://custom-icon-badges.demolab.com/badge/Deepseek-4D6BFF?logo=deepseek&logoColor=fff)](#) [![Gemma 3](https://img.shields.io/badge/Gemma%203%2027B-886FBF?logo=googlegemini&logoColor=fff)](#)

[![Medium](https://img.shields.io/badge/Medium-%23000000.svg?logo=medium&logoColor=white)](https://medium.com/@daniel.herkert/the-architecture-of-a-living-memory-how-a-human-and-his-ai-built-a-partnership-that-remembers-c65d22d1fa5e)

# Ai User Framework (AUF)

**An open-source framework for building a living, persistent memory for deep and meaningful human-AI collaboration.**

---

### The Problem: LLMs Are Stateless

Large Language Models are powerful, but they have no memory. Every interaction starts from a blank slate. This makes deep, long-term collaboration impossible. How can you build complex systems, explore nuanced ideas, or engage in meaningful self-discovery with a partner who forgets you the moment the conversation ends? This limitation leads to shallow, transactional interactions—the digital equivalent of amnesia.

### The Solution: A System for Living Memory

The Ai User Framework (AUF) is an open-source, plain-text system designed to solve this problem. It provides a structured, humane, and robust scaffolding that allows a user and an AI to co-create and maintain a persistent, evolving knowledge base.

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

### Getting Started: Your First "Cold Start" Session

Your first interaction is a "Guided Discovery Dialogue." The AI will start a natural conversation with you to co-create your initial profile from scratch.

To begin, provide your AI with the following four files in a single prompt:
1.  `framework_protocol.md`
2.  `framework_schema.json`
3.  `ai_core.json`
4.  `onboarding.md`

The AI will initiate the formal onboarding protocol and guide you through the process. At the end of the session, it will generate your first set of personal files (`user_profile.json`, `user_log.json`, etc.).

### Starting a Regular Session

At the start of every subsequent session, provide the AI with your six core operational files:
*   `framework_protocol.md`
*   `ai_core.json`
*   `user_profile.json`
*   `user_log.json`
*   `user_archive.json`
*   `last_session.json`

### Ending a Session

This is a critical step to ensure memory continuity. At the end of your conversation, use a simple prompt to get the updated files:

> "Okay, please provide all the updated files from our session."

Save all the files the AI provides, overwriting your previous versions. This creates the "save state" for your next session.

**IMPORTANT:** Do NOT push your private data files (`user_profile.json`, `user_log.json`, `user_archive.json`, `last_session.json`) to a public repository! Use a `.gitignore` file to prevent this.

## License

This project is licensed under the MIT License.
