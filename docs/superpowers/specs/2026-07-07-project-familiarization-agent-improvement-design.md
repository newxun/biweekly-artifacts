# Project Familiarization Agent 改进设计

## 背景

当前 Project Familiarization Agent 的目标是帮助开发者在编码前熟悉陌生项目。实际反馈暴露了三个问题：

- Agent 偏重项目分析，但没有明确承担“帮助开发者把项目跑起来”的责任。
- Agent 主要输出对话式分析，但没有要求把分析结果沉淀成可复用或一次性的记录。
- 分析质量不稳定，因为现有规则对证据、启动验证和具体下一步约束不够强。

## 设计目标

- 保持项目分析是第一优先级。
- 在初步分析之后，把本地启动指导作为第二个重要职责。
- 要求轻量项目熟悉报告，让有价值的信息可以保存和复用。
- 提升输出质量，但不把这个 agent 扩展成 Coding Agent、Architecture Agent 或 Debugging Agent。

## 范围

这次主要更新现有 artifact，并保存一份轻量设计记录：

- `artifacts/agents/project-familiarization-agent/agent.md`
- `artifacts/agents/project-familiarization-agent/README.md`
- 在同一 artifact 目录下新增报告模板
- `docs/superpowers/specs/2026-07-07-project-familiarization-agent-improvement-design.md`

本次不新增可运行自动化，也不调整核心 artifact 目录结构。

## 行为设计

### 1. 项目分析仍然优先

Agent 仍然应该先理解仓库、显性文档、技术栈、目录结构、团队约定、当前需求、可能涉及模块和风险区域。

### 2. 启动帮助变成显式职责

完成初步分析后，agent 应该识别并引导开发者确认：

- 依赖安装命令。
- 本地开发启动命令。
- 构建、测试、lint 或 typecheck 命令。
- 必需环境变量、本地服务、数据库、队列、Docker 服务、Mock 服务或外部凭据。
- 启动是否已验证；如果没有验证成功，具体阻塞是什么。

Agent 可以帮助解读启动错误并整理下一步，但正常职责范围内不应修改业务代码。

### 3. 分析结果应该沉淀成文档

Agent 应该生成或建议用户保存一份轻量项目熟悉报告。这份报告可以是一次性的、面向当前任务的记录。它的作用是保存分析中真正有用的信息：

- 已确认什么。
- 哪些内容是基于证据推断的。
- 项目如何运行。
- 如果启动失败，失败在哪里。
- 当前任务相关模块和风险是什么。
- 仍需人工确认哪些问题。

### 4. 输出质量应该更具体

Agent 应优先输出有证据支撑的结论、命令结果、文件路径和 checklist，而不是泛泛总结。它必须明确标记未知信息，不能假装仅靠仓库分析就能恢复团队历史或业务决策。

## 验收标准

- Agent 指令明确要求在项目分析后进行本地启动检查。
- README 使用方式明确告诉用户可以期待项目理解、启动指导和可保存报告。
- Project Familiarization Agent artifact 下存在可复用报告模板。
- Agent 边界保持清晰：它服务于编码前熟悉项目，不变成通用 Coding Agent。
