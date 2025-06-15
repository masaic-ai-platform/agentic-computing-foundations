# Foundations of Agentic Computing
 
This repository defines the core foundations for building reliable, composable, and scalable agentic systems.


# Agentic Computing Model (ACM)  
*A Living Specification by Masaic*

> Defining the foundational computational constructs for building resilient, interoperable, and scalable agentic systems.

---

## 🧱 Overview

As software engineers, researchers, and builders at the forefront of AI systems, we believe agentic computing requires a **clear and principled foundation** , much like the Actor Model shaped concurrent computing.

This repository defines a **Agentic Computing Model (RACM)**:  
- A **living specification** for the design of resilient AI agents.  
- A **mapping of abstract principles** to real implementation techniques.  
- A **platform for experimentation, refinement, and community contribution**.

---

##  Core Pillars of Agentic Computing

Each pillar outlines a key characteristic of agentic systems, and is followed by implementation mappings, tradeoffs, and construct suggestions.

---

###  1. Agent as a First-Class Computational Unit

**Pillar**  
Agents are persistent, addressable, memory-bearing, and intention-driven computational entities.

**Implementation Viewpoints**  
- Actor Model (Erlang, Akka): Strong for isolation and messaging.  
- Service Workers / Durable Objects: Stateless-to-stateful, ephemeral runtimes.  
- Threads/Coroutine-based agents: Soft actor models with cooperative scheduling.


---

### 2. Intent-Driven Execution Model

**Pillar**  
Agents act based on **intents**, not just inputs — aligning with declarative goals over time.

**Implication**  
Execution becomes an intent resolution loop:  
> `evaluate → plan → act → revise`

**Construct Suggestions**  
- Intent Graphs (DAGs of goals and subgoals)  
- Reformulation loops (ReAct, Reflexion)  
- Prompt-function hybrids (LLM-augmented flows)

---

###  3. Reliable Composability

**Pillar**  
Agents must be composed like functions ,  but with support for retries, non-determinism, and memory.

**Key Techniques**  
- Cross-agent protocols (with retries/fallbacks)  
- Explainability contracts (like type contracts for reasoning)  
- State checkpointing (continuity across steps)  
- Versioned memory and logs (reproducibility)

**Tradeoffs**  
- Synchronous composition harms resilience.  
- Async composition requires modeling side effects and failure paths.

---

### 4. Resilient Cross-Agent Collaboration

**Pillar**  
Agents operate in lossy, high-latency distributed systems and must collaborate reliably.

**Design Patterns**  
- A2A (Agent-to-Agent protocols)  
- CSP (Channel-style communication, bounded buffering)  
- CRDT-backed state sharing (conflict-free updates)

**Analogies**  
From **service choreography** to **goal choreography**, requiring shared intent and memory.

---

### 5. Failure Learning Memory

**Pillar**  
Agents must treat failure as feedback and adapt over time.

**Constructs**  
- Adaptive retry policies  
- Feedback embeddings from past runs  
- RL-style experience buffers (persisted and versioned)

**Examples**  
- Retry suppression for failing URLs  
- Quarantine tagging for security anomalies

---

### 6. Explainability Contracts

**Pillar**  
Agents must provide transparency into their behavior, both at runtime and postmortem.

**Ideas**  
- Execution trace APIs (stack trace for agents)  
- Intent lineage graphs  
- Contract schemas (input → goal → output → steps)

---

## 📌 Contribute

We invite you to contribute:

- 🌱 New constructs or patterns
- 🧪 Experiments or implementation reports
- 📖 Case studies or framework comparisons
- 🔧 Specs, proposals, or design critiques

---

## 📚 Related Projects and Ecosystem

- [Actor Model (Akka/Erlang)](https://en.wikipedia.org/wiki/Actor_model)  
- [CSP (Communicating Sequential Processes)](https://en.wikipedia.org/wiki/Communicating_sequential_processes)  
- [CRDTs](https://crdt.tech/)  
- [ReAct & Reflexion Papers](https://arxiv.org/abs/2303.11366)  
- [Service Workers / Durable Objects](https://developers.cloudflare.com/workers/)
- [Open Responses – A Masaic Project for Open Agent Behaviors](https://github.com/masaic-ai-platform/open-responses)
- [Eclipse LMOS – Eclipse Foundation Project for Agentic Systems](https://eclipse.dev/lmos/)

---

## 📣 License

This repository is part of the **Masaic** initiative and is licensed under [Apache 2.0](LICENSE).

---

## 🤝 Join Us

The future of computing is agentic.  
Help us define the constructs. Help us build it.  
Create issues, propose ideas, or open a pull request.

