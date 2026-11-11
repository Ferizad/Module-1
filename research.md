# Research on Generative AI Applications

Prepared for the introductory GenAI course assignment  
Date: 11 November 2026

## Scope and approach

Generative AI (GenAI) creates content such as text, code, and images from learned patterns and supplied instructions. A large language model (LLM) is one type of model used in text-based applications. This report examines six practical use cases. Product descriptions are based on the official sources linked below; business benefits, implementation challenges, and suggested evaluation measures are analytical judgments, not independently measured results. No hands-on product testing was performed for this report. Features and access depend on the product plan and configuration.

## 1. Customer support and service assistants

**Application and business value.** A GenAI assistant can interpret a customer's question, draft a relevant response, and explain a company's published guidance in conversational language. For example, it could help a customer understand a returns policy before escalating an unusual request to an employee. Retrieval-augmented generation (RAG) can supply relevant knowledge-base passages as context for the answer. Potential business value includes faster responses, consistent handling of routine questions, and more staff time for difficult cases. Useful evaluation measures include correct resolution rate, escalation quality, customer satisfaction, and cost per correctly resolved case.

**Technical challenges and weak points.** Implementation requires current source documents, reliable retrieval, customer authentication where needed, and integration with service systems through an application programming interface (API). Latency matters during live conversations. A hallucination could produce an invented policy, and prompt injection could attempt to make the assistant ignore its instructions or expose information. Guardrails should constrain actions and information access, while uncertain or sensitive cases should go to a person. A fluent answer is not evidence of a correct resolution; a high automated closure rate can hide unresolved problems.

**Existing implementation:**

