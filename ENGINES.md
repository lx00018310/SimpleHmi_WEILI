# ENGINES: 技术栈判定规范

本文档定义 SimpleHmi_WEILI 的前后端技术栈选择规则。AI 必须先判定，再生成项目结构。

## 1. 默认组合

默认技术栈：

- 前端：React + TypeScript + Vite
- 后端：TypeScript + Fastify
- 接口：REST + WebSocket 或 Server-Sent Events
- 配置：外置配置 + 启动强校验
- 部署：评估 deployment_control

默认组合适用于中小型工业 HMI、Kiosk、工位看板、公共工控机服务、快速 MVP。

## 2. Java Spring Boot 使用条件

满足任一条件时，应优先评估 Java Spring Boot：

- 甲方明确要求 Java。
- 需要对接大型企业系统。
- 甲方或运维团队只接受 Java 生态。
- 项目包含复杂权限、复杂事务、长期企业级运维。
- 旧系统已经是 Spring Boot，迁移到 TypeScript 的风险更高。

Java Spring Boot 使用时，前端仍默认 React + TypeScript + Vite，除非用户明确要求复用旧 Vue。

## 3. 禁止静默选择

AI 在架构阶段必须输出：

- 选择 TypeScript 后端的理由；或
- 选择 Java Spring Boot 的理由；或
- 需要用户确认的缺失信息。

禁止写“为了简单默认选择某技术栈”而不解释现场约束。

## 4. 选型表

| 判断项 | TypeScript 后端 | Java Spring Boot |
| --- | --- | --- |
| 项目规模 | 中小型优先 | 中大型优先 |
| 交付速度 | 快 | 中等 |
| 前后端统一 | 强 | 中 |
| 企业系统对接 | 一般 | 强 |
| 甲方 Java 要求 | 不适合 | 适合 |
| 旧系统复用 | 需评估 | Java 旧系统优先 |
| 运维团队 | 前端/Node 可维护 | Java 团队可维护 |

## 5. deployment_control 判定

无论后端选 TypeScript 还是 Java，部署阶段都必须评估 deployment_control。

启用条件：

- 需要统一版本发布。
- 需要健康检查和回滚。
- 多终端需要统一状态。
- 项目从零开始，部署架构可控。

谨慎条件：

- 存量项目强耦合。
- 多硬件、多系统、多平台混杂。
- 现场问题需要极短排查链。
