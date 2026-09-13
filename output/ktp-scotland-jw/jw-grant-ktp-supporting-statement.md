# Supporting statement: KTP Associate - AI Software Engineering

## Essential criteria

### Qualifications

I am completing an MSc in Advanced Computer Science at Queen Mary University of London in September 2026, supported by a BSc in Computer Science and more than 6 years of professional software engineering experience. I also completed the Nebius Academy AI Engineering Fellowship, an intensive programme covering LLM architectures, AI agents, MLOps, distributed training, and GPU performance engineering. During the fellowship, I built more than 12 working systems on Nvidia H100 infrastructure and tested the behaviour, reliability, and performance of each implementation.

### Programming experience

I have substantial programming experience in Python, Java, and JavaScript/TypeScript. At Mastercard, I built React and TypeScript frontends, Java and Spring backend services, REST APIs, and event-driven services using Kafka. I led the architecture of a microfrontend platform that enabled more than 10 product teams to deploy modules independently. I also owned testing, Jenkins delivery pipelines, monitoring, and production incident response. This background means I can take a system through design, implementation, testing, deployment, and operational support.

During the Nebius Fellowship, I used Python to build transformers, agent workflows, training pipelines, and inference experiments. I containerised training jobs with Docker, deployed distributed training across 2 Nvidia H100 nodes using Kubernetes and SkyPilot, and used CUDA events and `torch.profiler` to investigate performance bottlenecks.

### Large language models and open-source AI frameworks

I have direct experience with large language models and open-source AI tools including PyTorch, Transformers, LangGraph, LangChain, Chroma, Rasa, FastAPI, and Scikit-learn. I built a transformer language model from scratch, implementing causal self-attention, feed-forward layers, autoregressive generation, and KV caching. I verified causality through targeted tests rather than assuming the architecture behaved correctly.

I implemented LoRA fine-tuning on GPT-2 by freezing 124 million base parameters and training around 811,000 adapter parameters, or 0.65% of the model. This produced a 3 MB adapter rather than a 500 MB full checkpoint. I also rebuilt the inference loop around KV caching and preallocated sequence buffers, reducing generation time for 128 tokens from 0.943 seconds to 0.141 seconds on H100 infrastructure.

### Database systems and integration

My database experience includes PostgreSQL, Oracle, MongoDB, Redis, and vector databases. At Mastercard, I used PostgreSQL JSONB to support configurable forms without requiring a database migration whenever business teams introduced a field. I built database-backed services with Spring Data JPA and Hibernate and used Kafka for asynchronous, auditable communication between services. I have also used Chroma to store embeddings for a RAG-based internal documentation search system.

### Technical writing, reports, and documentation

I have published more than 40 technical articles covering AI, system design, observability, databases, testing, and distributed infrastructure. My work has appeared in industry newsletters, including the eBPF newsletter. Writing regularly has trained me to explain technical decisions, limitations, and trade-offs to readers with different levels of technical knowledge.

At Mastercard, I wrote company-wide whitepapers on accessibility and microfrontend architecture. They received CTO recognition, were circulated to 200 engineers, and became internal reference material. I have also delivered seminars on Kafka architecture, Kafka Streams, Kafka Connect, AMQP, Git, and version-control practices. This experience prepares me to write the KTP's technical and non-technical reports, documentation, case studies, conference material, and academic publications.

These examples fit the KTP's aim of joining data, AI agents, and existing business workflows. They also show how I work: I build working systems, add controls around failure and unsupported output, measure the result, and explain the design in plain language to the people who will use it. I am comfortable working directly with technical specialists, managers, and staff across operational teams. I can communicate progress clearly while adapting technical decisions to operational needs and user feedback.

## Desirable criteria

### Doctoral qualification and academic capability

I do not hold a PhD. I do, however, bring current postgraduate study, the Nebius AI Engineering Fellowship, and a record of independently investigating technical questions through implementation and measurement. For example, I compared pre-norm and post-norm transformer behaviour, tested whether Rotary Position Embeddings preserved vector norms to within `1e-5`, and ran hyperparameter searches across learning rate and batch size. My 40-plus articles also show that I can turn technical investigation into structured written material suitable for wider dissemination.

### Integrating LLMs through APIs, prompting, and fine-tuning

My Repository Summarizer is a FastAPI service that uses LLMs to produce readable summaries of GitHub repositories. It extracts code structure through AST and Tree-sitter, prioritises source files, and assembles useful context within a 7,000-token limit. This work required me to manage the interface between application code, model input, context selection, and generated output.

I have also used LLM APIs and prompt-based workflows through LangGraph, LangChain, and Rasa. My LoRA work gives me direct fine-tuning experience at model level. I understand the practical choices between prompting, retrieval, tool use, deterministic business logic, and parameter-efficient fine-tuning. I select the method according to the task, the evidence available, the risk of unsupported output, and the cost of running the system.

### RAG, agentic AI, and MCP

I built a RAG-based internal documentation search system using LangChain and Chroma. The system chunked and embedded internal documents, retrieved relevant passages, and returned grounded answers with source references. This gave me practical experience of preparing data for retrieval, connecting a vector database to an LLM workflow, and making the source of an answer visible to the user.

For agentic AI, I built a LangGraph ReAct research agent that planned and executed its own tool calls. I added a dataflow integrity check that compared every numerical claim in the final response with the tool log, catching unsupported claims before they reached the user. I also built a Rasa CALM booking flow in which Python enforced rules such as deposit caps, party-size limits, and time cut-offs, keeping commercial decisions auditable.

I designed an MCP shared tool layer so LangGraph, Rasa, and a voice pipeline could discover and call the same tools without duplicating business logic. Changing a venue's availability through the shared layer updated every client immediately. I then connected the exploratory and deterministic agents through an atomic handoff mechanism that allowed a rejected option to trigger a fresh search safely.
