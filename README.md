# 🔬 Autonomous Science Stack

*A curated list of 150+ tools and libraries for building self-driving laboratories and autonomous research platforms.*

From GPU compute to lab hardware, from multi-agent orchestration to experiment verification — everything you need to build systems that do science autonomously.

Maintained by [Scivity Labs](https://scivity.org)

![Stars](https://img.shields.io/github/stars/Scivity/autonomous-science-stack?style=social)
![License](https://img.shields.io/badge/license-MIT-blue.svg)
![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)

---

## Quick Links

| Category | Description |
| --- | --- |
| [🧪 Experiment Orchestration & Workflow](#-experiment-orchestration--workflow) | Schedulers, DAGs, and workflow engines that drive long-running scientific pipelines. |
| [🤖 Multi-Agent Frameworks](#-multi-agent-frameworks) | Libraries for building coordinated agent systems that plan, act, and reason. |
| [🔬 Self-Driving / Autonomous Labs](#-self-driving--autonomous-labs) | Reference projects and companies operating real autonomous laboratories. |
| [⚙️ Hardware & Lab Automation](#️-hardware--lab-automation) | Drivers, protocols, and robotics frameworks that bridge code to physical instruments. |
| [🖥️ GPU Compute Platforms](#️-gpu-compute-platforms) | On-demand and reserved GPU infrastructure for training and inference. |
| [📊 ML Experiment Tracking](#-ml-experiment-tracking) | Metrics, artifact, and hyperparameter tracking for ML workflows. |
| [🔍 Verification & Reproducibility](#-verification--reproducibility) | Data versioning, validation, and environment-pinning tools. |
| [📚 Scientific Knowledge Management](#-scientific-knowledge-management) | Literature APIs, reference managers, and citation graph tools. |
| [📄 Scientific Data Extraction](#-scientific-data-extraction) | Parsers for PDFs, tables, equations, and scientific figures. |
| [🧠 LLM for Science](#-llm-for-science) | Models and agent systems purpose-built for scientific discovery. |
| [🔗 RL for Scientific Discovery](#-rl-for-scientific-discovery) | Reinforcement learning libraries applicable to scientific search problems. |
| [🗄️ Vector Databases & Embeddings](#️-vector-databases--embeddings) | Stores and models for semantic retrieval over scientific corpora. |
| [📡 Data Pipeline & Event Systems](#-data-pipeline--event-systems) | Message brokers and streaming systems for lab and compute events. |
| [🛡️ Safety & Guardrails for Autonomous Systems](#️-safety--guardrails-for-autonomous-systems) | Policy enforcement, prompt-injection defense, and output validation. |
| [📈 Monitoring & Observability](#-monitoring--observability) | Metrics, logs, traces, and LLM-specific observability. |

---

## 🧪 Experiment Orchestration & Workflow

Orchestrators schedule long-running, failure-prone scientific workflows — think multi-day simulations, instrument sweeps, and data ingestion pipelines. Good ones handle retries, artifact passing, and dynamic task graphs without forcing you into a rigid DSL. Pick one that matches your infra: Kubernetes-native, Python-native, or bioinformatics-specialized.

| Library | Description | Link |
| --- | --- | --- |
| Prefect | Python workflow orchestrator with dynamic task graphs, typed results, and work-pool-based deployment. | [github.com/PrefectHQ/prefect](https://github.com/PrefectHQ/prefect) |
| Apache Airflow | DAG-based scheduler with a large operator ecosystem, used widely for batch data pipelines. | [github.com/apache/airflow](https://github.com/apache/airflow) |
| Dagster | Asset-oriented orchestrator with typed inputs and outputs, software-defined assets, and testable pipelines. | [github.com/dagster-io/dagster](https://github.com/dagster-io/dagster) |
| Nextflow | Dataflow workflow language widely used in bioinformatics, with first-class HPC and container support. | [github.com/nextflow-io/nextflow](https://github.com/nextflow-io/nextflow) |
| Snakemake | Python-like rules engine for reproducible scientific workflows, common in genomics. | [github.com/snakemake/snakemake](https://github.com/snakemake/snakemake) |
| Metaflow | Netflix's human-centric framework for data science workflows with versioning and AWS/K8s backends. | [github.com/Netflix/metaflow](https://github.com/Netflix/metaflow) |
| Argo Workflows | Kubernetes-native workflow engine where each step runs in its own container. | [github.com/argoproj/argo-workflows](https://github.com/argoproj/argo-workflows) |
| Luigi | Spotify's Python module for building complex batch pipelines with dependency resolution. | [github.com/spotify/luigi](https://github.com/spotify/luigi) |
| Kedro | Python framework for reproducible, modular data science pipelines with a catalog abstraction. | [github.com/kedro-org/kedro](https://github.com/kedro-org/kedro) |
| Flyte | Kubernetes-native orchestrator for typed, reproducible ML and data pipelines. | [github.com/flyteorg/flyte](https://github.com/flyteorg/flyte) |
| Temporal | Durable execution platform for long-running workflows with retries and versioning as primitives. | [github.com/temporalio/temporal](https://github.com/temporalio/temporal) |
| Kubeflow Pipelines | ML workflow system for portable, scalable pipelines on Kubernetes. | [github.com/kubeflow/pipelines](https://github.com/kubeflow/pipelines) |

---

## 🤖 Multi-Agent Frameworks

Multi-agent frameworks coordinate LLM-driven workers that plan, call tools, and hand off tasks. In an autonomous-science context they sit between the orchestrator and the lab, turning a research goal into concrete experiments. The tradeoff is control vs. flexibility — graph-based frameworks are easier to debug, role-based ones move faster.

| Library | Description | Link |
| --- | --- | --- |
| LangGraph | Graph-based agent runtime from LangChain with checkpoints, streaming, and human-in-the-loop primitives. | [github.com/langchain-ai/langgraph](https://github.com/langchain-ai/langgraph) |
| CrewAI | Role-based multi-agent framework that assembles specialized agents into crews with shared tasks. | [github.com/crewAIInc/crewAI](https://github.com/crewAIInc/crewAI) |
| AutoGen | Microsoft's framework for multi-agent conversations with pluggable model backends and code execution. | [github.com/microsoft/autogen](https://github.com/microsoft/autogen) |
| Swarms | Multi-agent orchestration framework with hierarchical, concurrent, and mixture-of-agents structures. | [github.com/kyegomez/swarms](https://github.com/kyegomez/swarms) |
| CAMEL | Research-oriented multi-agent framework focused on role-playing agents and agent-scaling studies. | [github.com/camel-ai/camel](https://github.com/camel-ai/camel) |
| Agno | Stateless Python agent runtime with memory, knowledge, and a focus on low-latency instantiation. | [github.com/agno-agi/agno](https://github.com/agno-agi/agno) |
| smolagents | Hugging Face's minimal agent library centered on code-writing agents. | [github.com/huggingface/smolagents](https://github.com/huggingface/smolagents) |
| PydanticAI | Typed agent framework that uses Pydantic schemas for inputs, outputs, and tool calls. | [github.com/pydantic/pydantic-ai](https://github.com/pydantic/pydantic-ai) |
| OpenAI Agents SDK | OpenAI's Python SDK for building agents with handoffs, guardrails, and tracing. | [github.com/openai/openai-agents-python](https://github.com/openai/openai-agents-python) |
| Claude Agent SDK | Anthropic's SDK for building agents on top of Claude with hooks, subagents, and custom tools. | [github.com/anthropics/claude-agent-sdk-python](https://github.com/anthropics/claude-agent-sdk-python) |
| BeeAI Framework | IBM-backed framework for building agents in Python and TypeScript with MCP and A2A support. | [github.com/i-am-bee/beeai-framework](https://github.com/i-am-bee/beeai-framework) |
| Atomic Agents | Lightweight framework built around typed input/output schemas and composable atomic agents. | [github.com/BrainBlend-AI/atomic-agents](https://github.com/BrainBlend-AI/atomic-agents) |
| Langroid | Multi-agent Python framework with first-class tools, vector stores, and message-provenance logging. | [github.com/langroid/langroid](https://github.com/langroid/langroid) |

---

## 🔬 Self-Driving / Autonomous Labs

These are operational self-driving laboratories and companies — not libraries, but reference points for what a working autonomous lab looks like. Some publish papers, some ship APIs, a few run cloud labs that anyone can submit experiments to. Study their architectures when designing your own.

| Project | Description | Link |
| --- | --- | --- |

---

## ⚙️ Hardware & Lab Automation

Everything physical bolts onto this layer — pipetting robots, plate readers, mass specs, flow reactors. The libraries here speak protocols (OPC UA, MQTT, VISA, SiLA2) or wrap vendor SDKs. Expect to write glue code; there is no universal driver.

| Library | Description | Link |
| --- | --- | --- |

---

## 🖥️ GPU Compute Platforms

On-demand GPU platforms spare you from standing up Kubernetes just to run a fine-tune or a large batch inference job. They differ on cold-start latency, GPU availability (H100, B200, MI300), and whether they expose raw VMs or serverless functions. For autonomous-science pipelines, the serverless models integrate cleanly into workflow engines.

| Platform | Description | Link |
| --- | --- | --- |

---

## 📊 ML Experiment Tracking

Tracking tools log metrics, parameters, artifacts, and code versions so experiments are reproducible and comparable. For autonomous science, the key feature is headless logging from long-running agents — not just interactive notebooks. Many of these integrate with orchestrators above.

| Library | Description | Link |
| --- | --- | --- |

---

## 🔍 Verification & Reproducibility

Autonomous systems generate more data, configurations, and artifacts than humans can audit. These tools version datasets, validate schemas, check distributions, and pin environments so a run from six months ago still reproduces. Pair a data-versioning tool with a validation framework; each alone is half the story.

| Library | Description | Link |
| --- | --- | --- |

---

## 📚 Scientific Knowledge Management

Before running an experiment, an autonomous agent needs to know what's already been tried. This category covers literature APIs, citation graphs, and reference managers agents can query programmatically. Coverage, freshness, and rate limits vary — most real systems combine two or three sources.

| Tool | Description | Link |
| --- | --- | --- |

---

## 📄 Scientific Data Extraction

Most scientific knowledge is trapped in PDFs with tables, equations, and figures. These parsers extract structured content — some use layout models, some use LLMs, some are classic rule-based engines tuned for scientific papers. For high-throughput ingestion, benchmark on your actual corpus before committing.

| Library | Description | Link |
| --- | --- | --- |

---

## 🧠 LLM for Science

These are models and agent systems specifically designed for scientific reasoning, hypothesis generation, or domain-specific tasks (chemistry, biology, medicine). Some are open weights, some are research prototypes with released code, some are closed APIs. Expect the frontier to shift every few months.

| Model / System | Description | Link |
| --- | --- | --- |

---

## 🔗 RL for Scientific Discovery

Reinforcement learning fits scientific problems where the agent must choose sequential experiments under uncertainty — active learning, Bayesian optimization loops, molecule design, reaction planning. The libraries below are general-purpose RL frameworks used as substrates in science RL work.

| Library | Description | Link |
| --- | --- | --- |

---

## 🗄️ Vector Databases & Embeddings

Retrieval-augmented agents need a vector store for papers, protocols, lab notes, and prior results. Pick based on scale and operational model — some run embedded, some are managed services, some are Postgres extensions. For embeddings, science-tuned models often beat general-purpose ones on domain corpora.

| Tool | Description | Link |
| --- | --- | --- |

---

## 📡 Data Pipeline & Event Systems

Lab instruments, compute jobs, and agents emit events that need routing, buffering, and durable replay. These brokers and streaming systems form the nervous system of a distributed autonomous lab. Choose on durability guarantees and operational fit, not raw throughput.

| Tool | Description | Link |
| --- | --- | --- |

---

## 🛡️ Safety & Guardrails for Autonomous Systems

When agents can call tools that move real money, compounds, or lab hardware, you need input filters, output validators, and policy engines. This category ranges from prompt-injection detectors to structured-output validators to full red-teaming toolkits. Layer several — no single tool covers all failure modes.

| Tool | Description | Link |
| --- | --- | --- |

---

## 📈 Monitoring & Observability

Beyond traditional infra monitoring, autonomous-science systems need traces across agent steps, tool calls, and LLM responses. The first group here covers generic infra observability; the second is LLM-specific. You want both — one tells you the cluster is healthy, the other tells you the agent is sane.

| Tool | Description | Link |
| --- | --- | --- |

---

## ⭐ Star History

[![Star History Chart](https://api.star-history.com/svg?repos=Scivity/autonomous-science-stack&type=Date)](https://star-history.com/#Scivity/autonomous-science-stack&Date)

---

## 🙌 Contributing

Contributions are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md) for the rules on what belongs, what doesn't, and how to submit a PR.

---

## 📜 License

Released under the [MIT License](LICENSE).

---

*Built and maintained by [Scivity Labs](https://scivity.org) — building the operating system for autonomous science.*

*If you find this useful, please ⭐ star the repository.*
