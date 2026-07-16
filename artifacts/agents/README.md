# Agents

这里存放面向真实研发场景的 AI Agent 设计与可复用指令。

Agent 应保持单一职责，明确边界，并遵循 Augment Humans, Not Replace Humans。它们可以帮助开发者理解、整理、检查和提问，但不能替代开发者做关键决策。

## 当前 Agent

- `project-familiarization-agent/`：帮助临时借调到陌生项目组的开发者，在编码前快速完成项目熟悉。

> `development-readiness-agent` 原在此目录，因其本质是人在环、跨会话的主线工作流，已改为 Skill 形态并迁至 [`../skills/development-readiness/`](../skills/development-readiness/)。

## 放置规则

每个 Agent 应包含：

- 适用场景
- 不适用场景
- 可直接使用的 Agent Prompt
- 输入要求
- 输出格式
- 已知限制
- 后续计划
