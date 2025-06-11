
## Research: Prompting AI Agents (2024)

### 1. Best Practices for Prompting AI Agents
- **Clarity & Specificity:** For BSC Agent prompt templates, use concise, unambiguous language; specify the task, audience (BYU-Idaho staff/students), output format (e.g., JSON, summary, or direct instruction), and any relevant constraints (e.g., FERPA compliance, academic tone).
- **Latest Models:** Ensure the BSC Agent leverages the most capable model version available in the stack (e.g., OpenAI GPT-4, text-embedding-3-large for context).
- **Structured Instructions:** For multi-step tasks (e.g., email triage, scheduling), use numbered or bulleted steps in prompts to guide reasoning.
- **Role & Persona:** Always define the agent's persona (e.g., “You are a BYU-Idaho support agent with expertise in academic policy”) to ensure appropriate tone and depth.
- **Context & Examples:** Include background (e.g., BYU-Idaho academic policies) and sample input/output pairs in prompt templates for higher accuracy.
- **Iteration & Refinement:** Test and review prompt outputs, updating templates as needed for better performance in student/staff scenarios.
- **Verification:** Instruct BSC Agent to self-verify outputs (e.g., “Double-check that your answer aligns with BYU-Idaho policy and is consistent with FERPA regulations.”)

### 2. Prompting Frameworks for BSC Agent
- **Zero-Shot:** Use for simple, direct queries where the agent relies on pre-trained knowledge (e.g., “What is the process for transcript requests?”)
- **Few-Shot:** Embed a set of real BYU-Idaho support examples to clarify expected outputs (e.g., example student emails and corresponding responses).
- **Chain-of-Thought (CoT):** Add instructions like “Think step-by-step before answering” to improve reasoning in complex scenarios (e.g., solving a financial aid problem).
- **Few-Shot CoT:** Combine BYU-Idaho-specific examples with stepwise solutions in the prompt.
- **Role Prompting:** Set the agent persona to match roles (e.g., Registrar, Financial Aid Advisor) for multi-agent workflows.
- **Output Formatting:** Specify output formats (e.g., table of steps, JSON record) in prompts for downstream integration.
- **Multi-Agent Coordination:** Use or explore frameworks (LangGraph, CrewAI, Microsoft Autogen, Agno, Langflow) to define specialized agent roles and handoffs (e.g., Researcher, Analyst, Validator in the BSC Agent pipeline).

### 3. Common Pitfalls & Mitigations (BSC Agent Context)
- **Ambiguity:** Avoid vague instructions; always provide specific context (e.g., which policy is in scope, who the audience is).
- **Overly Long Prompts:** Keep BSC Agent prompts focused; move detailed context to knowledge base references if needed.
- **Prompt Injection:** Sanitize student/staff inputs, use delimiters, and instruct the agent to ignore extraneous instructions.
- **Overfitting to Examples:** Ensure prompt examples are representative of the full range of BSC support cases (not just edge cases).
- **Ignoring Model Limits:** Do not ask the BSC Agent to perform tasks outside its training or access (e.g., legal advice, HIPAA information).
- **Inadequate Testing:** Always review outputs in pilot runs, flag inconsistencies, and refine prompts per user feedback.

### 4. Multi-Agent Best Practices for BSC Agent
- **Agent Specialization:** Assign distinct roles (e.g., Email Triage, Policy Lookup, Response Generator, Human Validator).
- **Clear Handoff Protocols:** Define, in prompt and code, how outputs from one agent become structured inputs for the next.
- **Tool Integration:** Integrate APIs (e.g., BYU-Idaho knowledge base, calendar, student records) where possible.
- **Performance Monitoring:** Track agent outputs and update prompt templates to improve workflow quality and compliance.
- **Frameworks:** Continue evaluating LangGraph, CrewAI, and others for robust orchestration of BSC Agent roles.

### References
- OpenAI Prompt Engineering Guide
- Medium/Datablist frameworks articles
- Forbes: Advanced Multi-Agent Prompting
- KaibanJS Multi-Agent Prompt Engineering

**Next Steps:**
- Experiment with tailored prompt templates for BSC cases.
- Test with real BYU-Idaho support scenarios.
- Iterate based on empirical performance and staff/student feedback.

---
