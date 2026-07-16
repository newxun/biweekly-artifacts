# Artifacts

这里存放能够提升真实研发效率的 AI 资产。

Artifact 可以是 Prompt、Workflow、Checklist、Knowledge、Benchmark、MCP、Agent、Skill、Template、Script、CLI、Experiment 等。第一版只保留少量分类，后续根据真实积累再扩展。

## 当前分类

- `agents/`：面向特定研发场景的 AI Agent 设计与可复用指令。
- `prompts/`：可复用提示词或提示词片段。
- `workflows/`：人机协作流程，强调步骤、输入、输出和人工确认点。
- `checklists/`：可在研发环节中重复使用的检查清单。
- `knowledge/`：经验、原则、模式、反模式和上下文工程资料。
- `evaluations/`：验证 Agent、Prompt 或 Workflow 行为与边界的场景化评估。

## 放置规则

优先放入现有目录。只有当某类 Artifact 已经有多个稳定条目时，再创建新的分类目录。

每个 Artifact 建议遵循：

- Problem
- Goal
- Use Cases
- Usage
- Limitations
- Roadmap
