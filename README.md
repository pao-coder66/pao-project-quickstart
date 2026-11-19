# pao-project-quickstart

让 AI Agent 带你快速上手陌生代码仓库：三步分析，产出一份带时序图和架构图的中文入门指南。

## 1. 安装

clone 到 Agent 技能目录（目录名与 SKILL.md 中 `name` 一致），新会话生效：

```bash
# QwenWork
git clone https://github.com/pao-coder66/pao-project-quickstart.git ~/.qwenworkcn/skills/pao-project-quickstart

# Claude Code
git clone https://github.com/pao-coder66/pao-project-quickstart.git ~/.claude/skills/pao-project-quickstart
```

纯 prompt 驱动，无脚本、无额外依赖。

## 2. 使用

对 Agent 说「快速上手这个项目 /path/to/repo」「带我熟悉这个仓库」即可，也可以只要某一步：「只分析核心模块」。

Agent 需能读取仓库并执行 shell（目录侦察、`git log` 统计）。

## 3. 你会得到什么

一份 `项目入门指南-<项目名>-<YYYYMMDD>.md`，按上手顺序渐进展开：

1. **整体架构** —— 这是什么项目？技术栈、构建命令表、目录与入口，最后一张**多颜色时序图**讲清一条请求怎么流转
2. **核心模块** —— 先看**分层颜色分块架构图**建立全景（领域层展开为与目录一一对应的子模块），再逐模块讲设计缘由 / 原则 / 模式（含代码位置佐证）
3. **维护方式** —— 改代码前要遵守什么：协作流程、CI、测试门禁、发布与文档制度

末尾附 3–5 条带 `file:line` 的学习路径，照着走读即可。用 GitHub / Typora / VS Code 等支持 Mermaid 的渲染器查看（时序图分组着色需 Mermaid ≥10.3）。

## 4. 它如何保证质量

- **证据优先**：设计缘由须有源码/文档佐证，不确定标「推测」，查不到写「未发现」
- **图只导航**：时序图 ≤7 参与者、≤25 条消息，架构图节点单行文案——细节留正文，图不膨胀
- **双图同色**：同一架构层在两张图颜色一致（蓝＝前端、绿＝应用、黄＝领域、紫＝基础设施…），可互相对照
- **交付自检**：遗漏核对 + 精炼约束 + 语法可渲染，通过才出报告

## 5. 定制

整个 skill 就一份 `SKILL.md`：配色表在 §2.0，精炼阈值在 §1.6/§2.0，模块裁剪规则在 §2.1，报告结构在「验证与最终交付」。

## License

MIT
