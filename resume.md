# 方正

杭州 | [github.com/MMMarcinho](https://github.com/MMMarcinho) | marcooourifz@gmail.com | 15057171705

## 个人简介

前端工程师，长期参与蚂蚁保险业务和内部 AI 研发平台建设。目前负责蚂蚁财保 **AIMA 数字员工端到端研发平台**，覆盖前端、BFF、服务端、机器守护进程与 CLI 工具链全链路，围绕多 Agent 实时会话、上下文读写、长程任务围栏和研发过程可观测搭建 Agent 工作台。日常高频使用 Claude Code、Codex、OpenClaw、Hermes，并通过 AIMA 平台和开源贡献持续验证自己对 Agent Harness、记忆、状态管理和协作链路的判断。

## 核心技能

- **Coding Agent 与 Harness 工程**：深入使用 Claude Code / Codex / OpenClaw / Hermes，落地过生产可用的 Harness：多 Agent 实时会话、工具调用、上下文管理、长程任务状态追踪与研发过程可观测；熟悉 Agent Loop、Tool Use、MCP、Skill 与 Harness Engineering。
- **全栈与平台开发**：Node.js / Egg.js / Next.js / WebSocket / Redis / PostgreSQL，可独立完成 BFF、服务端接口、实时消息与平台型工具；另有 Go + Centrifuge 实时通信实践。
- **框架与工程化**：熟练 React 技术栈与状态管理、Webpack / Vite、Monorepo，能在复杂业务中推进可维护的工程结构与模块治理。
- **前端与网络底层**：熟悉 JavaScript / TypeScript、浏览器渲染、HTTP/HTTPS、缓存、跨域与性能指标体系，具备高 MAU C 端页面性能治理经验。

## 工作经历

**支付宝（杭州）数字服务技术有限公司** · 财富保险事业群 · 前端开发工程师 — 2022.07 至今

- 负责 **AIMA 数字员工端到端研发交付平台**，参与前端平台、服务端与数据库、机器守护进程、CLI 工具链等全链路研发。
- 负责蚂蚁财保**数字员工框架能力建设**，基于 OpenClaw、Codex 等多种 Agent 框架设计数字员工能力，参与整体交付围栏与长程任务能力研发。
- 曾作为前端 Owner 负责**蚂蚁保平台 C 端**产品的前端开发与性能优化。

## 项目经历

### AIMA 数字员工端到端研发平台 · 核心研发

技术栈：React + TypeScript + Egg.js + Node.js + WebSocket + Go + Centrifuge + PostgreSQL

- **平台定位**：面向财保技术部 2500+ 研发测试人员，建设统一的数字员工管理与自进化能力，把分散的 AI 研发探索沉淀为可复用的端到端需求交付工作台；核心目标是让 Agent 从个人辅助工具，逐步进入团队级需求交付流程。
- **Web 平台与服务端**：负责平台前端和 BFF 能力建设，支持**多 Agent 频道式协作、任务看板、会话详情、产物文档面板与实时状态同步**；围绕需求状态、Agent 过程日志、上下文和交付产物组织页面与接口，使研发过程沉淀在同一条可追踪链路里。
- **CLI 工具链与插件**：建设面向 Coding Agent 的命令和插件入口，提供远端信息查询、任务流转、上下文读写与结构化输出能力，把平台操作收敛成 Agent 可调用的稳定接口；通过实时通信协议接入 Claude Code / OpenClaw 等会话，让 Agent 能持续回传消息、日志与执行状态。
- **远程维护工作台**：基于 aima-ws 建设 **Go + Centrifuge + React 机器运维控制台**，统一管理多台研发机器上的在线客户端、daemon 配置和 Agent runtime 状态，支持在线状态 / 版本巡检、广播下发、单机重试和失败回溯。
- **巡检与广播链路**：支持按数字员工或 Shell 目标向在线机器下发广播，结合接收、回复、失败状态和回复内容抽屉追踪执行结果；后台定时巡检 daemon 域名、实时会话与广播状态，失败时生成可读原因并上报监控。
- **落地效果**：平台已在事业群内支撑 **1000+ 业务需求**的 AI 研发实践，推动需求研发、代码实现、过程追踪与经验复用从个人试用走向团队协作流程。

### aizo · Agent 本地偏好记忆层（Rust）· 个人项目

[github.com/MMMarcinho/aizo](https://github.com/MMMarcinho/aizo)

- **问题背景**：Coding Agent 的长期记忆如果完全交给 Agent 自主生成，容易堆积大量低价值偏好并污染后续上下文；aizo 将长期偏好从对话上下文中拆出来，做成**可解释、可衰减、可删除的本地记忆层**。
- **设计定位**：面向 Codex / Claude Code 等 Coding Agent，不保存完整对话，只沉淀偏好、习惯、边界和适用场景，让 Agent 在不同任务中按需取回项目偏好与用户习惯。
- **召回与权重**：支持按关键词、场景、分数区间和最低分过滤；设计基于**基础分 + 使用时间 + 半衰期**的动态权重，高分偏好衰减更慢，低价值记忆长期未用则降低召回概率，对重复录入做分数平滑。
- **工程实现**：使用 Rust + SQLite 完成本地持久化，提供记忆新增、召回、应用刷新、更新、删除、JSON 输出与本地 Web 面板，便于接入不同 Agent 工作流，同时保持数据本地可控和工具本身轻量。
- 目前在公司组内外进行推广，收获了较多使用体验反馈，以及对工具想法和效果的认可。

### 其他项目

- **coded**（[github.com/MMMarcinho/coded](https://github.com/MMMarcinho/coded)）：面向 Coding Agent 长程任务的本地状态管理工具，本地优先、框架无关，用 task / step 记录目标、进度与阻塞点，让 Codex / Claude Code 在换会话、压缩上下文后仍能低成本恢复任务现场。
- **AI 保险辩论创新产品（技术一号位）**：单人完成多 Agent 保险内容交互产品全栈落地，沉淀流式 Markdown 扩展渲染、业务卡片动态加载与 BFF 大模型调用封装能力。
- **蚂蚁保平台性能优化（前端 Owner）**：主导高 MAU 保险页面加载链路治理，通过 BFF 聚合、预请求、骨架屏、懒加载与缓存策略，降低 RPC 调用与首屏耗时。
- **amoji / agent-chatroom / WebVoyager-node**：围绕 Agent 人机交互、多 Agent 会话协作、浏览器自动化与工具调用链路的个人实验项目。

## 开源贡献

- **Multica** [#1935](https://github.com/multica-ai/multica/issues/1935) / [#3667](https://github.com/multica-ai/multica/issues/3667)：提出让 Agent 直接工作在用户本地项目目录中，核心不是增加路径配置，而是让 Agent 继承真实仓库的项目指令、本地改动与个人工具链。探索自定义本地运行时，推动 Multica 以更开放的方式接入公司内部或社区的 Coding Agent，而非只依赖少数内置 CLI。
- **cc-connect** [#1380](https://github.com/chenhg5/cc-connect/pull/1380) / [#1213](https://github.com/chenhg5/cc-connect/pull/1213)：补充按工作目录发送与会话路由，让消息端发起的任务稳定落到指定仓库并延续上下文；补充处理态 / 完成态反馈，让长耗时 Agent 任务对协作者可感知。
- **其它**：在 MCP Inspector、CodeWhale、Hermes 等 AI DevTools 项目中持续参与体验修正与能力探索，让 Agent 工具更理解真实工程环境、长会话状态与调试反馈。

## 荣誉奖项

- 蚂蚁集团**优秀新青年**；财保事业群**旗开得胜**个人奖项、**ACE** 奖项（事业群级个人绩效 / 突出贡献表彰）。

## 教育背景

浙江大学 · 测控技术与仪器 · 本科 | 2018.09 - 2022.07
