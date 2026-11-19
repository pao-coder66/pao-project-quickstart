# pao-project-quickstart

一个用于**快速上手陌生代码仓库**的 Agent Skill：三步分析（整体架构 → 核心模块 → 维护方式），产出一份带双图的精炼中文 Markdown 入门指南。

基于 [Sherenei/code_view_skill](https://github.com/Sherenei/code_view_skill)（codebase-onboarding）的三步走框架，叠加实战打磨的增强：

| 增强 | 说明 |
| --- | --- |
| §1.6 请求路径时序图 | 文字链路 + Mermaid `sequenceDiagram`，`box rgb` 按架构层着色；参与者 ≤7、消息 ≤25 条 |
| §2.0 整体架构视角 | 逐模块分析前先画 `flowchart` 架构图：分层 subgraph + `classDef` 颜色分块，节点标注小节编号，**领域层展开为与实际目录一一对应的子模块** |
| 双图配色一致 | 统一配色表（蓝＝前端、青＝呈现、绿＝应用、黄＝领域、紫＝基础设施、红＝装配根、灰＝进程外），两图可对照 |
| 精炼优先 | 图只承担导航职责：节点单行文案、同源箭头 `&` 合并、读图要点 ≤6 条，机制细节留正文 |
| 证据优先 | 设计缘由须有源码/文档佐证，不确定标「推测」；交付前双图自检 + 遗漏核对 |

## 安装

clone 到你的 Agent 技能目录（目录名与 SKILL.md 中 `name` 一致）：

```bash
# QwenWork
git clone https://github.com/pao-coder66/pao-project-quickstart.git ~/.qwenworkcn/skills/pao-project-quickstart

# Claude Code（如适用）
git clone https://github.com/pao-coder66/pao-project-quickstart.git ~/.claude/skills/pao-project-quickstart
```

新会话生效。触发方式：「快速上手这个项目 <路径>」「带我熟悉这个仓库」「项目 quickstart」。

## 产出

`项目入门指南-<项目名>-<YYYYMMDD>.md`，结构：

1. 项目整体架构（技术栈 / 依赖 / 构建命令 / 目录与入口 / **请求路径时序图**）
2. 核心模块逐一剖析（**2.0 颜色分块架构图** → 各模块 Why / 原则 / 模式 / 文件分布）
3. 项目维护方式（协作 / CI / 测试与评测门禁 / 质量 / 发布 / 文档 / 运维）
4. 下一步建议（3-5 条带 file:line 的学习路径）

## 致谢

三步走框架与证据优先原则来自 [Sherenei/code_view_skill](https://github.com/Sherenei/code_view_skill)。

## License

MIT