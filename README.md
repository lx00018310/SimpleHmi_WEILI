# SimpleHmi_WEILI

SimpleHmi_WEILI 是一个面向 AI 的工业 HMI / 工控前后端统一栈规范仓库。

本项目的核心不是堆代码，而是把标准、流程、索引、模板和避坑经验写清楚，让 AI 能按统一规则快速生成极简、可运行、可验收的工业工控系统。

## 核心入口

- [AGENTS.md](AGENTS.md)：AI 必读入口，说明各阶段该读哪些规范。
- [SIMPLE_HMI.md](SIMPLE_HMI.md)：总规范，最高优先级。
- [ENGINES.md](ENGINES.md)：技术栈判定规则。
- [docs/00_INDEX.md](docs/00_INDEX.md)：规范索引。
- [deployment_control/README.md](deployment_control/README.md)：部署控制能力规范。

## 示例页面

- [工业工位 HMI 示例](examples/industrial-workstation-demo/index.html)：静态视觉示例，用于直观看到按本规范生成的界面风格。

## 项目原则

- 规范优先，代码从属。
- 默认禁止 Mock。
- 默认先做技术栈判定。
- 新项目必须评估 deployment_control。
- 不搬运任何具体业务项目代码，只沉淀通用工程规范。
- 每个阶段必须有验收门禁。

## 推荐使用方式

给 AI 的第一条指令应包含：

```text
请先读取 AGENTS.md、SIMPLE_HMI.md、docs/00_INDEX.md 和 ENGINES.md，
判断当前处于哪个阶段，再按对应规范和模板输出结果。
```

如果是新项目：

1. 进入规划阶段。
2. 使用 `templates/需求澄清模板.md` 收口需求。
3. 进入架构阶段。
4. 使用 `ENGINES.md` 判定后端技术栈。
5. 进入 Demo 阶段。
6. 只生成最小可运行主链路。
7. 进入开发、调试、部署、验收阶段。

## 许可证

MIT License。任何人可以使用、复制、修改和分发。
