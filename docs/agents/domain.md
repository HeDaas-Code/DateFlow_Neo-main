---
title: DateFlow_Neo Domain Docs
type: agents-config
parent: AGENTS.md
---

# Domain Docs

**单上下文布局**——`CONTEXT.md`（根） + `docs/adr/`（入仓） + `工作Wiki/`（不入仓）。

## 何时开 ADR

- 引入新依赖（如新 UI 库）
- 改变核心模块（src/core/）的公共 API
- 重命名项目（DateFlow → InfoFlow 这种）
- 推翻旧视图架构

## 何时不开

- bug fix
- 文档更新
- UI 微调