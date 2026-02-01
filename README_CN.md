# 元智能体引擎 (Meta-Agent Engine)

[English](README.md) | 简体中文

<div align="center">

**构建可持续长期运行的智能体协作框架**

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![GitHub Stars](https://img.shields.io/github/stars/huacc/metaAgentEngine.svg)](https://github.com/huacc/metaAgentEngine/stargazers)
[![GitHub Issues](https://img.shields.io/github/issues/huacc/metaAgentEngine.svg)](https://github.com/huacc/metaAgentEngine/issues)

</div>

---

## 📖 项目简介

**元智能体引擎**是一套创新的智能体编排框架，旨在构建能够**持续性长期运行**的智能体协作系统。不同于传统的单一智能体或简单多智能体系统，本项目实现了一个"生产智能体的智能体系统"——通过元智能体的协作，自动化地生产、组装、优化业务智能体及其协作流程。

### 核心理念

> **"不是用AI做事，而是用AI构建能做事的AI"**

本项目借鉴工业制造中的"母机"概念和软件工程中的"编译器"架构，让智能体系统具备自我生产、自我优化、自我进化的能力。

---

## ✨ 核心特性

### 🎯 智能体自动化生产

- **意图理解**：将模糊的用户需求转化为结构化的智能体蓝图
- **最佳实践注入**：自动检索行业标准和最佳实践，确保生产的智能体专业可靠
- **资产复用**：智能匹配已有智能体模板，避免重复造轮子
- **质量保证**：内置评估机制，确保生产的智能体符合质量标准

### 🧬 层级派生机制

支持智能体的层级派生，从通用到专业逐级深化：

```
L0 (通用) → L1 (领域) → L2 (专科) → L3 (细分)
示例：医生 → 内科医生 → 胃肠科医生 → 胃镜专家
```

**派生公式**：`派生智能体 = 继承(父能力) + 特化(专业知识) + 约束(边界限制)`

### 🔄 持续学习与优化

- **记忆系统**：长期存储知识、经验、用户偏好
- **模式识别**：从历史执行中提取成功模式
- **自动优化**：基于反馈持续优化Prompt和协作流程

### 🧩 灵活的组合能力

- **智能体组合**：支持多种智能体协作模式（串行、并行、混合）
- **Skill集成**：内置技能和外部技能的灵活组合
- **MCP协议**：支持标准MCP工具集成
- **工具扩展**：可接入各类外部API和自定义工具

### 👤 个人知识库

- **知识优先级**：个人知识 > 系统资产 > 互联网信息
- **多源学习**：支持主动注入、交互学习、反馈学习、行为观察
- **个性化定制**：基于用户习惯和偏好定制智能体行为

---

## 🏗️ 系统架构

### 元智能体体系（8个核心角色）

系统定义了8个元智能体，分为4个职能组：

| 职能组 | 角色 | 核心职责 |
|--------|------|----------|
| **情报组** | Researcher（情报研究员） | 检索外部最佳实践、行业标准 |
| | Asset Manager（资产管家） | 管理内部智能体模板、Prompt组件 |
| **设计组** | Architect（架构师） | 拆解意图，设计智能体蓝图 |
| | Weaver（织造者） | 编写System Prompt，赋予智能体灵魂 |
| **执行组** | Choreographer（编排者） | 设计协作拓扑（DAG/状态机） |
| | Orchestrator（调度者） | 运行时调度执行，管理上下文传递 |
| **运维组** | Evaluator（评估者） | 质量评估，拥有最终否决权 |
| | Learner（学习者） | 从历史中提取模式，持续优化 |

### 协同流程

```
用户意图
  ↓
[Researcher + Asset Manager] (情报收集)
  ↓
[Architect] (架构设计)
  ↓
[Weaver + Choreographer] (实例化)
  ↓
[Orchestrator] (执行)
  ↓
[Evaluator] (评估)
  ↓
[Learner] (学习优化)
```

### 智能体标准结构

每个智能体包含6个核心组件：

1. **基础信息 (Meta)**：ID、名称、版本、状态
2. **角色定义 (Role)**：角色描述、职能边界
3. **提示词 (Prompt)**：System Prompt模板
4. **技能 (Skills)**：内在技能、外部技能
5. **输入输出 (I/O Contract)**：输入规范、输出规范
6. **约束 (Constraints)**：能做什么、不能做什么

---

## 🚀 快速开始

### 环境要求

- Python 3.9+
- 支持的LLM：GPT-4、Claude 3.5、Gemini等
- （可选）向量数据库：FAISS、Chroma等

### 安装

```bash
# 克隆仓库
git clone https://github.com/huacc/metaAgentEngine.git
cd metaAgentEngine

# 安装依赖
pip install -r requirements.txt

# 配置环境变量
cp .env.example .env
# 编辑 .env 文件，填入你的API密钥
```

### 快速示例

```python
from meta_agent_engine import MetaAgentEngine

# 初始化引擎
engine = MetaAgentEngine()

# 生产智能体
result = engine.produce(
    user_query="我要构建一套智能问诊系统",
    domain="医疗健康"
)

# 获取生产的智能体
agents = result.agents
workflow = result.workflow

# 执行任务
output = engine.execute(agents, workflow, user_input="我头痛")
```

---

## 📚 文档

- [方法论文档](docs/方法论/元智能体引擎方法论.md)：完整的系统设计方法论
- [API文档](docs/api/)：详细的API使用说明（开发中）
- [示例集](examples/)：各种场景的使用示例（开发中）
- [贡献指南](CONTRIBUTING.md)：如何参与项目开发

---

## 🎯 应用场景

### 已验证场景

- **医疗问诊系统**：自动生成分诊员、问诊员、诊断员及协作流程
- **代码安全审计**：自动生成扫描员、分析员、修复建议员及审计流程
- **软件开发流程**：自动生成需求分析、架构设计、代码实现等智能体

### 潜在场景

- 法律咨询系统
- 投资分析系统
- 内容创作系统
- 业务流程自动化
- 教育辅导系统

---

## 🤝 贡献与招募

我们欢迎所有形式的贡献！特别欢迎以下方向的专家加入：

### 🔍 招募方向

| 方向 | 说明 |
|------|------|
| **大模型** | LLM应用、模型微调、Prompt工程 |
| **提示词工程** | 高级Prompt设计、Few-Shot学习、CoT优化 |
| **游戏引擎** | 实时系统设计、状态机、事件驱动架构 |
| **数字化方法论** | 企业数字化转型、流程优化、知识管理 |
| **本体方法论** | 知识图谱、本体建模、语义推理 |

### 如何贡献

1. Fork本仓库
2. 创建你的特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交你的改动 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 开启一个Pull Request

详细贡献指南请参考 [CONTRIBUTING.md](CONTRIBUTING.md)

---

## 📧 联系我们

- **项目负责人**：dongbeiler@gmail.com
- **GitHub Issues**：[提交问题或建议](https://github.com/huacc/metaAgentEngine/issues)
- **讨论区**：[GitHub Discussions](https://github.com/huacc/metaAgentEngine/discussions)

欢迎通过邮件联系我们，讨论合作、技术交流或加入项目开发！

---

## 📄 许可证

本项目采用 [MIT License](LICENSE) 开源协议。

---

## 🌟 致谢

感谢所有为本项目做出贡献的开发者和研究者！

特别感谢以下开源项目的启发：
- [LangChain](https://github.com/langchain-ai/langchain)
- [AutoGen](https://github.com/microsoft/autogen)
- [CrewAI](https://github.com/joaomdmoura/crewAI)

---

<div align="center">

**如果这个项目对你有帮助，请给我们一个 ⭐️ Star！**

Made with ❤️ by Meta-Agent Engine Team

</div>
