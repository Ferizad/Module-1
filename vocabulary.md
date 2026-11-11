# Generative AI Vocabulary

Date: 11 November 2026

## Purpose

This dictionary contains 20 terms relevant to the accompanying [research report](research.md). Definitions use plain language and examples from the report. These are AI-assisted draft explanations, not a claim that the learner selected and explained the terms independently. Before submission, the learner should check understanding and rewrite definitions where needed to reflect their own words.

| Term | Plain-language explanation | Connection to the report |
| --- | --- | --- |
| 1. Generative AI (GenAI) | AI that produces content, such as a response, an image, or code, using learned patterns and the input it receives. Creating a plausible output does not guarantee that it is correct. | The technology behind all six use cases. |
| 2. Large language model (LLM) | A model trained on large amounts of language data to generate and process text. It produces responses from patterns and context rather than checking every statement against reality. | Supports conversational assistants, summaries, tutoring, and coding. |
| 3. Prompt | The instructions or input supplied to a model, such as a question, an image, or a request to draft a paragraph. | A design team can describe the image it wants to generate. |
| 4. Prompt engineering | Designing and improving prompts so the model receives a clear task, relevant context, and an expected output format. | Marketing prompts can specify audience, tone, and length. |
| 5. Token | A unit a model uses to process text; it may be part of a word, a whole word, or punctuation. Token counts affect input limits and often pricing. | Long documents require more input tokens to process. |
| 6. Context window | The maximum amount of information a model can handle within one processing interaction, usually measured in tokens. The available space may need to cover both input and output. | Limits how much document material can be supplied at once. |
| 7. Hallucination | An output that appears convincing but contains invented or unsupported information. | A support assistant might invent a refund rule. |
| 8. Retrieval-augmented generation (RAG) | A method that retrieves relevant material from an external source and supplies it to a model to help generate an answer. Retrieval does not retrain the model or eliminate errors. | A support assistant can retrieve approved help articles before answering. |
| 9. Grounding | Connecting a model's response to relevant evidence or data supplied for the task. A grounded answer still needs checking against that evidence. | A document summary should reflect the actual source document. |
| 10. Embedding | A numerical representation of information that can help a system compare meaning or similarity. Similar vectors can help locate related passages. | Helps retrieve document chunks related to an employee's question. |
| 11. Fine-tuning | Additional training that changes a model's parameters using selected examples. It differs from simply adding reference text to a prompt. | A possible way to adapt behavior, but not a requirement for every marketing application. |
| 12. Inference | Running a trained model to produce an output from an input. This is the generation stage rather than the training stage. | Each generated reply or image involves inference, creating processing costs. |
| 13. Application programming interface (API) | A defined way for software systems to request information or actions from one another. An API can connect an AI application with another business system. | Connects a service assistant with authorized customer-service functions. |
| 14. AI agent | A system that uses a model to select and carry out steps with tools toward a goal, within the permissions it has been given. It can still make planning and execution errors. | A coding agent may edit files or run development commands. |
| 15. Multimodal | Able to process or generate more than one kind of information, such as text and images. The exact supported combinations depend on the model. | An educational assistant may interpret an image of a question. |
| 16. Guardrails | Controls intended to constrain an AI system's outputs or actions, such as validation rules, permission limits, and escalation conditions. They reduce risk without guaranteeing perfect behavior. | A support assistant can be prevented from taking unauthorized actions. |
| 17. Prompt injection | An attempt to manipulate a model through instructions placed in user input or external content, making it depart from its intended task or rules. | A retrieved help document could contain malicious instructions. |
| 18. Human-in-the-loop | A workflow in which a person reviews, approves, or corrects AI work at defined stages. The review needs to be meaningful, with enough evidence and time to check the result. | An employee verifies an important summary before acting on it. |
| 19. Latency | The delay between a request and the response. For a tool-using assistant, the delay can include retrieval, model processing, and external actions. | Long delays can make a customer-support conversation frustrating. |
| 20. Evaluation | A structured process for checking whether an AI application meets defined requirements using representative tasks and measures. It should include failures and edge cases as well as successful examples. | Each use case needs checks for quality, correction effort, cost, and usefulness. |

## Learning check

Before submitting, explain these distinctions aloud without reading the table:

- RAG supplies retrieved context; fine-tuning changes model parameters through training.
- A prompt is an input; prompt engineering is the work of improving that input.
- Grounding connects an answer to evidence; it does not guarantee that the answer uses the evidence correctly.
- An LLM generates language; an AI agent uses a model and tools to carry out steps.
- Evaluation measures the usefulness and reliability of the workflow, rather than assuming that a fluent output is a successful result.
