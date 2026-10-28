# Aegyce

Aegyce supports two product forms: installation on an existing OS, and Aegyce OS, a complete operating system adapted to the Aegyce architecture. V1.0 delivers Aegyce OS, built on openEuler 24.03 LTS. Both forms share a system-level AI Harness core: it organizes model calls, tool use, and execution around user requirements. It is currently in architectural design. The four core features below describe the intended behavior.<br>
<sub>Aegyce 包含安装到已有 OS 和完整适配自身架构的 Aegyce OS 两种产品形态。V1.0 交付以 openEuler 24.03 LTS 为基础的 Aegyce OS。两种形态共用系统级 AI Harness 核心框架：围绕用户需求组织模型调用、工具使用与执行流程。项目目前处于架构设计阶段，以下四项核心特性均为设计目标。</sub>

- **Self-evolution**: Analyze work records and feedback to improve existing agents and create specialized agents. Validate candidate changes before adopting a new version, without inheriting permissions from past work.<br>
  <sub>**自进化**：分析工作记录与反馈，改进已有智能体，按需生成领域智能体。候选变更经验证后按版本采用，不继承历史工作的权限。</sub>

- **Security**: Enforce identity checks, permissions, runtime isolation, and data protection in code. Keep sensitive source data and replacement mappings local. Check protected requests before sending them to external models.<br>
  <sub>**安全**：由代码执行身份验证、权限检查、运行隔离和数据保护。敏感原文与替代映射保留在本地，发送给外部模型的请求须先经过保护和出口检查。</sub>

- **Self-organization**: Let each requirement coordinate agents, dependencies, and result validation. Support collaboration between Aegyce systems while each system checks its own permissions and resource limits.<br>
  <sub>**自组织**：由各需求协调智能体分工、执行依赖和结果验收。跨 Aegyce 系统协作时，各系统分别检查自身权限与资源限制。</sub>

- **Precise decision-making**: Choose actions using task goals, scenario rules, and the current state. Code handles explicit rules; decision models support semantic or uncertain judgments as needed. Framework code checks permissions, resources, and execution conditions before the responsible module acts.<br>
  <sub>**精准决策**：结合任务目标、场景规则和当前状态选择行动。明确的规则由代码判断，需要理解语义或处理不确定情况时调用决策模型。模型提出行动建议，框架代码检查权限、资源与执行条件，再由对应模块执行。</sub>

**Initial platform:** openEuler 24.03 LTS · **Language:** Rust · **Interface:** Terminal user interface (TUI)<br>
<sub>**首发平台：** openEuler 24.03 LTS · **开发语言：** Rust · **交互界面：** 终端用户界面（TUI）</sub>

The long-term direction is a general-purpose AI OS. The current framework does not replace the operating-system kernel or train foundation-model weights. Decision quality, performance, recovery behavior, and security controls require implementation and validation.<br>
<sub>长期方向是通用 AI OS。当前框架不替代操作系统内核，不训练基础模型权重。决策效果、性能、故障恢复和安全控制仍需实现与验证。</sub>

The [Aesy repository](https://github.com/Aegyce/agent-aesy) maintains Aegyce's general-purpose agent. [Aegyce Marketplace](https://github.com/Aegyce/aegyce-marketplace) distributes reusable components from agents. These may include skills, MCP integrations, tools, and other capabilities that can be used by AI tools through supported formats and interfaces.<br>
<sub>[Aesy 仓库](https://github.com/Aegyce/agent-aesy) 维护 Aegyce 的通用 Agent。[Aegyce Marketplace](https://github.com/Aegyce/aegyce-marketplace) 分发各 Agent 的可复用组件，可包括 Skill、MCP 集成、工具等，通过其他 AI 工具支持的格式与接口接入。</sub>

Original materials are licensed under [CC BY-NC 4.0](LICENSE). Commercial use requires [separate written permission](COMMERCIAL-LICENSE.md).<br>
<sub>原创内容采用 [CC BY-NC 4.0](LICENSE) 许可，商业用途须取得[单独书面授权](COMMERCIAL-LICENSE.md)。</sub>
