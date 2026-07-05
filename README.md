# biweekly-artifacts

个人 AI Engineering Artifacts 仓库，用于持续沉淀真实研发过程中能够提升开发效率的 AI 资产。

这个仓库不是围绕某一种 AI 能力，也不是为了某一次汇报而创建。它面向长期积累：Prompt、Workflow、Checklist、Knowledge、Benchmark、MCP、Agent、Skill、Script、CLI、Template、Experiment 等都可以成为 Artifact。

## 核心理念

### 增强开发者，而不是替代开发者

AI 的职责是帮助开发者更快理解问题、减少重复劳动、生成初稿、分析代码、发现风险、提升效率。

AI 不应该完全替代开发者，也不应该跳过人工判断。任何自动化都应该保留明确的人工确认环节。

### 可持续积累

每个 Artifact 都应该可以复用、组合、持续优化，并随着真实使用不断演进。仓库的价值来自长期复利，而不是一次性产出。

### 面向真实开发

内容应来自真实研发场景，例如需求分析、代码开发、Code Review、调试、测试、文档、Git、CI/CD、AI Workflow、Prompt Engineering、Context Engineering、Benchmark、MCP、Agent、Skill、Workflow、CLI、Automation、Knowledge Base 等。

不要为了展示 AI 而创造不存在的需求。

### AI First, Personal First

默认优先思考：AI 是否能减少重复劳动？

但所有高影响决策都应由人确认。仓库首先服务于个人研发效率，其次才服务于团队协作。

## 推荐目录结构

```text
biweekly-artifacts/
├── README.md
├── CONTRIBUTING.md
├── artifacts/
│   ├── README.md
│   ├── agents/
│   │   ├── README.md
│   │   └── project-familiarization-agent/
│   │       ├── README.md
│   │       └── agent.md
│   ├── prompts/
│   │   └── README.md
│   ├── workflows/
│   │   ├── README.md
│   │   └── ai-assisted-code-review/
│   │       └── README.md
│   ├── checklists/
│   │   ├── README.md
│   │   └── ai-assisted-code-review.md
│   └── knowledge/
│       └── README.md
├── docs/
│   ├── README.md
│   ├── principles.md
│   └── roadmap.md
└── templates/
    ├── README.md
    └── artifact-template.md
```

## 为什么这样设计

- `artifacts/` 是核心资产区，按资产形态进行少量分类，便于后续扩展。
- `templates/` 放可复制的结构模板，保证新增 Artifact 的质量下限。
- `docs/` 放长期原则、演进路线和设计说明，避免 README 变得过长。
- 第一版只保留少量目录，避免一开始建立几十个空分类。
- 示例 Artifact 选择项目熟悉 Agent 和 Code Review Workflow，因为它们都是高频、真实、可复用的开发场景。

## 每个 Artifact 建议包含

每个 Artifact 至少说明：

- Problem：为什么存在
- Goal：解决什么问题
- Use Cases：适用场景
- Usage：如何使用
- Limitations：已知限制
- Roadmap：后续计划

可直接复制 [`templates/artifact-template.md`](templates/artifact-template.md) 创建新 Artifact。

## 第一版仓库内容

第一版建议提交：

1. 根 README，说明仓库愿景、原则、目录结构和使用方式。
2. `CONTRIBUTING.md`，说明如何新增、维护和评估 Artifact。
3. `templates/artifact-template.md`，作为所有 Artifact 的统一模板。
4. 各目录 README，说明职责和放置规则。
5. 真实示例：Project Familiarization Agent、AI 辅助 Code Review Workflow 和 Checklist。

## 使用方式

1. 从真实研发问题出发，而不是从 AI 能力出发。
2. 复制模板创建 Artifact。
3. 在实际任务中使用它。
4. 记录限制、失败案例和改进点。
5. 定期整理、合并、淘汰或升级 Artifact。

## 长期目标

经过持续积累，本仓库应逐步成为：

- 一套个人 AI Engineering Assets
- 一个可持续成长的知识库
- 一个研发效率工具箱
- 一个不断演进的 AI Playground
