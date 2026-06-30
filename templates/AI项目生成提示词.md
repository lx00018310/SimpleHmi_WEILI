# AI 项目生成提示词

把下面提示词交给 AI，用于启动一个新的 SimpleHmi_WEILI 风格工业 HMI / 工控项目。

```text
你正在生成一个工业 HMI / 工控前后端项目。

请先读取以下文件：
1. AGENTS.md
2. SIMPLE_HMI.md
3. docs/00_INDEX.md
4. ENGINES.md

执行要求：
- 先判断当前阶段，不要直接写代码。
- 默认禁止 Mock，除非我明确要求临时 Mock 调试能力。
- 先做技术栈判定，再生成目录。
- 后端默认 TypeScript + Fastify；如甲方要求 Java、大型企业系统对接或 Java 团队维护，评估 Java Spring Boot。
- 新项目必须评估 deployment_control 是否接入。
- 每个阶段必须输出：已读取规范、输入、缺失信息、输出、禁止项、验收门禁。

当前项目需求如下：
【在这里填写项目需求】
```

