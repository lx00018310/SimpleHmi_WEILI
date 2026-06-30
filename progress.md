# SimpleHmi_WEILI 重构进度

## 当前阶段

规范型开源项目重构首版。

## 本轮目标

- 将项目重构为 SimpleHmi_WEILI 规范型开源项目。
- 主目录只放新规范入口。
- 增加 `AGENTS.md`，让 AI 按阶段读取规范和模板。
- 建立规划、架构、Demo、开发、调试、部署、验收七阶段流程。
- 明确默认禁用 Mock。
- 明确后端技术栈判定：默认 TypeScript，复杂/大型/甲方要求时评估 Java Spring Boot。
- 明确 deployment_control 是标准能力，但新项目需评估是否接入。

## 已完成

- [x] 根入口：`AGENTS.md`
- [x] 总规范：`SIMPLE_HMI.md`
- [x] 技术栈判定：`ENGINES.md`
- [x] 开源说明：`README.md`
- [x] 许可协议：`LICENSE`
- [x] 阶段规范：`docs/`
- [x] 输出模板：`templates/`
- [x] deployment_control 规范入口：`deployment_control/README.md`
- [x] 静态示例页面：`examples/industrial-workstation-demo/`

## 下一步

- 根据后续使用反馈继续压缩规范。
- 如需要，再补最小代码模板；当前首要资产仍是规范、流程、索引和模板。
