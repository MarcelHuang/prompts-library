# Prompt Engineering Resources

A curated collection of prompt engineering guides, documentation, and references from leading AI labs and community sources.

---

## Official Docs by AI Provider

### Anthropic (Claude)
- [Prompt Engineering Overview](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/overview) — Top-level guide covering the full prompting toolkit for Claude models
- [Be Clear and Direct](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/be-clear-and-direct) — Foundational technique: explicit, precise instructions
- [Use Examples (Multishot Prompting)](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/multishot-prompting) — 3–5 diverse examples for consistency and structured output
- [Let Claude Think (Chain of Thought)](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/chain-of-thought) — Step-by-step reasoning for complex tasks
- [Use XML Tags](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/use-xml-tags) — Structuring prompts with XML for clarity
- [Give Claude a Role (System Prompts)](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/system-prompts) — Shaping behavior via system-level instructions
- [Chain Complex Prompts](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/chain-prompts) — Breaking multi-step tasks into sequential subtasks
- [Use Prompt Templates and Variables](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prompt-templates-and-variables) — Separating fixed and dynamic prompt content
- [Prompt Generator (Console Tool)](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prompt-generator) — Auto-generate first-draft prompt templates
- [Prompt Improver (Console Tool)](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prompt-improver) — Automated analysis and enhancement of existing prompts
- [Claude 4 Best Practices](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/claude-4-best-practices) — Model-specific guidance for Claude Opus 4, Sonnet 4, and Haiku 4.5
- [Long Context Tips](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/long-context-tips) — Handling large documents and retrieved content
- [Extended Thinking Tips](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/extended-thinking) — Prompting strategies for extended thinking models

---

### OpenAI (GPT)
- [Prompt Engineering Guide](https://platform.openai.com/docs/guides/prompt-engineering) — Official guide covering message roles, grounding, and model-specific strategies
- [Best Practices for Prompt Engineering with the OpenAI API](https://help.openai.com/en/articles/6654000-best-practices-for-prompt-engineering-with-the-openai-api) — Practical formats and examples from OpenAI's help center
- [OpenAI Cookbook](https://cookbook.openai.com/) — Code examples, notebooks, and links to third-party resources

---

### Google (Gemini / Vertex AI)
- [What is Prompt Engineering? — Google Cloud](https://cloud.google.com/discover/what-is-prompt-engineering) — Foundational overview from Google Cloud
- [Introduction to Prompting — Vertex AI Docs](https://docs.cloud.google.com/vertex-ai/generative-ai/docs/learn/prompts/introduction-prompt-design) — Components of a prompt; system instructions; Gemini-specific guidance
- [Overview of Prompting Strategies — Vertex AI Docs](https://docs.cloud.google.com/vertex-ai/generative-ai/docs/learn/prompts/prompt-design-strategies) — Structured workflow: content, format, iteration, and debugging checklist
- [Gemini 3 Prompting Guide — Vertex AI Docs](https://docs.cloud.google.com/vertex-ai/generative-ai/docs/start/gemini-3-prompting-guide) — Model-specific tips for Gemini 3, including temperature, persona, and long-context handling
- [Best Practices for Prompt Engineering — Google Cloud Blog](https://cloud.google.com/blog/products/application-development/five-best-practices-for-prompt-engineering) — Six developer-focused best practices (contextual prompts, bias awareness, iterative testing)

---

### Microsoft (Azure OpenAI)
- [Prompt Engineering Techniques — Azure OpenAI / Microsoft Learn](https://learn.microsoft.com/en-us/azure/ai-foundry/openai/concepts/prompt-engineering?view=foundry-classic) — Prompt components, grounding, and parameter tuning for GPT models on Azure
- [System Message Design — Azure OpenAI](https://learn.microsoft.com/en-us/azure/ai-foundry/openai/concepts/advanced-prompt-engineering?view=foundry-classic) — How to design effective system prompts (metaprompts) for chat applications
- [Apply Prompt Engineering with Azure OpenAI — Microsoft Learn Training Module](https://learn.microsoft.com/en-us/training/modules/apply-prompt-engineering-azure-openai/) — Hands-on module covering model selection, deployment, and prompting on Azure

---

## Community & Academic References

### Comprehensive Guides
- [Prompt Engineering Guide — DAIR.AI (promptingguide.ai)](https://www.promptingguide.ai/) — The most widely cited community guide; covers techniques, papers, model-specific tips, and agents. Also available on [GitHub](https://github.com/dair-ai/Prompt-Engineering-Guide)
- [Learn Prompting](https://learnprompting.org/docs/introduction) — Free, open-source guide; beginner-to-advanced; co-authored with OpenAI and cited by Google, Microsoft, and Wikipedia. Backed by the 76-page *Prompt Report* (1,500+ papers analyzed)
- [IBM Think: The 2026 Guide to Prompt Engineering](https://www.ibm.com/think/prompt-engineering) — Broad practitioner guide covering techniques, context engineering, RAG, and structured inputs

### Interactive Tools & Playgrounds
- [OpenAI Playground](https://platform.openai.com/playground) — Live prompt testing with parameter controls (temperature, max tokens, etc.)
- [Anthropic Console](https://console.anthropic.com/) — Prompt generator, improver, and evaluation tool built into the Claude developer console
- [Google Cloud Vertex AI Prompt Gallery](https://docs.cloud.google.com/vertex-ai/generative-ai/docs/learn/prompts/prompt-gallery) — Pre-built prompt examples for common use cases

---

## Key Techniques Quick Reference

| Technique | What It Does |
|---|---|
| **Zero-shot prompting** | Ask the model without examples; relies on pre-trained knowledge |
| **Few-shot / Multishot prompting** | Provide 3–5 examples to guide output format and style |
| **Chain of Thought (CoT)** | Ask the model to reason step-by-step before answering |
| **System prompt / Role prompting** | Assign a persona or role via system-level instructions |
| **Prompt chaining** | Break complex tasks into sequential subtasks, passing outputs forward |
| **XML / delimiter structuring** | Use tags or separators to reduce ambiguity in prompt parsing |
| **Retrieval-Augmented Generation (RAG)** | Ground the model with external documents injected into the prompt |
| **Temperature tuning** | Lower = deterministic; higher = creative (typically 0–1 range) |
| **ReAct (Reason + Act)** | Combine internal reasoning with external tool calls (search, calculators) |

---

*Last updated: February 2026*
