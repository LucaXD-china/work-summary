# ScyllaDB Storage · ScyllaDB 存储运维

> 部署并运维多个 ScyllaDB 集群，覆盖常规节点运维、官方监控接入与离线安装。
> Deployed and operated multiple ScyllaDB clusters: routine node ops, official monitoring, and offline install.

## 概览 Overview

ScyllaDB 这块以**部署与运维**为主，而非大量额外开发：

- **多集群部署**：部署多个 ScyllaDB 集群（新加坡 / 美国等多机房），并负责日常运维使用。
- **常规节点运维**：熟悉增减节点、替换故障节点、repair 等常规操作。
- **官方监控**：搭建官方通用的 ScyllaDB Monitoring 监控工具，做集群与表级指标监控。
- **离线安装**：无外网环境下，用本地 deb 包安装 ScyllaDB。
- **Flink 连接器**：提供 Flink SQL 写 ScyllaDB 的连接器，供流任务使用。

## 部署与运维

- 部署多个 ScyllaDB 集群，负责日常运维使用——节点增减、故障节点下线与替换、repair 等常规操作。
- 搭建官方 ScyllaDB Monitoring 监控工具，接入 Prometheus / Grafana 做集群与表级监控。
- 整理集群安装 runbook 与资产清单（新加坡 / 美国多机房）。

## 离线安装与连接器

- **离线安装**：在无法访问官方 apt 源的环境，通过自带 deb 包安装 ScyllaDB。
- **Flink 连接器**：提供 Flink SQL 写 ScyllaDB 的连接器，让流任务用 SQL 直接落地。

## 我的角色 My Role

- 部署并运维多个 ScyllaDB 集群（新加坡 / 美国多机房）。
- 搭建官方 ScyllaDB Monitoring 监控工具。
- 整理离线安装包与集群安装 runbook。
- 提供 Flink SQL 写 ScyllaDB 的连接器。
