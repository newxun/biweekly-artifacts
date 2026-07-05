# Contributing

这个仓库首先服务于个人研发效率。新增内容时，请优先判断它是否来自真实开发问题、是否能被未来复用、是否保留了人工判断空间。

## 新增 Artifact 的原则

新增 Artifact 前，先回答三个问题：

1. 它解决了哪个真实研发问题？
2. 它是否能在未来再次使用或继续演进？
3. 它是否增强开发者，而不是替代开发者做关键决策？

如果答案不清晰，先把想法记录到 `docs/roadmap.md`，不要急着创建新目录。

## 推荐流程

1. 从 `templates/artifact-template.md` 复制模板。
2. 放到最合适的现有目录。
3. 补全 Problem、Goal、Use Cases、Usage、Limitations、Roadmap。
4. 添加最小可用示例。
5. 使用一次后再根据实际反馈调整。

## 命名建议

- 使用小写英文和连字符，例如 `ai-assisted-code-review`。
- 名称描述问题或场景，而不是描述一次性任务。
- 避免使用过大的词，例如 `ultimate-agent`、`all-in-one-workflow`。

## 质量标准

一个可提交的 Artifact 应该：

- 面向真实研发场景。
- 使用方式清晰。
- 有明确边界和限制。
- 不承诺完全自动化。
- 可以被后续版本迭代。

## 何时创建新目录

只有当现有目录无法容纳多个同类 Artifact 时，才创建新目录。

例如：

- 已经积累多个 MCP 相关内容时，再创建 `artifacts/mcp/`。
- 已经积累多个 benchmark 或 evaluation 内容时，再创建 `artifacts/evaluations/`。
- 已经有可运行脚本或 CLI 时，再创建 `artifacts/automation/` 或 `tools/`。

## 维护节奏

建议定期做轻量整理：

- 删除不再使用的 Artifact。
- 合并重复的 Prompt 或 Checklist。
- 把临时经验沉淀为可复用模板。
- 把成功案例和失败案例补充到对应 Artifact。
