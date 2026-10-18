# 竞品调研与产品方向

## 结论

现有产品分别解决了快速启动、日历任务规划、每日笔记、纯文本捕捉或 AI 整理，但在本轮样本中没有看到一个产品同时把以下链路作为核心：

> 终端/Neovim 原生捕捉 + 开发上下文 + AI 整理 + 日历时间线 + 本地优先 + Agent/MCP 扩展。

这构成 Lumjot 的切入点。

## 竞品观察

| 产品 | 可借鉴能力 | Lumjot 的差异机会 |
|---|---|---|
| Raycast | 全局入口、快捷键、Notes、Calendar、AI Actions | 以终端和编辑器为第一入口，而不是启动器 |
| Routine | 全局 Console、Universal Inbox、任务/笔记/日历、AI | 保留完整上下文，减少应用中心的重量感 |
| NotePlan | 每日笔记、任务、项目笔记、日历、时间块、Markdown | 把终端和 Neovim 捕捉放在核心路径 |
| Akiflow | Command Bar、任务收集、日历整合、时间块 | 补足长期笔记和知识检索 |
| Morgen | 快捷键捕捉、自然语言任务、来源 URL | 扩展到 Git、文件、代码选区和终端命令 |
| Tana | 结构化节点、日历同步、AI、外部消息捕捉 | 提供无结构负担的一句话入口 |
| Org-mode | 低打断 Capture、模板、Agenda、纯文本 | 用现代 CLI、Neovim 和 Agent 降低配置成本 |
| zk / zk-nvim | Neovim 内纯文本笔记、搜索和链接 | 增加日历、AI 分类和跨设备查看 |
| jot | 终端一命令捕捉、本地文档打开、日历助手尝试 | 建立统一的开发上下文和时间线模型 |

## 产品模型

默认把输入保存为时间线记录，而不是立即创建日历事件。只有当输入明确表达了行动或时间，例如“下周二 15:00 讨论 API”，才生成待确认的任务或日历草稿。

每条记录保存：

- 原始内容和创建时间
- 类型：note、task、event、reference
- 项目、Git 仓库、分支、文件和行号
- 来源 URL、终端命令或 Agent 会话
- AI 提取的日期、人物、标签和关联记录

## MVP

1. CLI 一句话捕捉、stdin 捕捉、本地存储、全文搜索。
2. Neovim 插件：快捷键、选区捕捉、当前文件和项目上下文。
3. 今日/每周时间线，支持从记录跳回原始内容。
4. 自然语言解析日期和任务，正式写入日历前确认。
5. MCP 接口：capture、search、today、create_task、schedule_event、open_note。

## 参考资料

- [Raycast Calendar](https://manual.raycast.com/calendar)
- [Raycast AI Extensions](https://manual.raycast.com/ai/ai-extensions)
- [Routine](https://routine.co/)
- [NotePlan](https://noteplan.co/)
- [Akiflow Integrations](https://product.akiflow.com/en/help/collections/1999346-integrations)
- [Morgen Easy Tasks](https://www.morgen.so/easy-tasks-by-morgen)
- [Tana Integrations](https://tana.inc/integrations)
- [Org Capture](https://orgmode.org/orgguide.pdf)
- [zk-nvim](https://github.com/zk-org/zk-nvim)
- [jot](https://github.com/Intina47/jot)
