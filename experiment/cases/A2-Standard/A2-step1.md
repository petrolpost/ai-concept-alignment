
根据来源《Agents - OpenAI Agents SDK》，作者/组织对“Agent”的要求和定义可以区分如下：

### 1. 明确要求的能力/属性（Required）

根据来源中的“基本配置（Basic configuration）”属性表，只有一项被明确标记为“Required: yes”：

* **名称 (name)**：必须具备一个人类可读的 Agent 名称。

### 2. 来源反复强调但未明确规定为必要条件的属性

这些属性出现在 Agent 的核心定义中，或者被标记为“强烈推荐”，但在具体参数要求上被列为可选（no）：

* **基于大语言模型 (LLM)**：在“Agents”章节的起始定义中，明确指出“Agent 是一个配置了指令、工具和可选运行时行为的大语言模型 (LLM)”。但在属性表中，`model`（指定使用哪个 LLM）被标记为“Required: no”。
* **指令 (instructions)**：包含在 Agent 的核心定义中，且在属性表中被标注为“强烈推荐 (Strongly recommended)”，它可以是静态系统提示词或动态回调函数。
* **工具 (tools)**：同样包含在 Agent 的核心定义中，指 Agent 可以调用的功能列表。

### 3. 只是实现方式/可选功能，而非 Agent 概念本身的必要属性

这些项被来源明确归类为“可选（optional）”、“运行时行为”或属于多 Agent 系统的设计模式：

* **可选运行时行为 (Optional runtime behavior)**：
  * **移交 (handoffs)**：将对话委托给其他专家 Agent。
  * **护栏 (guardrails)**：对输入或输出进行验证/筛选。
  * **结构化输出 (output_type)**：要求 Agent 产生 Pydantic 对象等特定格式的输出，而非纯文本。
* **具体配置参数与实现机制**：
  * **prompt**：针对 OpenAI Responses API 的特定提示配置。
  * **model_settings**：如温度 (temperature) 等模型调优参数。
  * **hooks**：用于观察和记录 Agent 生命周期的回调函数。
  * **tool_use_behavior / reset_tool_choice**：控制工具调用后是继续由 LLM 处理还是停止运行的具体逻辑。
  * **mcp_servers**：基于 MCP 协议的工具服务器配置。
* **外部协作与支撑**：
  * **上下文 (Context)**：作为依赖注入工具传递给 Agent 的 Python 对象，用于存储状态。
  * **Runner**：用于运行 Agent 并管理回合、会话状态的编排组件。
  * **多 Agent 设计模式**：如“经理模式 (Manager)”或“移交模式 (Handoffs)”，这些是 Agent 协作的方式。
* **特定变体**：
  * **SandboxAgent**：在隔离工作区中运行并具有清单定义文件能力的特殊 Agent 类型。
