
根据来源《大语言模型驱动的自主代理综述》（A survey on large language model based autonomous agents），作者/组织对 “Agent” 的要求和定义区分如下：

### 1. 明确要求的能力/属性

这些属性是来源直接定义或明确指出 Agent 必须具备的，以区别于普通的 LLM 或传统系统。

* **处于环境之中且能感知与行动（Situatedness, Sensing, and Acting）：** 来源引用了 Franklin 和 Graesser (1997) 的定义，要求 Agent 必须是一个处于环境之中并作为环境一部分的系统，能够感知环境并对环境做出行动。此外，作者指出 Agent 必须能“自主地感知环境并从中学习”。
* **追求自身目标（Pursuit of own agenda）：** Agent 的行动必须是为了追求其自身的目标（Agenda），并以此影响其未来感知到的内容。
* **随时间推移的持续性（Over time）：** 代理的感知与行动过程是持续性的，而非单次触发。
* **自主性（Autonomy）：** Agent 需要具备“自我驱动的规划和行动”（self-directed planning and actions）能力来完成任务。
* **扮演特定角色（Role-playing）：** 作者明确指出，构建自主代理与简单的问答（QA）不同，Agent 需要“履行特定角色”（fulfill specific roles）。
* **自我演化（Self-evolution）：** Agent 被要求能够像人类一样通过从环境中学习来“进化自身”。

### 2. 来源反复强调但未明确规定为必要条件的属性

这些属性在文中频繁出现，通常作为研究目标或理想状态，但未被列入 Agent 的基础定义。

* **类人智能（Human-like Intelligence）：** 来源多次提到 LLM 使 Agent 展现出“类人智能”的潜力，并期望 Agent 获得“类人决策能力”。但这更多被视为 LLM-based Agent 的**优势或预期目标**，而非 Agent 概念本身的准入条件。
* **一致性与合理性（Consistency and Reasonableness）：** 文中提到记忆模块可以帮助 Agent 以更一致、合理和有效的方式行事，但未规定不具备这些特性的系统就不是 Agent。
* **社会性与协作（Social and Collaborative Capabilities）：** 来源在应用和未来方向中大量讨论了多代理协作和社会模拟，但这被视为特定应用场景的需求，而非所有 Agent 的通用必要属性。

### 3. 只是实现方式，而非 Agent 概念本身的属性

这些是来源提出的“统一框架”或技术手段，属于 Agent 的构建策略（Construction strategies）。

* **以 LLM 作为核心控制器（LLMs as central controllers）：** 虽然本综述的主题是基于 LLM 的 Agent，但作者承认这是一种“利用 LLMs 构建自主代理”的当代方法，其引用的原始定义（1997年）并不依赖于 LLM。
* **四模块架构（Profiling, Memory, Planning, Action）：** 作者提出了一个统一框架，包含配置模块、记忆模块、规划模块和行动模块。作者将其比作 Agent 的“硬件基础”，这只是作者为了总结现有研究而提炼出的**设计模式**。
* **具体的记忆结构（如向量数据库、短/长期记忆）：** 来源详细讨论了混合记忆、嵌入向量等实现方式，这些是增强 Agent 能力的手段。
* **能力获取策略（微调与非微调）：** 包括通过人类标注数据进行微调，或通过提示工程（Prompt Engineering）和机制工程（Mechanism Engineering）获取能力，这些被定义为 Agent 的“软件资源”获取方式。
* **外部工具的使用（External tools）：** 赋予 Agent 调用 API、数据库或外部模型的能力，这被视为扩展 Agent 行动空间的一种手段。

### 总结

根据该来源，一个系统被称为 “Agent” 的核心在于其**在环境中的自主感知-行动循环以及对特定角色和目标的追求**。而基于 LLM、拥有特定的四个模块或使用提示工程，均属于该综述所关注的特定实现范畴，而非 Agent 概念的通用约束。
