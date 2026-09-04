# Data Engineer · 数据开发工程师

*This document was created by **DeepSeek (deepseek-v4-pro)** on **2026-09-04**, compiled by reading the project repositories in the workspace (READMEs, design docs, source code, Git history) and the author's verbal descriptions.*
*本文档由 **DeepSeek（deepseek-v4-pro 模型）** 于 **2026-09-04** 创作，通过阅读工作区内的项目仓库（README、设计文档、源码、Git 历史）并结合作者口述介绍整理而成。*

> I build the data infrastructure that turns raw events into reliable, queryable insights — across batch & streaming ingestion, distributed storage, offline/real-time compute, and AI-facing data services.
>
> 我构建把「原始事件」变成「可靠、可查询洞察」的数据基础设施——覆盖批流一体接入、分布式存储、离线与实时计算，以及面向 AI 的数据服务。

---

## 👋 About Me · 关于我

My data career began as a **data analyst** — from 2020 I built the analytics framework, warehouse, and BI directly on raw game logs for overseas agency titles (**LOL, CODM, AOV, FIFA Online**, and more), later pivoting to internal new-project support. Watching raw-data quality constantly undermine those analyses pushed me toward engineering, with one clear goal: **improve data quality**. Today I'm a **data development engineer** with nearly 4 years of hands-on experience spanning the full data pipeline — and as AI reshapes the field, I'm leaning toward becoming a **full-stack data engineer**. My goal is to deliver **complete, end-to-end data solutions** for a project — not just optimize one link of the chain. My work sits at the intersection of **distributed storage, batch & streaming processing, and data engineering for mobile gaming & digital advertising**, and has been expanding toward **AI-facing data services**. I care about making data systems work *reliably at scale* — and I turn every task into a documented, reusable artifact.

我的数据之路始于 **数据分析师**——从 2020 年起，我直接在原始游戏 log 上搭建分析框架、数仓与 BI，服务海外代理游戏（**LOL、CODM、AOV、FIFA Online** 等），其后转向内部新项目支持。眼见原始数据质量问题不断拖累这些分析工作，我决心转向工程侧——目标只有一个：**提升数据质量**。如今我是一名 **数据开发工程师**，有近四年覆盖数据全链路的实战经验——随着 AI 演进，我更趋向于成为 **数据全栈**。我致力于为项目提供**全套的数据解决方案**，而不只是着眼于某一个环节。工作横跨 **分布式存储、批流处理，以及面向移动游戏与数字广告的数据工程**，并正朝 **AI 数据服务** 方向延伸。我在乎的不只是"能跑"，而是"在大规模下稳定可靠地跑"，并且习惯把每一个任务沉淀成可复用、有文档的东西。

---

## 🗓 Timeline · 时间线

- **2020–2021** — 以数据分析师身份起步：从原始游戏 log 搭建分析框架、数仓与 BI，服务海外代理游戏（LOL、CODM、AOV、FIFA Online 等）；在交接给海外团队后转向内部新项目支持，并因原始数据质量痛点萌生向数据工程转型的念头。
  **2020–2021** — Started as a data analyst: built the analytics framework, warehouse, and BI on raw game logs for overseas agency titles (LOL, CODM, AOV, FIFA Online, etc.); after handing off to the overseas team, shifted to internal new-project support — where raw-data quality pain sparked the move toward data engineering.

- **2022** — 在「老批式导入框架」上起步，面对其数据常常不可用与项目管理混乱的问题。
  **2022** — Started on the legacy offline ingestion framework, facing its data-unavailability and messy management.

- **2023** — 共同创建「新批式导入框架」；移动归因与第三方平台数据接入、Flink 任务管理平台运维与流任务管理。
  **2023** — Co-founded the new offline ingestion framework; mobile-attribution & third-party pipelines, Flink job-platform ops and stream-job management.

- **2024** — 批流接入与性能工程：新批式导入框架、Spark 性能诊断、YARN 资源治理、ScyllaDB 压测起步、运营用户名单系统。
  **2024** — Ingestion platform & performance engineering: batch-import framework, Spark profiling, YARN governance, early ScyllaDB load-testing, user-list generation.

- **2025** — 存储与广告接入深化：ScyllaDB 全面铺开（写入/监控/迁移）、广告买量数据接入、MCP 起步。
  **2025** — Deepening storage & ad ingestion: ScyllaDB at scale (write/monitor/migrate), ad-attribution ingestion, early MCP work.

- **2026** — AI 数据服务与集群级运维：ScyllaDB 集群拆分与多地部署、AI 查询网关体系（MCP + 元数据 + 安全护栏）、AI 分身与个人侧项目。
  **2026** — AI data services & cluster ops: ScyllaDB cluster split & multi-region, the AI query gateway stack (MCP + metadata + guardrails), AI digital-twin and side projects.

---

## 🧭 What I Do · 我的工作

