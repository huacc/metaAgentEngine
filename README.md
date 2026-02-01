# Meta-Agent Engine

English | [简体中文](README_CN.md)

<div align="center">

**Building a Sustainable Long-Running Agent Collaboration Framework**

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![GitHub Stars](https://img.shields.io/github/stars/huacc/metaAgentEngine.svg)](https://github.com/huacc/metaAgentEngine/stargazers)
[![GitHub Issues](https://img.shields.io/github/issues/huacc/metaAgentEngine.svg)](https://github.com/huacc/metaAgentEngine/issues)

</div>

---

## 📖 Introduction

**Meta-Agent Engine** is an innovative agent orchestration framework designed to build **sustainable, long-running** agent collaboration systems. Unlike traditional single-agent or simple multi-agent systems, this project implements a "system that produces agents" — through the collaboration of meta-agents, it automatically produces, assembles, and optimizes business agents and their collaboration workflows.

### Core Philosophy

> **"Not using AI to do things, but using AI to build AI that can do things"**

This project draws inspiration from the "mother machine" concept in industrial manufacturing and the "compiler" architecture in software engineering, enabling agent systems to have self-production, self-optimization, and self-evolution capabilities.

---

## ✨ Key Features

### 🎯 Automated Agent Production

- **Intent Understanding**: Transform vague user requirements into structured agent blueprints
- **Best Practice Injection**: Automatically retrieve industry standards and best practices to ensure professional and reliable agents
- **Asset Reuse**: Intelligently match existing agent templates to avoid reinventing the wheel
- **Quality Assurance**: Built-in evaluation mechanism to ensure produced agents meet quality standards

### 🧬 Hierarchical Derivation Mechanism

Support hierarchical agent derivation, from general to specialized:

```
L0 (General) → L1 (Domain) → L2 (Specialized) → L3 (Sub-specialized)
Example: Doctor → Internal Medicine Doctor → Gastroenterologist → Endoscopy Specialist
```

**Derivation Formula**: `Derived Agent = Inheritance(Parent Capabilities) + Specialization(Domain Knowledge) + Constraints(Boundary Limits)`

### 🔄 Continuous Learning & Optimization

- **Memory System**: Long-term storage of knowledge, experience, and user preferences
- **Pattern Recognition**: Extract successful patterns from historical executions
- **Auto-Optimization**: Continuously optimize prompts and collaboration workflows based on feedback

### 🧩 Flexible Composition

- **Agent Composition**: Support multiple agent collaboration patterns (serial, parallel, hybrid)
- **Skill Integration**: Flexible combination of built-in and external skills
- **MCP Protocol**: Support standard MCP tool integration
- **Tool Extension**: Integrate various external APIs and custom tools

### 👤 Personal Knowledge Base

- **Knowledge Priority**: Personal Knowledge > System Assets > Internet Information
- **Multi-source Learning**: Support active injection, interactive learning, feedback learning, and behavior observation
- **Personalized Customization**: Customize agent behavior based on user habits and preferences

---

## 🏗️ System Architecture

### Meta-Agent System (8 Core Roles)

The system defines 8 meta-agents, organized into 4 functional groups:

| Group | Role | Core Responsibility |
|-------|------|---------------------|
| **Intelligence** | Researcher | Retrieve external best practices and industry standards |
| | Asset Manager | Manage internal agent templates and prompt components |
| **Design** | Architect | Decompose intent and design agent blueprints |
| | Weaver | Write system prompts and give agents their "soul" |
| **Execution** | Choreographer | Design collaboration topology (DAG/State Machine) |
| | Orchestrator | Runtime scheduling and context management |
| **Operations** | Evaluator | Quality assessment with final veto power |
| | Learner | Extract patterns from history for continuous optimization |

### Collaboration Workflow

```
User Intent
  ↓
[Researcher + Asset Manager] (Intelligence Gathering)
  ↓
[Architect] (Architecture Design)
  ↓
[Weaver + Choreographer] (Instantiation)
  ↓
[Orchestrator] (Execution)
  ↓
[Evaluator] (Evaluation)
  ↓
[Learner] (Learning & Optimization)
```

### Standard Agent Structure

Each agent contains 6 core components:

1. **Meta Information**: ID, name, version, status
2. **Role Definition**: Role description, capability boundaries
3. **Prompt**: System prompt template
4. **Skills**: Internal skills, external skills
5. **I/O Contract**: Input specification, output specification
6. **Constraints**: What it can do, what it cannot do

---

## 🚀 Quick Start

### Requirements

- Python 3.9+
- Supported LLMs: GPT-4, Claude 3.5, Gemini, etc.
- (Optional) Vector Database: FAISS, Chroma, etc.

### Installation

```bash
# Clone the repository
git clone https://github.com/huacc/metaAgentEngine.git
cd metaAgentEngine

# Install dependencies
pip install -r requirements.txt

# Configure environment variables
cp .env.example .env
# Edit .env file and fill in your API keys
```

### Quick Example

```python
from meta_agent_engine import MetaAgentEngine

# Initialize the engine
engine = MetaAgentEngine()

# Produce agents
result = engine.produce(
    user_query="I want to build an intelligent medical consultation system",
    domain="Healthcare"
)

# Get produced agents
agents = result.agents
workflow = result.workflow

# Execute task
output = engine.execute(agents, workflow, user_input="I have a headache")
```

---

## 📚 Documentation

- [Methodology](docs/方法论/元智能体引擎方法论.md): Complete system design methodology (Chinese)
- [API Documentation](docs/api/): Detailed API usage guide (In Development)
- [Examples](examples/): Usage examples for various scenarios (In Development)
- [Contributing Guide](CONTRIBUTING.md): How to contribute to the project

---

## 🎯 Use Cases

### Validated Scenarios

- **Medical Consultation System**: Automatically generate triage agents, inquiry agents, diagnosis agents, and collaboration workflows
- **Code Security Audit**: Automatically generate scanner agents, analyzer agents, fix recommendation agents, and audit workflows
- **Software Development Process**: Automatically generate requirement analysis, architecture design, code implementation agents

### Potential Scenarios

- Legal consultation systems
- Investment analysis systems
- Content creation systems
- Business process automation
- Educational tutoring systems

---

## 🤝 Contributing & Recruitment

We welcome all forms of contributions! We especially welcome experts in the following areas:

### 🔍 Recruitment Areas

| Area | Description |
|------|-------------|
| **Large Language Models** | LLM applications, model fine-tuning, prompt engineering |
| **Prompt Engineering** | Advanced prompt design, few-shot learning, CoT optimization |
| **Game Engines** | Real-time system design, state machines, event-driven architecture |
| **Digital Transformation** | Enterprise digitalization, process optimization, knowledge management |
| **Ontology Methodology** | Knowledge graphs, ontology modeling, semantic reasoning |

### How to Contribute

1. Fork this repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

For detailed contribution guidelines, please refer to [CONTRIBUTING.md](CONTRIBUTING.md)

---

## 📧 Contact Us

- **Project Lead**: dongbeiler@gmail.com
- **GitHub Issues**: [Submit issues or suggestions](https://github.com/huacc/metaAgentEngine/issues)
- **Discussions**: [GitHub Discussions](https://github.com/huacc/metaAgentEngine/discussions)

Feel free to contact us via email to discuss collaboration, technical exchanges, or joining the project development!

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## 🌟 Acknowledgments

Thanks to all developers and researchers who have contributed to this project!

Special thanks to the following open-source projects for inspiration:
- [LangChain](https://github.com/langchain-ai/langchain)
- [AutoGen](https://github.com/microsoft/autogen)
- [CrewAI](https://github.com/joaomdmoura/crewAI)

---

<div align="center">

**If this project helps you, please give us a ⭐️ Star!**

Made with ❤️ by Meta-Agent Engine Team

</div>
