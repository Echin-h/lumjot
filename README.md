# Lumjot

开发者的环境式记忆层：在终端、Neovim、Agent 或浏览器里想到就记，之后自动整理到时间线和日历。

## 目标

Lumjot 解决的是“记录之前的寻找过程”——不需要离开当前工作环境，不需要先决定放在哪个笔记本，也不需要填写复杂的表单。

```text
Ghostty / Terminal / Neovim / Agent
              ↓
        一键快速捕捉
              ↓
       Inbox + AI 整理
              ↓
      时间线 / 任务 / 日历
```

## 设计原则

- 捕捉优先：一句话、一条命令就能保存。
- 本地优先：数据可用纯文本或本地数据库保存，支持离线和导出。
- 上下文完整：保存项目、Git 分支、文件、选区、终端和来源链接。
- AI 可控：AI 提供分类和日历草稿，正式写入日历前由用户确认。
- 可组合：CLI、Neovim 插件、MCP、Web 和移动端共享同一套数据模型。

## 计划中的入口

```bash
lumjot "重构 auth middleware，考虑拆出 token 刷新逻辑"
lumjot today
lumjot search "token refresh"
lumjot open <id>
```

Neovim 计划提供 `:LumjotCapture`、选区捕捉、今日时间线和搜索；Agent 通过 MCP 调用捕捉、检索、创建任务和生成日历事件。

## 文档

- [竞品调研与产品方向](docs/competitive-research.md)

## 状态

项目处于产品验证和 MVP 设计阶段。