**Batch & Streaming Ingestion · 批流一体数据接入**
Design and operate the core batch & streaming ingestion that moves data into the warehouse: batch importers for relational/object stores, Kafka-to-HDFS real-time landing, and scheduled offline ingestion into Hive — with incremental sync, late-data handling, and Airflow orchestration.

负责核心数据接入：面向关系库/对象存储的批式导入器、Kafka 实时落地到 HDFS、以及定时离线入库到 Hive——包含增量同步、延迟数据处理与 Airflow 调度。

**Distributed Storage · 分布式存储**
Deploy and operate multiple ScyllaDB clusters: routine node operations (add/remove nodes, repair), official ScyllaDB monitoring, and offline install — plus a Flink SQL connector for writing to ScyllaDB.

部署并运维多个 ScyllaDB 集群：常规节点运维（增减节点、repair）、官方 ScyllaDB 监控、离线安装，并提供 Flink SQL 写 ScyllaDB 的连接器。

**Real-time & Batch Compute · 实时与离线计算**
Operate a Flink job-management platform and its anti-cheat applications — an API to batch-launch punishment real-time jobs, plus a field-change detection job — and own long-term a real-time output task feeding the company's core dashboard. Batch side: Spark (performance diagnosis, YARN governance).

运维 Flink 任务管理平台及其反作弊应用——提供 API 批量上线处罚实时任务、字段定时变更检测——并长期负责把实时数据出仓到公司核心看板的下游任务；离线侧用 Spark（性能诊断、YARN 治理）。

**Schema & Data Serving · 建表与数据服务**
Own schema management and data serving: external-table schema sync (e.g. StarRocks), table design and SQL review, and turning ingested data into well-modeled, trustworthy tables for downstream teams.

负责 schema 管理与数据服务：外表 schema 同步（如 StarRocks）、建表设计与 SQL 审查，把接入的数据整理成下游可信任、口径清晰的表。

**AI Data Applications · AI 数据应用**
Build AI-facing data applications end to end — from safe query access to governed delivery. Query side: a production AI-query stack with clean separation of concerns — a unified read-only MCP query gateway (Hive / MySQL / ClickHouse; auth, SQL admission, execution routing, audit), a metadata & policy service (objective table facts + query policy — no permissions, no SQL execution), and semantic-layer skill packs, so LLM agents query data safely and accountably. Delivery side: a report platform for the AI-coding era — AI-assisted coding makes HTML data reports far faster to produce and iterate, but once reports multiply, update daily, and cross team boundaries, they still need a platform for identity, authorization, data contracts, and traceable releases; my platform lets analysts own the page and metric logic while it handles secure hosting and reliable delivery (SSO, role/membership authorization, manifest/contract between pages and data snapshots, versioned releases with rollback, optional read-only live binding).

构建端到端的 AI 数据应用——从安全查数到受治理交付。查询侧：生产级 AI 查询体系，职责分离——统一的只读 MCP 查询网关（兼容 Hive / MySQL / ClickHouse，负责认证、SQL 准入、执行路由、审计）、元数据与策略服务（客观表事实 + 查询策略——不做权限、不执行 SQL）、语义层 skill 包，让大模型安全、可审计地查数。交付侧：面向 AI 编码时代的报告平台——AI 辅助编码让 HTML 数据报告产出与迭代大幅提速，但报告变多、更新变频繁、跨团队后仍需统一平台负责身份、权限、数据契约与可追溯发布；该平台让分析师负责页面与指标计算，平台负责安全托管与可靠交付（SSO 身份认证、角色/成员授权、页面与数据快照之间的 manifest/contract 契约、可回滚的版本化发布、可选只读数仓实时绑定）。

**Platform Operations & Observability · 平台运维与可观测性**
Cluster monitoring and alerting (Prometheus exporters, Grafana dashboards), YARN metrics collection, Spark deployment governance, and infrastructure ops runbooks — including ScyllaDB cluster installation and inventory.

集群监控与告警（Prometheus exporter、Grafana 看板）、YARN 指标采集、Spark 部署治理，以及基础设施运维手册——包括 ScyllaDB 集群安装与资产清单。

**Internal Tools & Web Services · 内部工具与 Web 服务**
Build internal web services that put platform capabilities in non-engineering teams' hands — the flagship being an end-to-end audience-list service: a Django portal where OPS/OM teams self-serve targeting conditions (game, region, country, activity/churn window, payment flag, level range, small-account filtering) and name the audience; an offline PySpark + Airflow engine then computes the matching users from the warehouse, diffs against the previous snapshot to pick up only changes, and auto-uploads the refreshed audience to ad platforms on a daily schedule.

搭建面向非工程团队的内部 Web 服务，把平台能力交到业务团队手上——核心是一套端到端的人群包服务：Django 门户让 OPS/OM 团队自助配置定向条件（游戏、区域、国家、活跃/流失窗口、付费标记、等级区间、去小号过滤）并命名人群包；背后的离线 PySpark + Airflow 引擎从数仓按条件计算出匹配用户、与上一版快照 diff 只取增量，并按天自动把刷新后的人群包上传到广告投放平台。

