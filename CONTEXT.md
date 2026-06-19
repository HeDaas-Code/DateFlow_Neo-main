---
title: DateFlow_Neo 领域术语表
type: context
status: active
last_updated: 2026-06-19
---

# CONTEXT.md — DateFlow_Neo 领域术语表

## 项目核心概念

### DateFlow / InfoFlow

**个人排期助手**——基于 PyQt5 + PyQt-Fluent-Widgets 的桌面应用。

**注意命名不统一**：
- README 标题：`DateFlow个人排期助手`
- `src/main.py` 内部：`"InfoFlow个人排期管理工具"`
- logger：`app="InfoFlow"`

**当前理解**：DateFlow 是产品名，InfoFlow 是内部项目代号（待 owner 确认）。

### 视图模式

| 视图 | 模块 | 用途 |
|---|---|---|
| 日程视图 | `ui/calendar_view.py` | 日历形式 |
| 甘特图 | `ui/gantt_view.py` | 时间线 / 任务持续 |
| 流程图 | `ui/flow_view.py` | 任务依赖关系 |

### 核心模块（src/core）

- `app_context.py`——应用上下文（依赖注入容器）
- `config_manager.py`——配置管理
- `plugin_manager.py`——插件加载
- `scheduler.py`——调度核心
- `subtask_manager.py`——子任务管理

### 插件系统

- 内置插件：`src/plugins/schedule_assistant/`
- 插件模板：`docs/plugin_template.zip`
- API 参考：`docs/plugin_api_reference.md`
- 开发指南：`docs/plugin_development.md`

## 项目特定命名

| 术语 | 含义 |
|---|---|
| **PyQt-Fluent-Widgets** | 第三方 Fluent Design Qt 控件库（`qfluentwidgets` 包） |
| **FluentTranslator** | 多语言切换器 |
| **QSplashScreen** | 启动画面 |
| **subtask** | 子任务（任务可拆解为 subtask） |
| **AppContext** | 应用上下文（IoC 容器） |

## 不混淆概念

- **DateFlow ≠ DateFlow_Neo-main**——后者是仓库名（带 "-main" 后缀，疑似 fork 命名）
- **InfoFlow ≠ DateFlow**——**这一致性需 owner 确认**
- **PyQt-Fluent-Widgets ≠ Qt Fluent**——前者第三方库，后者微软 Fluent Design
- **subtask ≠ task**——subtask 是 task 的子项

## 待补

- [ ] DateFlow vs InfoFlow 命名冲突——owner 确认
- [ ] src/data/ 子模块结构
- [ ] src/resources/ 内容（图标、splash 等）
- [ ] plugin 接口签名（plugin_api_reference.md 详细）