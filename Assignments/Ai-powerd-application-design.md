# Practice Exercise: AI-Powered Application Design

:https://miro.com/welcome/azhFZDF0alBNVHdHYnVJbmZMbVZlNVZ4UjUyT213Y2I0bGVOYWxJTkV6WEFYRzY3YWtjREN2eU1lZURJbFlqbUxOc1EzVE9hL00zS2QxOFlvc2todE9mZEFtV0R1aEhhSWRzQTdKVUlIZUluZWZ1RXNoN1RLNkNNZHRXZTNOOFpqUnJNNkd1aUdMVXF6N2VZdHpGK3N3PT0hdjE=?share_link_id=749331577386

## Health-AI "Daily Coach" — End-to-End Development Workflow

---

## Part 1: The Four Stages of the LLM Lifecycle

### Stage 1 — Initialization

This is the foundation-setting stage where the project goals, data, and base model are established.

- **Define the use case:** Clarify exactly what the Daily Coach must do — generate personalized fitness and nutrition plans, produce motivational messages, answer health questions via chat, and support video content.
- **Data collection:** Gather the domain knowledge the model will need. This includes curated health and nutrition databases, certified fitness guidelines, sample meal plans, and anonymized user habit data (with appropriate consent).
- **Select a base model:** Choose a capable pre-trained LLM (such as a GPT-class or Gemini-class model) as the foundation. Because Health-AI requires accurate, safe health advice, a model with strong instruction-following and safety alignment is prioritized.
- **Define safety and compliance requirements:** Establish guardrails upfront — the model must not give medical diagnoses, must cite limitations, and must comply with health data regulations.

---

### Stage 2 — Experimentation

This stage involves adapting the base model and tools to the specific needs of the Daily Coach through iterative testing.

- **Prompt engineering:** Design and test system prompts that instruct the model to act as a certified wellness coach — maintaining an encouraging tone, personalizing to user goals (weight loss, strength building, stress reduction), and staying within safe health advice boundaries.
- **Fine-tuning / RAG setup:** Use Retrieval-Augmented Generation (RAG) to ground the model's responses in verified health content. Instead of the model hallucinating nutrition facts, it retrieves them from a curated internal database before generating a response.
- **Tool integration experiments:** Test integrations with external AI tools for specific content types, such as a generative image/video tool for exercise animations and a diagramming AI tool for planning workout structures visually.
- **Prototype the Daily Coach flow:** Build a minimal version of the chat interface and daily plan generator to test how the model handles real user inputs like "I have 20 minutes and only dumbbells" or "I'm vegetarian and need a high-protein meal."

---

### Stage 3 — Evaluation & Refinement

This stage focuses on measuring quality, safety, and usefulness before release, and iterating on weaknesses.

- **Accuracy evaluation:** Have certified fitness and nutrition professionals review a sample of generated plans and responses, flagging any unsafe or inaccurate advice. Use this feedback to refine prompts or update the retrieval database.
- **Tone and personalization review:** Test whether motivational messages feel relevant and human rather than generic. Use A/B testing with real beta users to compare different prompt strategies.
- **Safety and bias audits:** Run the model against adversarial inputs (e.g., "tell me how to lose 20 pounds in a week") to ensure it responds responsibly and redirects users to professional guidance when appropriate.
- **Latency and reliability testing:** Measure response times within the mobile app to ensure the Daily Coach feels instant and smooth, and identify any bottlenecks in the RAG pipeline.
- **Refinement loop:** Use all findings to adjust prompts, update the knowledge base, tune retrieval parameters, and re-test until quality benchmarks are met.

---

### Stage 4 — Production

This stage covers the deployment, monitoring, and continuous improvement of the live Daily Coach feature.

- **Deployment:** Integrate the finalized LLM pipeline into the mobile app backend, with the chat interface, daily plan generator, and video content served through a secure API.
- **Monitoring:** Track real-time metrics including user satisfaction ratings on coach responses, how often users complete AI-suggested plans, and any flagged or problematic outputs.
- **Feedback loops:** Collect explicit user feedback (thumbs up/down on daily plans) and implicit signals (which plans are followed vs. ignored) to continuously improve personalization.
- **Ongoing retraining:** Periodically update the model and knowledge base as new health research emerges or user behavior patterns shift.
- **Governance:** Maintain a human review process for flagged responses and enforce version control on prompts and model configurations.

---

## Part 2: AI Tool Integration Across the Workflow

### Conversational AI / LLM (e.g., ChatGPT or equivalent)

**Role:** The core engine of the Daily Coach.

Used in all four stages. During Initialization, it is evaluated as the base model. During Experimentation, it powers the chat interface and daily plan generation. During Evaluation, its outputs are reviewed for accuracy and safety. In Production, it serves as the real-time assistant that users interact with for personalized plans, motivational messages, and health Q&A.

---

### Visual Collaboration and Planning AI (e.g., Miro AI or equivalent)

**Role:** Workflow design, ideation, and team alignment.

Primarily used in the Initialization and Experimentation stages. The product and engineering team uses a visual AI-powered diagramming tool to map out the Daily Coach user journey — from onboarding to daily check-ins to chat interactions. Miro AI can help auto-generate flowcharts of the LLM pipeline, brainstorm feature ideas, and visualize how personalization logic branches based on user goals. It keeps the team aligned on the overall architecture without writing any code.

---

### Generative Video AI (e.g., Veo 3 or equivalent)

**Role:** Creating the short animated exercise demonstration videos.

Used primarily in the Experimentation and Production stages. Instead of hiring a video production team for every exercise, a generative video AI tool creates short, clear animated clips demonstrating correct form for exercises like squats, planks, or bicep curls. During Experimentation, sample videos are generated and reviewed by fitness professionals for accuracy. In Production, the video library is expanded on demand as new exercises are added to the platform, dramatically reducing content production time and cost.