---

## 📚 Deep Dives · 深入文档

- [数据接入 Data Ingestion](docs/ingestion.md) — 老批式导入框架 / 新批式导入框架 / 广告数据接入 / 实时落地服务 / 并发指标采集器 的功能逻辑
- [ScyllaDB 存储运维 ScyllaDB Storage](docs/storage.md) — 多集群部署运维、官方监控、离线安装、Flink 连接器
- [AI 数据应用 AI Data Applications](docs/ai-applications.md) — AI 查询体系（查询网关 + 元数据与策略服务 + 语义层技能包）+ 报告交付与数据可视化平台

---

## 🛠 Tech Stack · 技术栈

| 类别 Category | 工具 Tools |
|---|---|
| Storage 存储 | HDFS, ScyllaDB / Cassandra, TiDB, StarRocks, MySQL, PostgreSQL, ClickHouse |
| Compute 计算 | Apache Spark, Apache Flink, Hive |
| Messaging 消息 | Kafka |
| Orchestration & Infra 调度与基础设施 | Airflow, Docker, Kubernetes, YARN |
| Languages 语言 | Python（主力）, SQL, Scala, Shell, Go, TypeScript / Vue |
| AI & Data 面向 AI | MCP (Model Context Protocol), LLM integration, RAG |
| Observability 可观测性 | Prometheus, Grafana |

---

## 🎯 Areas of Deep Focus · 深耕方向

- **Batch/streaming ingestion & real-time ops** — designing robust import pipelines, and operating Flink real-time jobs.
  **大规模批流接入与实时运维**——设计健壮的导入管道，运维 Flink 实时任务。

- **ScyllaDB / wide-column storage** — deploying and operating multi-DC clusters: node add/remove, repair, official monitoring, and offline install.
  **ScyllaDB / 宽列存储**——部署运维多机房集群：节点增减、repair、官方监控、离线安装。

- **Data platform for AI** — exposing warehouses to AI via MCP, and designing complete data services for AI workloads.
  **面向 AI 的数据平台**——通过 MCP 把数仓开放给 AI，为 AI 应用设计完整的数据服务。

---

## 🎮 Side Projects · 个人侧项目

Beyond my day job, I build small end-to-end products to stay sharp across the full stack — for example:

- A **women's-football-themed web game** (squad building + manager simulation), including its desktop packaging and audio assets — playable at https://LucaXD-china.github.io/ball-girl-99/.
- An **AI "digital twin" demo** that gradually builds a personal clone from interactive journeys — code not public (an internal hackathon winner).
- A **personal A-share value-research tool** for low-volatility dividend indices.

工作之外，我也会做点小产品，保持全栈手感——例如：

- 一款**女子足球题材的 Web 游戏**（阵容构筑 + 经理模拟），含桌面端打包与音频资产——访问地址：https://LucaXD-china.github.io/ball-girl-99/。
- 一个**AI 分身 Demo**，通过互动旅程逐步构建个人数字分身——代码不公开（内部 hackathon 获奖作品）。
- 一个**个人 A 股价值研究工具**，聚焦红利低波类指数。

---

## 🚀 Recent Exploration · 近期探索

I'm currently expanding toward **AI + data infrastructure**: exposing warehouses through MCP, building AI data services, and prototyping ideas at the intersection of data platforms and LLM applications.

我目前正朝 **AI + 数据基础设施** 方向延伸：通过 MCP 把数仓开放给 AI、构建 AI 数据服务，并探索数据平台与大模型应用结合的可能。

---

## 📌 Principles · 工作方式

- **Data quality first** — I moved from analyst to engineer because bad raw data blocks everything downstream; I'd rather be a step slower than ship data others can't trust.
- **Anchor on the team's core need** — I orient my work around the most important problem the team is facing, and let that set where I focus.
- **Think end to end** — I aim to deliver complete data solutions for a project, not just optimize one link of the chain — from ingestion and storage to compute and the last-mile application.
- **Design top-down, build bottom-up** — I sketch the framework and architecture before coding, but implement from the ground up: prototype fast without pre-assuming complexity, then let real usage drive how the project evolves.

- **数据质量优先**——我从分析师转做数据开发，正是因为差的原始数据会拖垮一切下游；宁可慢一步，也不交付别人无法信任的数据。
- **锚定团队核心需求**——把解决团队最核心的需要作为工作重心与方向。
- **端到端思考**——致力于为项目提供全套数据解决方案，而不只是优化链条上的某一个环节——从接入、存储、计算，一直延伸到最后一环应用。
- **自顶向下设计、自下而上实现**——思考上先搭框架、再动手；实现上不预设复杂情景，先快速把原型落地，再按真实使用情形演进。