- [Intercom Fin AI Agent](https://www.intercom.com/help/en/articles/7120684-fin-ai-agent-explained) — A customer-service AI agent that generates responses using configured support knowledge and can hand conversations over to human teams.

## 2. Document summarization and workplace knowledge assistance

**Application and business value.** GenAI can turn long reports and conversations into summaries, extract action items, and help employees locate relevant information. For example, a project manager could request a summary of a project document and then check the original passages before making decisions. Grounding answers in authorized source material can improve relevance. Potential value includes reduced reading time and faster preparation for meetings. Evaluation should consider factual consistency, coverage of important details, source traceability, and time saved after verification.

**Technical challenges and weak points.** Documents must be parsed accurately, divided into useful chunks when necessary, and retrieved with their access permissions intact. Embeddings can help match a question with related passages, but semantic similarity does not guarantee relevance. A context window limits how much material a model can process at once, and token volume affects processing cost. Summaries may omit exceptions, merge contradictory statements, or assign an action to the wrong person. Sensitive documents also require protection against data leakage. Human-in-the-loop review is especially important when a summary informs consequential decisions.

**Existing implementation:**

- [Microsoft 365 Copilot](https://www.microsoft.com/en-us/microsoft-365-copilot/business) — A workplace assistant offering document drafting, editing, and summarization within supported Microsoft 365 experiences.

## 3. Software development and code assistance

**Application and business value.** A coding assistant can suggest code, explain unfamiliar functions, draft documentation, and help developers investigate defects. For example, a developer could ask it to draft a data-validation function, then inspect and test that function against real requirements. Potential benefits include faster prototyping and less repetitive coding. The appropriate evaluation is whether reviewed code behaves correctly and is maintainable, rather than how many lines the assistant generates. Teams can measure task completion time, defects, review effort, and security findings.

**Technical challenges and weak points.** The assistant needs relevant repository context, accurate requirements, and compatibility with existing dependencies. When an AI agent can run commands or edit files, its tool permissions must be limited to the intended task. Generated code may call nonexistent APIs, introduce vulnerabilities, or pass a simple test while failing edge cases. Suggestions can also create licensing or provenance questions that need review. Developers should inspect changes and use meaningful tests and security checks; accepting a suggestion transfers responsibility for its behavior to the development team.

**Existing implementation:**

- [GitHub Copilot](https://docs.github.com/en/copilot/get-started/about-github-copilot) — An AI coding assistant with features for code suggestions, conversational help, and supported agent-based development workflows.

## 4. Education, tutoring, and lesson preparation

**Application and business value.** GenAI can draft lesson resources, propose differentiated explanations, and support tutoring through questions and hints. For example, a teacher could request three explanations of the same mathematical concept and adapt them for different learners. A tutor can ask a learner to explain a step rather than immediately reveal an answer. Potential institutional value includes reduced preparation time and more opportunities for individual practice. Evaluation should examine curriculum alignment, accuracy, accessibility, teacher editing time, and learning demonstrated without AI assistance.

**Technical challenges and weak points.** Educational systems need age-appropriate responses, reliable subject content, and careful handling of student information. Multimodal systems may interpret text and images, but can still misread a diagram or handwritten calculation. Hallucination and bias can create incorrect or culturally unsuitable examples. Another weak point is overreliance: completing a task with AI does not prove the student understands it. Teacher review, clear rules for permitted assistance, and assessment of independent work remain necessary. Automated feedback should support professional judgment rather than determine high-stakes grades by itself.

**Existing implementation:**

- [Khanmigo by Khan Academy](https://www.khanacademy.org/khanmigo) — An AI tutor and teaching assistant designed to guide learners with prompts and support teachers with resources such as lesson plans and rubrics.

## 5. Marketing copy and content adaptation

**Application and business value.** GenAI can draft promotional text, generate alternative headlines, and adapt a message for different audiences or formats. For example, a small business could turn an approved product description into several draft social posts while retaining the same factual claims. Prompt engineering can specify audience, tone, length, and required information. Potential value includes faster production of alternatives and easier reuse of approved material. Evaluation should consider factual accuracy, brand consistency, editing effort, and audience response to approved content.

**Technical challenges and weak points.** The application needs trustworthy product information and explicit constraints on claims. Fine-tuning may help adapt a model's behavior in some settings, but it is not automatically necessary; clear instructions and approved reference material may be sufficient. Generated copy can invent features, repeat stereotypes, or sound generic. Translation and localization can also lose meaning or cultural nuance. Human editors must check claims and suitability before publication. Producing more content creates little business value if the material is inaccurate or fails to serve its audience.

**Existing implementation:**

- [Canva Magic Write within Magic Studio](https://www.canva.com/newsroom/news/magic-studio/) — A writing tool that helps draft, summarize, expand, and adapt text within Canva's content-creation workflow.

## 6. Visual design and image generation

**Application and business value.** Generative image tools can turn a text prompt into a draft illustration or modify part of an existing image. For example, a design team could explore alternative campaign concepts before investing in final production. These tools can reduce the time spent preparing early visual options and make experimentation more accessible. Evaluation should consider adherence to the brief, visual quality, brand consistency, revision effort, and suitability for the intended publication. Faster generation is useful only when it reduces the total time needed to produce an acceptable asset.

**Technical challenges and weak points.** Achieving a precise layout, consistent characters, or accurate product details can require repeated generation and manual editing. Model outputs may contain distorted objects, misleading details, or unwanted associations. Teams need to review the provenance of inputs and the applicable terms for the particular model and output; access to a commercial tool is not a universal guarantee of legal clearance. Generated images are also a weak choice for exact charts, scientific diagrams, or evidence of real events, because visual plausibility does not establish factual accuracy.

**Existing implementation:**

- [Adobe Firefly](https://helpx.adobe.com/firefly/web/get-started/learn-the-basics/adobe-firefly-faq.html) — A generative creative application offering tools for creating and editing visual content from prompts and reference material.

## Cross-case implementation priorities

1. Define a narrow user problem and the standard of an acceptable result.
2. Identify approved data sources and enforce access permissions.
3. Build a small evaluation set containing ordinary tasks, ambiguous requests, and failure cases.
4. Compare quality, latency, total cost, and human correction effort with the existing workflow.
5. Add guardrails and human review in proportion to the consequences of an error.
6. Monitor failures after deployment and update sources and instructions as needed.

GenAI is most useful when the whole workflow produces a better result. Fluency, output volume, and automation alone do not demonstrate business value.

## Source and authorship note

The six linked official sources document the example products; they do not independently validate the benefits proposed in this report. This report was drafted with AI assistance. The analysis presents potential uses and implementation considerations rather than claims of personal deployment experience. Related terminology is explained in [vocabulary.md](vocabulary.md).
